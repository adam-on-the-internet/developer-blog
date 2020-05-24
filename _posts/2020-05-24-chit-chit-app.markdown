---
layout: post
title: "Chit Chat App"
date: 2020-05-24
categories: chat
---

I took a short break from working on other apps to create a new small app, [Chit Chat][chit-chat]. This was a nice
change of pace from the bigger projects I was working on, as I was able to go from an idea to "done" in less than a week.

The idea of the app is based off cards I found at a thrift store once. Each card had a conversation topic on it. I 
have already made virtual card decks before, so I already had everything I needed to make a small app that 
acted like these cards. I went beyond the physical card decks by allowing user suggestions for questions. When users
suggest a question, the question is saved but flagged as "hidden" so that I can manually approve submissions 
(and therefore avoid any bad actors). I get 
an email when each suggestion is made.  

The app consists of an Angular frontend with Bootstrap 4 (which includes Font Awesome) that connects to the same backend 
most of my apps use: an Express app that talks to a Mongo database.

Beyond adding more questions, I consider this app completed. Three features I considered but didn't build out were 
adding more styling, namely animations to make the card drawing more like actually drawing a card, getting
daily or weekly emails with suggestions, and having a twitter account automatically tweet out a random question once 
per day. I may return to this app at some point to build those out, as they all cover things I don't have much
experience with: advanced styling / animations and timed jobs. 
That shows how small projects like this help me, I will be able to practice new ideas with this app
without disrupting a more complicated project. 

[chit-chat]: https://aoti-chit-chat.herokuapp.com/