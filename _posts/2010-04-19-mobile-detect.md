---
layout: post
title: "Mobile detect"
description: ""
category: 'arrrrcamp'
tags: ['tech', 'ruby', 'rails', 'arrrrcamp']
---
{% include JB/setup %}

Working on the [arrrrcamp](http://arrrrcamp.be) website we wanted a lighter version for mobile devices. Specially when people would visit the website during the event to see the schedule or more information about a talk or a speaker.

For the mobile design I use a very common and basic iPhone CSS and HTML framework [iphone universal](http://code.google.com/p/iphone-universal/).
At first we  would just tell everyone that you could visit [m.arrrrcamp.be](http://m.arrrrcamp.be), because users could then still visit the normal website.
But you can find all the information on the mobile version, so we could immediately redirect the users browsing with a mobile device to the mobile website.

A couple of weeks ago we found a nice Rack middleware that took care of this logic, [Rack mobile detect](http://github.com/joren/rack-mobile-detect). This middleware detects which device is visiting the website and adds a header to the request.
Because we use a different url for the mobile design, we added a redirect options which the author also added to his version.

So just install the gem `sudo gem install rack-mobile-detect`
and `require 'rack/mobile-detect'` to your environment.

Afterwards simply add `config.middleware.use "Rack::MobileDetect", :redirect_to => '/mobile'` and your mobile visitors will be redirected to the mobile version.

We did added some [page caching](http://guides.rubyonrails.org/caching_with_rails.html#page-caching) to make it faster.
