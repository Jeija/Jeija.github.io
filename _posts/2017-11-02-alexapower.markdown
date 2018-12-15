---
layout: single
title:  "ESP32 + Dash Button + Alexa = Power Button"
date:   2017-10-02 18:00:00 +0100
categories: wireless ESP32
---

My home is already very cluttered with tech, so whenever possible, I like to have it get out of my way.
But hiding my desktop computer poses the obvious problem that this makes it very annoying to have to press the power button in an uncomfortable location every time I want to turn on my PC.

So I created `alexa-power-button` which solves this by allowing me to use either voice commands for Amazon's digital assistant "Alexa" or an Amazon Dash Button to start my computer.
It is based on an ESP32 that subscribes to an MQTT channel on AWS IoT enabling it to react to commands from a custom Alexa skill.
Morever, the ESP32 continuously sniffs WiFi traffic while looking for WiFi packets transmitted by a specific Amazon Dash Button.
Whenever it receives an MQTT update or detects a packet from my Dash Button, it turns on the computer.
No more bending over to reach the power button :D

Design files for the ESP32 PCB, firmware and documentation can be found [on GitHub](https://github.com/Jeija/alexa-power-button).
