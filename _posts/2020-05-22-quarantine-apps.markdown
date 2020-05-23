---
layout: post
title: "Quarantine Projects"
date: 2020-05-20
categories: general
---

COVID quarantine has given me time to wrap up and convert old projects, 
create a few small ones, and start a few longer-term ideas. 
This blog will cover my progress on these ventures (and beyond), but I wanted to recap my progress first.

Before quarantine, I had a series of small applications. Primarily, I had a cheap .club domain with 
shared hosting from Bluehost which held various (disorganized) projects. I wanted to get rid of this due to the cost
of shared hosting and the discovery that the cheap .club domain was blacklisted as "potentially unsafe" by many 
corporate firewalls. I already made the call to switch to a .com domain back in November 
so I didn't look sketchy to anyone checking out my work. With more free time, I had the chance to get off that setup and 
finally use the .com domain.
Some of these old projects were raw HTML, JS, CSS, and PHP, but others were Angular projects. I had a few other projects on 
Heroku already. I made judgments and selected which projects were
worth keeping around. Those that were deemed worthy were pulled into their own repositories and moved to free 
hosting on Heroku. The rest, mostly incomplete or older versions of current things, were deleted.

My main professional site is now [Adam on the Internet][adam-on-the-internet]. This is one of the few custom domains
I have purchased. It is an Angular UI that gets its data from a Node.js Express App, which pulls from a Mongo database.
This Express app is hosted for free on Heroku and used for most of my projects. Because of how the free tier of Heroku 
implements apps that "sleep" when they are unused,
it makes the most sense to have one Express application for all my endpoints. I also preferred to have one set of users and login credentials
to manage between all my apps, though that could've been handled with separate Express apps as well.
The Mongo database is a free cloud database
running on Mongo Atlas. For my simple projects, I found Mongo more appropriate than SQL. Most of my UIs are either Angular apps or just simple HTML. 
I have simple setups to run both of those types of UI on Express, so setting up a deployment pipeline takes minutes. 
The Express app and Mongo database have a Prod and Nonprod version, as do some UIs.

I now had these apps in an acceptable state to release into the world. Most were not "done", but when is an application ever done? 
This new fleet of apps got a bit annoying to manage, so I created an [App Hub][app-hub] to link to my projects. 
The apps on this site are either "Featured", "Other", or "Archived". Nobody can see the "Archived" projects without logging in.
It feels good to have everything wrapped up or tossed out, allowing me to just work on one or two higher priority apps at a time.
Currently, I'm working on Order in the Court and Chit Chat, which you'll hear about in other blog entries.

You can out what's currently available [HERE][app-hub]. As I write this, these applications are available:

# Featured
* Order in the Court : my current main project, a browser-based game perfect for quarantine
* XPath Assistant : a small older project I built as a dev tool for myself
* Adam on the Internet : my main professional site
* Armor Equipment : an older site I built for a small company

# Other 
* Zoom Backgrounds : a collection of some Zoom backgrounds I found on twitter
* User Management : my admin app, mainly used to manage login credentials
* Basic Angular App : a sample application that demonstrates Angular with no styling. 
* Overton Portfolio : a portfolio prototype for a project I did not complete
* Basic Express App : the API for most of my applications
* Story Dice : a converted version of a very simple old app that acts as virtual dice
* Kids Book Debate Club : a site for a debate club I'm running 
* Spectre Squad : a converted version of a companion app for a board game I made in college
* AI Minesweeper : a python project that tries to solve Minesweeper
* DES Encryption : a college project that tries to solve DES Encryption
* Developer Blog : a Jekyll blog for my development progress
                                 
[adam-on-the-internet]: http://www.adamontheinternet.com/
[app-hub]: https://aoti-app-hub.herokuapp.com/


