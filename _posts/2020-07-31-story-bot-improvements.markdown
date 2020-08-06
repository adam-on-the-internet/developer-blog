---
layout: post
title: "Story Bot Update: Improvements"
date: 2020-07-31
categories: bot
---

I enhanced my Twitter bot [Stories from Another Universe][stories-universe] yet again. I've slowly been adding
content (stories to alter and words to use) but this may be the final update to the functionality.

First, I refactored the existing Story Bot code to use async/await instead of explicit promises. I'm not sure which I
prefer, but wanted to try the async/await path with something, and this small project seemed like a good candidate.

After the refactoring (along with some cleanup) I built two more endpoints for the Story Bot. Both use Datamuse API's
endpoints to find word replacements (http://api.datamuse.com/). The first finds rhymes to replace words
(ex. Gone with the Wind -> Gone with the Sinned). The second grabs a bunch of potential word replacements 
(synonyms, antonyms, and more) for even more variation (ex. Gone with the Wind -> Gone with the Breeze).

The bot now tweets out a message every hour, alternating between four endpoints. Previously, I had a POST and GET
version of each endpoint. The POST would tweet and the GET wouldn't. I switched to using only GET requests and added
a query parameter for requests that should tweet, removing some code duplication. Hopefully this bot is in good 
shape for a while!

[stories-universe]: https://twitter.com/StoriesUniverse
