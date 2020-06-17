---
layout: post
title: "Stories from Another Universe"
date: 2020-06-16
categories: bot
---

I just created my first Twitter Bot, [Stories from Another Universe][stories-universe]. 

This bot tweets out titles of media "from another universe". To create these titles I took popular media (books,
movies, games, etc) and substituted nouns & adjectives randomly. 
For instance, ***Indiana Jones and the Temple of Doom*** might become ***Indiana Jones and the Toilet of Doom***.
I was inspired to do this because my Order in the Court app has a similar function 
that generates random case names in the format
***The Case of the ADJECTIVE NOUN***. I enjoyed seeing the randomly generated phrases (some funnier than others), 
and wanted that 
feature to live on its own. That exact structure is used by this bot with 
***Sherlock Holmes and the Case of the ADJECTIVE NOUN***.
This uses some of the same code as Order in the Court does.

This app allowed me to experiment with the Twitter API and cron-jobs, both of which I am unfamiliar with. 
I used the Twitter Developer API a bit with Order in the Court, but this would be a more intentional use. 
I have never used CRON jobs outside of Travis CI. I set a cron-job on cron-job.org for this bot to trigger every
four hours.

I'm excited to see what titles this comes up with. Meanwhile, I'm thinking of other bots to build in the future.

[stories-universe]: https://twitter.com/StoriesUniverse