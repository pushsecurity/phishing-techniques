---
layout: technique
title: Visual obfuscation
description: Using visual obfuscation to defeat computer vision detections
---

# Visual obfuscation

## Summary

Sandbox analysis tools often screenshot the browser window and run the rendered page through a computer vision model to compare to known, legitimate login pages. 

Subtle changes to the page can often defeat these kinds of detection, such asapplying an overlay blur, or a subtle color shift that is not noticeable by a human, but enough to throw off an automated comparison.

To get around this, attackers are dynamically generating visual elements on the page using phishing kits with a customizable frontend. This means they can modify the layout, backgrounds, logos, and colors almost infinitely so as not to trigger detections based on real page matching. 

## Examples

- [Example 1: NakedPages AitM kit page title randomization](https://pushsecurity.com/blog/how-aitm-phishing-kits-evade-detection-p2/#id-dom-obfuscation-techniques_id-2-randomizing-page-titles) — Randomizing the HTML page title each time the page loads.
- [Example 2: NakedPages AitM kit dynamic text decoding](https://pushsecurity.com/blog/how-aitm-phishing-kits-evade-detection-p2/#id-dom-obfuscation-techniques_id-2-randomizing-page-titles) — Storing login form text as a Base64 string and decoding it in the browser using JavaScript (e.g. via atob() function) when the page loads.
- [Example 3: Image obfuscation](https://pushsecurity.com/blog/how-aitm-phishing-kits-evade-detection-p2/#id-dom-obfuscation-techniques_id-5-image-element-obfuscation) — Using using styled containers or canvas drawing to render the logo, changing background images, removing/changing favicons, and substituting logos. 
