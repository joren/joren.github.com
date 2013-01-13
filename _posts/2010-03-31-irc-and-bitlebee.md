---
layout: post
title: "irc and bitlebee"
description: ""
category: 'tech'
tags: ['tech', 'irc']
---
{% include JB/setup %}

Lots of stuff at [Openminds](http://www.openminds.be) goes via irc, it started with our company channel for internal communication. After a while I found the joy of irc by joining community channels like #rails, #spree, #git, where, most of the time, you can find an answer really quickly.
But it was time to do more with it.

Since I'm mostly using Skype, I don't really run Adium anymore to connect with MSN, Google Talk or even Facbook chat, that just uses Jabber.
~

### Quick start
For a quick start, visit http://www.bitlbee.org/main.php/servers.html and connect to the server closest near you. After you got connected start by registering. Do use a good password for this step!

* `register *<password>*`

### Adding accounts
Then you can start adding some accounts. The syntax for this step is like this:

* `account add jabber handle password servertag`

In my case I wanted to ad my MSN, Google Talk and Facebook account. (you will need a [Facebook username](http://www.facebook.com/username/))

* `account add msn handle password`
* `account add jabber <username>@chat.facebook.com> <Facebook password>`
* `account add jabber username@gmail.com mypasswd`

you can find more information for more account types here: [https://help.ubuntu.com/community/Bitlbee#line-57](https://help.ubuntu.com/community/Bitlbee#line-57)

### Start chatting
After you created all your accounts, you can see them by typing `account list` and with `account on` you can activate all accounts.

With the command `blist on` you can see al you online account. When you use facebook chat you will see that all you buddies called somthing like u12345678456, which is pretty hard to remember :)
But no worries, there is a [script](http://browsingtheinternet.com/temp/bitlbee_rename.txt) which allows you to rename all those buddies.
Be sure to sign off and on after you loaded the script with 'account off' and 'account on'

So you wanne start a conversation? Type `/msg username message` to start one in en new window or just `user: message` for just a single IM.

For more stuff just use our good friend google.

There is a nice quickstart document with some basic commands to see your accounts, your buddies and much more. Download the [pdf](http://quark.humbug.org.au/publications/internet/bitlbee.pdf)
