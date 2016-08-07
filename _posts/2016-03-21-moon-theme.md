---
layout: post
title:  "Controlling the appliances"
date:   2016-04-06
excerpt: "Using Raspberry Pi, PHP, and Apache Webserver to save electricity."
project: true
---


{% capture images %}
	https://media.giphy.com/media/keCZcgJ8FuPGE/giphy.gif
{% endcapture %}
{% include gallery images=images caption="Finished Product <a href="https://github.com/BrianAllenGit/HandsFreeLightsOff">Github</a> website code repo." cols=1 %}
   
## The Problem
With electricity being costly (and me feeling lazy when I'm watching a good movie), I needed a way to shut off the lights from my couch or while I'm out and about. I needed a way to check if my lights were on as well.

## Assumptions
* The power outlets would need to be able to respond to signals
* A Raspberry Pi can power a transceiver.
* A web server can be used to send signals to the transceiver 


## The Solution
I was able to purchase outlet covers that can accept 433 MHz signals to control the flow of electricity. I wired a 433 MHz transceiver to the Raspberry Pi. I was able to use the open source WiringPi package to send signals to the reciever. 

I created a PHP website on an Apache Webserver. The website displayed buttons that would display the current state of the outlets. Clicking the buttons would send an Ajax call to the Raspberry Pi to toggle the state of the specified outlet. A little dynamic DNS and router magic exposed the website to the world, so that I can control everything on the go.