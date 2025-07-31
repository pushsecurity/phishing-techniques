---
layout: technique
title: Delayed execution
description: Implementing delays to prevent automated scanning tools from detecting malicious content
---

# Delayed execution

## Summary

Phishing sites often employ time delays or multi-step loading so that automated analysis tools (which only scan a page for a fixed, limited time period) don’t catch the malicious content. 

The phishing payload (like a login form or malicious script) is only revealed after a period of time, user interaction, or through a chain of redirects — by which point an automated scanner may have timed out. This buys the phishing site more time to remain undetected and is an effective way of combating automated analysis.

## Examples

- [Example 1: Delaying malicious content through multiple redirects](https://socradar.io/the-blogspot-based-phishing-attacks/#:~:text=based%20on%20the%20user%E2%80%99s%20location%2C,redirects%2C%20attackers%20can%20evade%20detection) - Phishing campaigns on platforms like Blogspot have used chains of HTTP 302 redirects to “delay” the final malicious page. The user might go through several innocuous-looking URLs before landing on the phish. This tricks security crawlers that often only check the first page.
- [Example 2: Requiring user interaction before serving malicious content](https://medium.com/@balasubramanya.c/unmasking-the-shadows-a-deep-dive-into-anti-cloaking-techniques-for-phishing-prevention-7267b7751366) — Some phishing kits hide the credential input form until they detect real user interaction. For example, a kit may not render the password field or submit button until the user moves the mouse or clicks the page. This fools headless browsers or sandboxes that don’t mimic user behavior by keeping the login form hidden until a user click event occurs. 
— [Example 3: Auto-redirecting after a delay](https://www.catonetworks.com/blog/evasive-phishing-kits-exposed-cato-networks-in-depth-analysis-and-real-time-defense/) — Some phishing campaigns first show an innocuous page or error, then auto-redirect to the phish after a delay. One example shows a phish that landed on a fake “Error 403 – Access Denied” page with a support link; after a short delay or on clicking the link, it moved to the real phishing login.
