---
layout: post
title:  "Events listing updates"
categories: jekyll
---
We've pushed some updates around the event listings. Previously, we were just relying on things being in the future, now it's much more dynamic!

Using some of the tags that Jekyll provides (which uses Liquid) we are able to apply some logic on what is shown. So, we have upcoming and previous events happening automatically and appearing in the right places.

You might be wondering what we have set up in order to achieve this. Well, we are making use of [collections](http://jekyllrb.com/docs/collections/) in Jekyll to add some front-matter about an event and then this is pulled in to the relevant layout file using an [include](http://jekyllrb.com/docs/includes/) with some parameters.

Below is an example event.

```
---
title: "#umbMeatUp - project by Callum Whyte"
host: "The Golden Guinea"
datetime:   2017-07-14 16:00:00 +0100
meetup: https://umbracobbq.com/
---
```

In our layout file, we have an include which pulls in the relevant events (as used in the [archive page]({% link archive.html %})). We then have a little bit of logic around what we want our events to render in the events listing. 

{% gist tcmorris/152188a6e744a05113fcda7e399a5437 %}

Hopefully that gives you an idea of how you can quickly build some useful functionality in to a static site using Jekyll. 

-- 

P.S. You might be thinking why we are writing about Jekyll when this is an Umbraco user group. We will definitely be posting about Umbraco a lot more in the future. The plan currently is to do some write-ups from the meetups we hold and also to talk about things going on in the umBristol community.