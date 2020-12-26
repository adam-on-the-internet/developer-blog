---
layout: post
title: "The Quest Bot: Update 1"
date: 2020-12-26
categories: bot
---

Now that [The Quest Bot][qb-twitter] has been running for some time, I decided to make some major updates.
There have been a few tweaks [The Quest Bot UI][qb-ui] and lots of content added, but this is the first 
set of changes that actually adds to the original concept.

The Quest Bot is a Twitter bot that sends heroes on quests until they die. Originally, it used randomized stories
without any user input. Each story was entirely its own, without any connection to the others. 
With the new update I wanted to allow some user interaction and have some connection between the stories. 

The first part of the update allows anyone to interact with the current Hero through the [The Quest Bot UI][qb-ui].
The interaction is minimal, people can simply select to throw a snake or an apple in the hero's path to 
help or hurt them on their journey. This opens the door to more ways for people to interact in the future.

The second part of the update uses information about the heroes journeys to determine the state 
of the world. For instance, it compares the progress of Good and Evil heroes and uses that comparison to determine
if the world is overall Good or Evil. This is also minimal, but could be used in the future to affect the stories 
as they unfold. If nothing else, it provides fun statistics to look at.

Lastly, the world information and the general stats will be tweeted out each Sunday. This will provide a record
of the bot's overall progress and overarching story. 

For now, I will probably continue to make minor tweaks and content updates, but I am sure I will
add more significant changes in the future.

[qb-twitter]: https://twitter.com/TheQuestBot
[qb-ui]: https://adam-on-the-internet.github.io/the-quest-bot-ui
