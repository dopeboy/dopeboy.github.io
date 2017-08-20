---
layout: post
title: Running the Seedstars django-react-redux-base boilerplate project on Heroku
---

One of the biggest pains with doing modern full stack web development is in the configuration of the toolchain. Luckily, the folks at [Seedstars](https://www.seedstars.com/) have put together a fantastic boilerplate project, based on Django & React + Redux, that does all of that for you. 

Here are the adjustments needed to get that boilerplate project deployed on Heroku. Because Seedstars constantly improves their project, I can guarantee that these instructions work at the time of this writing on release [b41971f](https://github.com/Seedstars/django-react-redux-base/tree/b41971fcfd20ae8feb068870c68db40856db36cb). 

## Instructions

1. Add a `Procfile` to your root directory with the following contents:
``
web: gunicorn --pythonpath src djangoreactredux.wsgi
``




