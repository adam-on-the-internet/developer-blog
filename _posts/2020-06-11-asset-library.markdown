---
layout: post
title: "Asset Library"
date: 2020-06-11
categories: general
---

Today I created a simple [Asset Library][asset-library] site. 

I have several apps which use images in creative ways, and it made technical sense to have one spot
to save these statically. I had tried in the past to store images in a database but found
that there wasn't an easy way to manage that, on top of the performance issues with 
images being retrieved from databases. 

The straw that broke the camel's back was my experimenting with
the Twine game engine. Twine games are simple html projects that rely on external images. This site 
provides a place for me to expose any images I want to use in Twine games. 

I wanted to keep things as barebones as possible, so this site is just one html file that is populated
by a short bit of JavaScript. That JavaScript reads a local JSON file that catalogs the images stored
within the application. 

In the future, I will want to find non-static ways to manage images. For now, this is more than enough.

[asset-library]: https://adam-on-the-internet.github.io/asset-library/