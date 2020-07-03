---
layout: post
title: "Story Bot Update: Synonyms"
date: 2020-07-02
categories: bot
---

I enhanced by Twitter bot [Stories from Another Universe"][stories-universe] by adding a new type of message.
Originally, the bot sent out messages by changing a random word in a popular title 
(ex. Gone with the Wind -> Gone with the Juice). 
The new message type uses a thesaurus to find a synonym for one of the words in the title instead of a random selection
(ex. Gone with the Wind -> Gone with the Breeze). I was able to do this easily by using the datamuse api 
(http://api.datamuse.com/).

The bot now tweets out a message every 2 hours, alternating between the "random" and "synonym" messages. I'm
really enjoying seeing what the bot comes up with in both situations.

[stories-universe]: https://twitter.com/StoriesUniverse