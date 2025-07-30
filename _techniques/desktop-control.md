---
layout: technique
title: Desktop control & streaming
description: Using remote desktop control to render a web page loaded in the attacker's browser.
---

# Desktop control & streaming

## Summary

Rather than using traditional phishing infrastructure, attackers are using remote desktop control and streaming software to trick victims into remotely accessing and entering their credential into sites rendered directly in the attacker's browser — a bit like handing your laptop to someone and asking them to log in. This is also known as a Browser-in-the-Middle attack. 

This has a few advantages from a technical perspective as it renders the webpage as a canvas element rather than showing the typical DOM structure of the page. 

It is relatively easy to detect the use of remote desktop software, but given that a number of sites use remote control and streaming tools, filtering malicious use from legitimate can be challenging. 

## Examples

- [Example 1: EvilNoVNC] (https://pushsecurity.com/blog/phishing-2-0-how-phishing-toolkits-are-evolving-with-aitm/) — Also see this [video demo](https://www.youtube.com/watch?v=6W1eN5_KbKY)
- [Example 2: CuddlePhish](https://posts.specterops.io/phishing-with-dynamite-7d33d8fac038)
