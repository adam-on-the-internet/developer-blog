---
layout: post
title: "Vaudeville Mews Bot"
date: 2021-12-04
categories: bot
---

Today I wrapped up my [Vaudeville Mews Twitter Bot](https://twitter.com/VaudevilleMewsB)
that tweets "Today at the Vaudeville Mews..." messages using a
[data of Vaudeville Mews shows](https://adam-on-the-internet.github.io/vaudeville-mews-archive/) 
I archived earlier. This bot is dedicated to the recently-closed local Des Moines Venue of the same name.

I released the bot before completing it, and it immediately became more popular than any of my other
bots. Originally, it tweeted out 12 shows a day at random. As of now, it tweets 2 early shows, 2 late shows,
and one irregularly scheduled show per day. This should make it a little less noisy and also might make each tweet
a little more special. 
I also had it calculate the length of each tweet just in case
any show had too many bands to fit in 280 characters. 

This bot works via a [cron job](https://cron-job.org/en/) that routinely hits a NodeJS API.
Most of that API was already in place for the archival site, but I added a bit to make this bot work smoothly.

Looking forward, there are some improvements I could make:
 - Completing the data set (I'm missing data from December 2002 to November 2008)
 - Adding pictures, stories, and other archival content
 - Putting safeguards around duplicate tweets (there's a slim chance it could randomly tweet the same show twice)
 - Filtering out some shows (cancelled shows, postponed shows, shows with certain bands now known to be predators)
