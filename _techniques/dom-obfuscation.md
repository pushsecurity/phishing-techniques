---
layout: technique
title: DOM obfuscation
description: Changing the DOM structure to evade cloned page detections
---

# DOM obfuscation

## Summary

Security tools that can inspect a webpage will analyse the DOM for malicious indicators. One of the most common checks is to assess whether the webpage is a clone of a genuine page — both visually and in terms of the underlying code. 

Attackers are getting around this by changing the DOM structure so that the phishing page isn’t obviously cloned from the genuine page that it’s impersonating (e.g. login.microsoft.com).   

It’s possible to construct a completely different DOM that ensures the same visual output with a very different underlying code. It’s also possible to use dynamic modification techniques to ensure the DOM changes during execution, to frustrate fixed point-in-time analysis controls (like those that may be used by web proxies). 

Rather than loading a complicated HTML page, then loading JS components to make the page reactive, these kits often use a very simple “loader” HTML page. This HTML might not even contain a <html> or <head> and <body> tags, but a single script tag that loads obfuscated JS, which in turn replaces the page’s DOM and then proceeds to build the page dynamically.

## Examples

- [Example 1: NakedPages AitM kit DOM structure change example](https://pushsecurity.com/blog/how-aitm-phishing-kits-evade-detection-p2/#id-dom-obfuscation-techniques) — Example of a phishing page delivering a visually authentic clone of a Microsoft page while using a radically different DOM structure.

## Further reading

- [How phishing kits evade detection](https://pushsecurity.com/resources/on-demand-webinar-phish-kit-teardown)
