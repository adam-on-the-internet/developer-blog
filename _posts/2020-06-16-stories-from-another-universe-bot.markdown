---
layout: post
title: "Stories from Another Universe"
date: 2020-06-16
categories: bot
---

I just created my first Twitter Bot, [Stories from Another Universe][stories-universe]. 

This bot tweets out titles of books and movies "from another universe", which just means I have 
replaced nouns and adjectives from popular titles with random other nouns and adjectives. 
For instance, Eternal Sunshine of the Spotless Mind might become Eternal Sunshine of the Confused Mind.
I was inspired to do this because my Order in the Court app has a similar function 
that generates random case names in the format
"The Case of the ADJECTIVE NOUN". I enjoyed seeing this randomly generated phrases (some funnier than others), 
and wanted that 
feature to live on its own. This uses some of the same code as Order in the Court does, which made this a very
small bit of work.

This app allowed me to experiment with the Twitter API and cron-jobs, both of which I am unfamiliar with. 
I used the Twitter Developer API a bit with Order in the Court, but this would be a more intentional use. 
I have never used CRON jobs outside of Travis CI. I set a cron-job on cron-job.org for this bot to trigger every
four hours.

I'm excited to see what titles this comes up with. Meanwhile, I'm thinking of other bots to build in the future.

[stories-universe]: https://twitter.com/StoriesUniverse