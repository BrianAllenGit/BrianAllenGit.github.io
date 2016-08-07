---
layout: post
title:  "Pokemon Server"
date:   2014-05-01
excerpt: "Building a server-client setup to play Pokemon with many players"
project: true
---


{% capture images %}
	https://media.giphy.com/media/8P2Lhj2IAlgaY/giphy.gif
{% endcapture %}
{% include gallery images=images caption="Finished Product" cols=1 %}
  
## The Problem
I wanted to play an older Pokemon game, but with multiple people from my class to see what the outcome would be like. 

## Assumptions
* C / C++ can be used to simulate key strokes
* Threading can be kicked off by incoming TCP requests 


## The Solution
I developd a client-server program where the server would host an emulated version of Pokemon Red. Clients would attempt to join the game through a TCP connection. The server would listen on a particular socket, and respond to TCP requests by starting a thread to accept user input from the client. The game became a great jumbled mess when a large amount of users joined.

## The Code

Website - <a href="https://github.com/BrianAllenGit/Distributed_Pokemon">Github</a>.