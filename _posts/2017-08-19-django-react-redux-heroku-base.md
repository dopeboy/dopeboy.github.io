---
layout: post
title: Running the Seedstars django-react-redux-base boilerplate project on Heroku
---
_Edit 02/04/19: This is outdated and I would not advise using it anymore. We now have create-react-app too. Also, I rushed to using redux during this period. I would argue against using redux (or any similar store solution) unless you have good reasons to use it. I've recently come up with an [alternative](https://github.com/dopeboy/django-react-docker-heroku) that might be more helpful._

One of the biggest pains with doing modern full stack web development is in the configuration of the toolchain. Luckily, the folks at [Seedstars](https://www.seedstars.com/) have put together a [fantastic boilerplate project](https://github.com/Seedstars/django-react-redux-base), based on Django & React + Redux, that does all of that for you. 

Here are the adjustments needed to get that boilerplate project deployed on Heroku. Because Seedstars constantly improves their project, these instructions are guaranteed to work at the time of this writing on release [b41971f](https://github.com/Seedstars/django-react-redux-base/tree/b41971fcfd20ae8feb068870c68db40856db36cb). I'm assuming you've already created a Heroku instance and that you're using Postgres.

## Instructions

1. We'll use gunicorn on Heroku. Add a `Procfile` to your root directory with the following contents:
```
web: gunicorn --pythonpath src djangoreactredux.wsgi
```
<br/>

2. Tell Heroku which python runtime to use. Add a `runtime.txt` to your root directory with the following contents:
```
python-3.6.2
```
<br/>
3. In `package.json`, in the `scripts` section, add a `postinstall` entry. This runs after a `yarn` (which runs a `npm install`) and has webpack generate the static JavaScript files you will serve:  
```
"scripts": {
  "dev": "....",
  "prod": "...",
  "postinstall": "yarn run prod"
}
```
<br/>
4. Tell Heroku details about node and npm. In `package.json`, in the root node, add an `engines` entry:
```  
"engines": {
  "node": "6.2.2",
  "npm": "3.9.3"
}
```
<br/>
5. For some reason, a hardcoded non HTTPS prefix is used for every request to the backend. This won't work on Heroku which by default serves on HTTPS. In `./src/static/utils/config.js`, clear the `SERVER_URL` variable:
```
export const SERVER_URL = '';
```
<br/>
6. Heroku expects a `requirements.txt` in the root whereas the Seedstars folks store in a directory. Create a `requirements.txt` in your root that refers to the files in the directory:
```
-r ./py-requirements/prod.txt
```
<br/>
7. We'll use `dj_database_url` to help Django get the database string from Heroku. In `./py-requirements/prod.txt`, add:
```
dj-database-url==0.4.2
```
<br/>
8. In `src/djangoreactredux/settings/prod.py`, add the following. Make sure to remove the exisiting `DATABASES` variable:
```
import dj_database_url
...
...
DATABASES = {}
DATABASES['default'] = dj_database_url.config()
```
<br/>
9. By default, Heroku skips installing everything in `devDependencies` in our package.json. To change that, run:
```
heroku config:set NPM_CONFIG_PRODUCTION=false
```
<br/>
10. Check out `./src/djangoreactredux/wsgi.py`. There's a line in there that says if we don't specify an environment variable, Django will load the dev settings file. To correct that, run:
```
heroku config:set DJANGO_SETTINGS_MODULE=djangoreactredux.settings.prod
```
<br/>

11. Set our buildpacks so that Heroku knows what kind of application we're pushing to it:
```
heroku buildpacks:add --index 1 heroku/nodejs
heroku buildpacks:add --index 2 heroku/python
```
<br/>

12. We're ready to push our code! This should go without a hitch:
```
git push heroku master
```
<br/>
13. Run the migrations and load the initial data from the fixtures and then open our project!
```
heroku run python src/manage.py migrate
heroku run python src/manage.py loaddata src/fixtures.json
heroku open
```


 


  

