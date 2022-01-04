---
layout: post
title: "Mystery Mansion Companion"
date: 2022-01-03
categories: general
---

Over the holidays I created a [Mystery Mansion Companion](https://github.com/adam-on-the-internet/mystery-mansion) app that runs in command-line.
This app was created to go along with the 1995 board game [Electronic Talking Mystery Mansion](https://www.google.com/url?sa=t&rct=j&q=&esrc=s&source=web&cd=&cad=rja&uact=8&ved=2ahUKEwi9noG175b1AhVNOs0KHbc7CZ0QFnoECAYQAQ&url=https%3A%2F%2Fboardgamegeek.com%2Fboardgame%2F2343%2Felectronic-talking-mystery-mansion&usg=AOvVaw1l2UJ_GkTK4WKigWIzQvRY) (Mystery Mansion for short),
which uses a small electronic "organizer" to run part of the game.

In Mystery Mansion, players compete to find the money hidden in a mansion of randomly-generated rooms (some of which are locked), 
which each contain partially randomized furniture that can be searched for clues (item cards), hints (public or private), or the hidden money.
The first perosn to find the money (which requires two specific Clues, a person and an item) wins.

My family owns a copy of this game and we played it often growing up. We were worried that someday the electronic device may stop working and the game may become unplayable.
To prevent that possibility, 
I decided to reverse-engineer the game logic of the device as much as possible and then create an app to replace it, without worrying about making a true one-to-one replication.
This was done through a combination of examining the game itself and talking with my family to remember how the game worked.
For instance, the core game should play the same way (the clues, furniture, rooms, and hints should use the same setup as the original)
but the randomization of what furniture appears in what room could behave differently, as this wouldn't be apparent to the player.

I decided to work on this project in Python 3, since I wanted to experiment more with Python and because it felt appropriate
for a small game project. At first, I would have the Python App read some settings from static local .csv files and then create
a markdown file with the game's setup. Having the markdown made for easy debugging and visualizing the game logic. In theory, 
a "game master" could run the game by using the markdown file, though I doubt the game will ever be played that way. 
The idea was to separate the game generation from the actual gameplay for a more modular application.

Each game setup was referred to as a Mansion and had the following:

- 10 Clues (in the original, these are physical cards) abstracted out to Assets consisting of:
    - 2 keys, which open locked doors
    - 8 people & items, each required to get a private Hint or find the Money
        - what each person and item did was determined at random each game
- 9 Rooms abstracted out to Spaces which each have:
    - a room name
    - a status of locked or unlocked
    - 2-5 items of Furniture abstracted to Interactions as follows:
        - each Room has only certain furniture allowed, for instance the Bed is always in the Bedroom
        - each item of Furniture could be searched and would yield a Clue card, a Hint (public or private), or the Money
- there are a lot more caveats I won't mention here

Once I was able to generate a randomized Mansion,
I then started on a second Python script that would generate one game 
and then act as a replacement for the original game's
electronic device (with some extra bells and whistles).

The original device took in a Code (two digits for Rooms, three digits for Furniture) and then
gave the user a message based on the Code. 
If the Room was Locked or the Furniture required a Clue to search,
it would ask follow-up questions. 
In the Python Script, this was simply a game loop that kept allowing code inputs until the Money was found.
The follow-up parts were a bit more complicated, as they had to handle a Code plus one or two Answers from the user.
I also added a "virtual deck" that could be switched on or off that would tell the user what Clue cards they got
instead of having to rely on a physical deck.

I added some special help functions (such as a furniture list and a map of the Mansion) and then ran a play test with my brother,
who knew the original game. For our Test we did not use the physical game, we instead drew the gameboard on a blank piece
of paper and noted the furniture items in each room as we went. The game worked except for Code I had mistyped, so I polished
the command-line interface and found some more steps to take to finish it off.

The biggest win I had after reaching Minimum Viable Product was to add text-to-speech with the library pyttsx3.
The original version talked, so this app should too. 
Granted, the original had voice acting and this automated voice was less appealing,
but it still got the same idea across. 
There are private hints in the game that show on screen to one person,
so I made sure those wouldn't be read aloud. 
When playing a game, this feature can be switched on or off (vital since the voice can be annoying).

After getting this to work, and refactoring a lot, I did a few more small expansions:

- when generating a game, you can enter the # of mansions you'd like to generate
- when generating a game, the Mansion gets tested for validity and "invalid" Mansions cause the randomization to re-run
- when generating or playing a game, you can choose different styles:
    - "classic" is the original version
    - "small" uses the original version, but a 4 room mansion instead of a 9 room mansion
    - "sequel" is an experimental version, where I removed some the oddities of the original (such as duplicate furniture) with the aim of eventually having a fully-digital version    
    
It isn't ideal to have the app as a .py file playable through command-line, but it is not at a point where the original version
is as preserved as we need to continue playing the game without the old electronic device. Eventually, it would be nice to 
take this beyond the command-line (perhaps with a Python GUI and an .exe file) and to actually save the Mansions to a database
rather than just markdown files. Better yet, it would be awesome to have this game fully-playable from a browser.
In a perfect world, we would even get new voice acting for the final product.

This was a nice small Python project to complete, and leaves a lot of room for future work.
I may have to find a way to release this to hobbyists who may have a copy
of the game with a broken electronic device.
