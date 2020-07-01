---
layout: post
title: "App Migration"
date: 2020-06-30
categories: general
---

At the end of this month (June 2020) I ran out of Heroku app hours for the first time. 
I have updated the app locations in the [App Hub][app-hub]. 

I have been hosting
all of my apps through Heroku for months and this is the first time I hit the 1000 hours limit. I knew it was
going to happen, but had incorrectly assumed that their paid tier would be an overall upgrade to apps I had- turns
out the up-charge only upgrades a single app. I have over 10 apps on Heroku, so paying for all of them was not an
option.

For now, I am paying for my backend to have the paid upgrade. I have migrated a few of my Angular apps to GitHub Pages.
I do not like GitHub pages as much as Heroku as it feels a bit more hodge-podge to me. For example, in deploying 5 or so
apps to GitHub Pages, twice I had to delete my first attempt and try again to get it to work just because of some invisible
error. This was all a massive headache. I was very pleased to have all my apps on one service, and now they're 
spread out far more than I'd like. I'll see how the hours this week go, long-term I will probably find another solution.

I also migrated my Asset Library this week. I wanted the Library contents to be private, and the GitHub Pages free tier does 
not allow a private repo (more pain with GitHub Pages, I guess that's the theme). I now have the [Asset Reader][asset-reader] as 
a GitHub pages site which reads from a static Netlify site hosting the actual library contents. Needless to say,
more headaches. I think I'm in a better spot now on all accounts though.  

[app-hub]: https://adam-on-the-internet.github.io/app-hub/
[asset-reader]: https://adam-on-the-internet.github.io/asset-reader/