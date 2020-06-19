---
layout: post
title: "The Clue Bot"
date: 2020-06-19
categories: bot
---

I just created my second Twitter Bot, [The Clue Bot][clue-bot]. 

This bot runs through cycles with randomly-generated murder mystery stories! It has bits and pieces of
project ideas I've worked on and imagined before. I was surprised how quickly this came together. It is essentially
a mixture of Order in the Court, which creates prompts for users to make stories, and Stories from Another Universe Bot,
which just tweets out a random parody story title every four hours. After completing that Story Bot, I realized 
how easy it would be to make a more interesting bot that actually progressed through a story. And so, I created The Clue Bot
over a couple days. 

The Clue Bot let me use random-generation a lot. 
The bot randomly picks a case title in the pattern ***The ADJECTIVE MYSTERY-WORD of the IMAGINARY-LOCATION***, and it makes sure not to repeat.
There are enough combinations of the words I have provided to create over 37500 unique titles, 
so, with the current 3-day game cycle, my game can last over 100 years without repeating a title. After picking a title,
the bot gets sets of items, treated as cards for a board game: 12 Weapons, 13 Suspects, and 12 Locations. 
One suspect (unlucky #13) becomes the victim. Then the bot makes selections: one of each become the "true" answer to the murder, 
5 of each are possible options, and 6 of each are potential decoys. The bot shuffles the possible options together, and the game begins.

The first phase of the game consists of four tweets. The first introduces the story by describing the crime. 
The next three provide the lists of possible Suspects, Weapons, and Locations.

The second phase of the game consists of fifteen Clue tweets. Each of these Clue tweets eliminates one potential option.
These tweets also sometimes add in decoys to add some complexity. The text of the Clues is randomly-generated based
on the Clue type (Weapon, Location, or Suspect). 

The third and final phase consists of one tweet calling for answers and then one last tweet giving the solution.

All together, there are 21 tweets to tell one story. I am setting up a Cron-Job to trigger the bot 7 times
a day, meaning a new cycle will start every 3 days. It is pretty straight-forward to get the right answer with the 
clues provided, but I 
think it will still provide an interesting experience! I don't know any other Twitter bots like this. I have some ideas
to make this bot much more interesting but I am not planning on spending time on those any time soon.

I think I'm moving onto other projects (not Twitter bots) for a while, but I'm already starting to get more story-telling
ideas like this one. It would be especially neat to have any sort of interactivity, though that's currently beyond
my knowledge. For now, this will do!

[clue-bot]: https://twitter.com/TheClueBot