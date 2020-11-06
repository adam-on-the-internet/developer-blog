---
layout: post
title: "The Quest Bot"
date: 2020-11-06
categories: bot
---

After a long hiatus from new projects, I am finally wrapping up my third (and by far, biggest) twitter bot, 
[The Quest Bot][qb-twitter]. It is a bot that 
randomly generates heroes and sends them on quests until they die. It is similar to The Clue Bot but
much more involved and with a lot more randomness. I wanted to create a bot that actual told a randomly 
generated story over time, a form of Emergent Storytelling,
and with what I learned through The Clue Bot I had the patterns to do so. 
I also created [a basic UI][qb-ui] to go along with the bot
so people can engage with it beyond Twitter.

Similar to my other Twitter Bots, The Quest Bot is part of my broader Node / Express service that runs on Heroku.
A Cron job is set to hit it often during the day to Tweet out updates as the story unfolds. The UI is a small
Angular project.

The bot has a flow for how it tells stories. If there are no living heroes, it creates one randomly and spends some
time giving their backstory and stats. It then sends them out on a random quest, which requires them to travel a certain 
distance before completing a task. As they travel, they encounter random events like fighting Goblins and
stopping to smell the roses. Once they reach their destination, they complete the quest's finale task and then 
take a moment to rest. As they rest, they gain some health and may level up. After resting, they are given another random
quest and so the story continues. Eventually, at some point in this flow, the hero will die and eventually 
be replaced by a new younger but weaker hero. It will be exciting seeing how long these heroes can live. With
the clue bot, every story took the exact same time, only the names changed. With The Quest Bot, there is a lot
more room for randomness.

At the start of this project I wanted it to be fairly simple, but I kept adding more and more until it is
what it is today. The random heroes each have several things that affect their journey such as stats and traits,
but they also have things that, at least for now, are just there to add flavor like race and alignment.

This bot safely falls into the "0-player game" category, a game that plays itself. This was an enjoyable first concept,
I look forward to developing other things like this in the future. 

I have more ideas to add to this, and lots of more content I intended to add, but for now it is in a good spot
to run on its own for a while. 

[qb-twitter]: https://twitter.com/TheQuestBot
[qb-ui]: https://adam-on-the-internet.github.io/the-quest-bot-ui
