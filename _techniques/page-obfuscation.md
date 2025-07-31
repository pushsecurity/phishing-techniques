---
layout: technique
title: Page obfuscation
description: Obfuscating and randomizing page elements
---

# Page obfuscation

## Summary

Phishing pages change and even randomize elements of the page to avoid static fingerprints and defeat comparison-based checks against real pages. This includes the page title, text, images, backgrounds, logos, favicons, etc. — all of which may be signatured components using web page analysis tools. These elements can even be embedded in an encoded form so it isn't present in the initial HTML, and is instead dynamically set at runtime when loaded. 

## Examples

- [Example 1: NakedPages AitM kit page title randomization](https://pushsecurity.com/blog/how-aitm-phishing-kits-evade-detection-p2/#id-dom-obfuscation-techniques_id-2-randomizing-page-titles) — Randomizing the HTML page title each time the page loads.
- [Example 2: NakedPages AitM kit dynamic text decoding](https://pushsecurity.com/blog/how-aitm-phishing-kits-evade-detection-p2/#id-dom-obfuscation-techniques_id-2-randomizing-page-titles) — Storing login form text as a Base64 string and decoding it in the browser using JavaScript (e.g. via atob() function) when the page loads.
- [Example 3: Replacing ASCII text values with ASCII and HTML encoding](https://www.akamai.com/blog/security/catch-me-if-you-can-evasive-and-defensive-techniques-in-phishing) — Similarly to example 2, loading page elements dynamically so the values are not visible in the initial HTML.
- [Example 4: Image obfuscation](https://pushsecurity.com/blog/how-aitm-phishing-kits-evade-detection-p2/#id-dom-obfuscation-techniques_id-5-image-element-obfuscation) — Using using styled containers or canvas drawing to render the logo, changing background images, removing/changing favicons, and substituting logos. 
