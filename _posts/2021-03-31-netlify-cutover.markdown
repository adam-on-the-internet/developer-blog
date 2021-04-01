---
layout: post
title: "Netlify Cutover"
date: 2021-03031
categories: general
---

After dragging my feet for months, I finally cutover two of my sites to use Netlify and Custom Domains.

My game "Order in the Court" was run on Heroku, which I found limiting for an Angular UI. Last year I had
bought a custom domain, so I took this time to use Netlify instead of Heroku and the custom domain instead of 
the Heroku domain. The app is now available [here][order]. The old Heroku app has a simple redirect page in its place.

My main professional app "Adam on the Internet" already had a custom domain but was also on the limiting Heroku
platform. It is still available [here][aoti], now with slightly better performance. 

Now, with a few exceptions, I use Heroku for my REST Services and GitHub Pages & Netlify for my user-facing UIs. 
In the future, I'd like to cut more off of GitHub Pages to Netlify, as the workflow feels cleaner to me, but
that is not a priority for me. I also find the Netlify works better with custom domains, but most of my projects
do not have custom domains.

[order]: http://www.orderinthecourtgame.com
[aoti]: http://www.adamontheinternet.com/
