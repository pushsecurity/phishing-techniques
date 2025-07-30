---
layout: technique
title: Local webpage
description: Local webpage
---

# Local webpage

## Summary

Attackers are spawning local, client-side phishing pages to stealthily capture credentials. This is most commonly performed using HTML Applications (HTAs), which are Microsoft Windows programs using HTML, CSS, and scripting languages (like JScript or VBScript). These files are saved with an ".hta" extension and execute like standalone desktop applications, rather than within a web browser's security sandbox.

In the context of identity-driven phishing, most email security threats look for known security threats (e.g. URLs pointing to malicious websites), and since HTAs are essentialy just HTML and script files packaged together, they often don't trigger standard filters. And because the phishing content isn't hosted online, it can't be scanned or blocked ahead of time by page analysis or automated scanning tools. 

## Examples

- [Example 1: High prevalence of HTML attachments](https://assets.barracuda.com/assets/docs/dms/2025-email-threats-report.pdf) — HTML attachments were the most weaponized text-based file found in emails—23 % of HTML files flagged as malicious, and over 75% of malicious attachments were HTML.
- [Example 2: Loading HTML that decodes into blob URLs](https://www.techradar.com/pro/cybercriminals-have-found-a-sneaky-way-of-stealing-tax-accounts-and-even-encrypted-messages-heres-what-you-need-to-know) — Example of HTML that decodes into blob URLs, linking to what appears to be a legitimate page, often hosted on trusted domains such as Microsoft’s OneDrive.
- [Example 3: Using SVGs as an alternative to HTAs](https://www.cloudflare.com/en-ca/threat-intelligence/research/report/svgs-the-hackers-canvas/) — SVGs are being increasingly used not just as redirectors to credential harvesting sites, but as self-contained phishing pages (SVGs that contain full phishing pages encoded in Base64, rendering fake login portals entirely client-side). 
