---
layout: technique
title: Cross-domain iframes
description: Using cross-domain iframes to block injected detections
---

# Cross-domain iframes

## Summary

Phishing kits have been seen loading the core of the page inside a cross-domain iframe. At a glance this extra step doesn’t seem to provide much additional network obfuscation, but one possible reason is to protect against web-proxy based detections that function by injecting JS scripts to run detections once web pages actually load in the browser — a way of getting around the shortcomings of network-based detections. 

Cross-domain iframes are useful in this case because the injected scripts run in unprivileged context (like any other normal script) and therefore are prevented from accessing what happens inside the iframe — where the malicious code lives. Controls that run in the browser in a privileged position (like an extension) are needed to circumvent these protections.

## Examples

- [Example 1: Frame injection attacks](https://securelist.com/phishing-scam-techniques-tricks/108247/) —  The attacker’s phishing kit opens a trusted site in a cross-domain iframe on the rogue page, then overlays a deceptive login form on top. Visually, the page looks identical to the real site (since the user sees genuine content in the background), but any credentials entered into the overlay are captured by the phish. 
- [Example 2: Phishing kits are useing iframes to simulate legitimate pop-up login windows](https://freemindtronic.com/bitb-attacks-how-to-avoid-phishing-by-iframe/#:~:text=match%20at%20L328%20browser%20window,such%20as%20Google%2C%20Facebook%2C%20or) — The phishing page renders what looks like an OAuth or SSO login dialog (for instance, a Microsoft 365 or Google account prompt) as a HTML/CSS overlay. Critically, an invisible cross-domain iframe is embedded within this fake window to load content from another URL (often an attacker-controlled page that mimics the real login)
- [Example 3: EDG phishing kit analysis](https://www.vmray.com/inside-the-latest-phishing-campaigns-dissecting-carphish-edg-tpass-and-mamba2fa-kits/#:~:text=3,script%20mentioned%20in%20point%203) — the EDG phishing kit (detailed by VMRay in late 2024) deliberately keeps its credential-stealing form out of the initial HTML and loads it at runtime via a script. The kit’s landing page includes a placeholder iframe element, and the real phishing UI is pulled from an external source and embedded only after the page loads. This cross-domain loading technique obfuscates the malicious content from static scanners. Only when a user interacts does the iframe fill with the fake login form, which then captures credentials and posts them to the attacker’s server. 
