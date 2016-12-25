---
layout: post
title: Rendering a HTML link across Gmail, Outlook, and iCloud mail
---

I came across an interesting bug recently that had me scratching my head for awhile. A client of mine wanted his web application to send emails to users. The body of the email would contain links. 

Simple enough I thought. I've done this before. I'll use Mailgun's API and send raw HTML in the payload. I did exactly that and then we started testing. We had the web application send an email to a Gmail account and it rendered as follows:

<img src="https://s3-us-west-1.amazonaws.com/dopeboy/render-email-blog-post/rendered_gmail.png"/>

OK great. And the link works too. We did the same with an iCloud account and something funny happened:

<img src="https://s3-us-west-1.amazonaws.com/dopeboy/render-email-blog-post/rendered_icloud.png"/>

That's just text. Strange. We did the same again with an Outlook account and something funny happened again:

<img src="https://s3-us-west-1.amazonaws.com/dopeboy/render-email-blog-post/rendered_outlook.png"/>

Uhh OK. ALmost looks like markdown. 

My first thought was maybe the mail server was changing the message's source code. I checked and the source was the same across all three clients. I went back to my code and checked exactly what I was sending out:

```
domain = "example.com"
url = domain + "/building/show/" + str(building.id)
email_text = "<html><head></head><body><a href='" + url + "'/>Camille Rouge Apartments</a></body></html>"
api_call_to_mailgun(email_text, ...)
```

Hmm. Let's see how the link gets rendered in each of the three web clients. I went to each and inspected the link element. Gmail gave me:

```
<a href="http://example.com/building/show/123" target="_blank" data-saferedirecturl="https://www.google.com/url?hl=en&amp;q=http://example.com/building/show/123&amp;source=gmail&amp;ust=1482686872740000&amp;usg=AFQjCNGDsVUEvhZC0ztVDi5B9IQWMM266Q">Camille Rouge Apartments</a>
```

Interesting. Gmail's client injected the "http://" prefix into the 'href' attribute. And what did Outlook do?

```
[example.com/building/show/72a53035-a2c5-4e8e-924f-eec8c5d4408c]Camille Rouge Apartments
```

That is plain text. Outlook drops the `<a>` tag altogether. And iCloud mail?

```
<a>Camille Rouge Apartments</a>
```

Am I sending out non-compliant HTML? I went over to the [W3C HTML validator](https://validator.w3.org) and checked:

<img src="https://s3-us-west-1.amazonaws.com/dopeboy/render-email-blog-post/w3c.png"/>

Nope. What is going on? Well, we know the link works in Gmail and we also know it is injecting the protocol prefix. Let's try putting in the prefix ourselves:

```
domain = "https://example.com"
url = ...
email_text = ,,,
api_call_to_mailgun(email_text, ...)
```

And that actually worked! Looks like the iCloud and Outlook clients are picky.

Moral of the story: include the "http[s]" prefix in your `href` attributes. Hope that saves someone out there some unncessary head scratching.