---
layout: technique
title: Bot protection
description: Using legitimate bot protection tools to prevent automated analysis
---

# Bot protection

## Summary

Attackers are using common bot protection technologies like CAPTCHA and Cloudflare Turnstile to prevent security bots from accessing their web pages to be able to analyse them (and therefore block pages from being automatically flagged). 

This requires anyone visiting the page to pass a bot check/challenge before the page can be loaded, meaning the full page cannot be analysed by automated tools without human interaction. 

## Examples

- [Example 1: NakedPages AitM phishing kit](https://pushsecurity.com/blog/how-aitm-phishing-kits-evade-detection/#id-step-2-cloudflare-turnstile-for-bot-detection) — Using Cloudflare Turnstile for bot protection.
- [Example 2: Tycoon 2FA AitM phishing kit](https://www.trustwave.com/en-us/resources/blogs/spiderlabs-blog/tycoon2fa-new-evasion-technique-for-2025/) — Using a custom CAPTCHA rendered via HTML5 canvas.
