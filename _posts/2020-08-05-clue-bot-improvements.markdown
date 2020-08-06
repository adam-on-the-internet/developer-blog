---
layout: post
title: "Clue Bot Update: Improvements"
date: 2020-08-05
categories: bot
---

I recently enhanced my Twitter bot [The Clue Bot][clue-bot]. This bot creates murder mysteries with 
a random culprit, murder weapon, and crime scene and then provides clues to slowly reveal the solution.

I had previously set up this bot to run specific day phases. 
The bot had 7 updates a day, every 7th with a day-ending message. I found that slow networks occasionally 
made the updates fail leading to the bot getting off of its cycle and not knowing when to send the day-ending message.
I decided to simplify my bot by cutting out the 3 day-ending messages and just letting it run in a cycle.

Now, each mystery has 24 updates. One clue is revealed each hour, so usually there is one mystery per day.
However, if the bot messes up and misses a message, the tweets will all still make sense since there aren't 
messages that specify any sort of day or time. This will make the bot much easier to maintain.

Additionally, I cleaned up [The Clue Bot UI][clue-bot-ui] and added a "clue tracker" display that 
uses the updates the bot has announced to solve mysteries on its own by eliminating items.

Hopefully The Clue Bot can live on its own for some time without any updates. I'm excited to 
see what it comes up with!

[clue-bot]: https://twitter.com/TheClueBot
[clue-bot-ui]: https://adam-on-the-internet.github.io/the-clue-bot-ui/
