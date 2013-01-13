---
layout: post
title: "new blog powered by toto"
description: ""
category: 'tech'
tags: ['tech', 'ruby']
---
{% include JB/setup %}

### A little History
Back in the old days I started blogging with [Geeklog](http://www.geeklog.net/), this evolved to [Xoops](http://www.xoops.org/) an later on to a basic [Wordpress](http://wordpress.org/).

When I started with Rails, first I wanted to build my own system, customize it to my needs. But after the first edition of [ArrrrCamp](http://arrrrcamp.be) the guys of [Gorilla Webdesign](http://gorilla-webdesign.be) could convince me to try [Radiant](http://radiantcms.org/).
~
I liked the system, but as I wanted to post more media, the flow was to slow. For this I started using ['tumblr'](http://jorendegroof.be) where I can dump the media I collect on the internet.

Still, my radiant blog, which I use mainly for technological stuff was to slow, I needed something smaller, easier and I wanted to be able to write posts without login in, saving the post when it wasn't ready, continue typing offline on the train. Which isn't possible with Radiant or any other online system.

### Toto
Then I bumped into [Toto](http://cloudhead.io/toto) a git powered, minimalistic blog engine, entirely build on [Rack](http://rack.rubyforge.org/). You just

If you have an account on [Heroku](http://heroku.com/), it really just takes 10 seconds to have it online.

### Customizing
After I played with it for a while, adding some extra functionalities to it like [rack-google-analytics](http://rubygems.org/gems/rack-google-analytics) and [rack-rewrite](http://rubygems.org/gems/rack-rewrite) to have my old posts still working. All just added to the *config.ru* file.
I really like the lightness of Rack and this blog. It maybe has 300 lines of code and is superfast.

### Deploying
After that I just had to add a very simple capfile and deploy it on the account where used to run my Radiant blog.
You could just use a [default passenger capfile](http://underpants.openminds.be/questions/kan-ik-werken-met-capistrano) but skip all the database and assets stuff.

Just give it a try yourself!
