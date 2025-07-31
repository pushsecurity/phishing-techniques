---
layout: technique
title: Email attachment
description: Embedding malicious links in email attachments
---

# Email attachment

## Summary

Attackers have used malicious links embedded in files for a long time, but it remains an effective way to bypass traditional email-based phishing controls. Recently, we’ve seen attackers move away from traditional PDF attachments to use SVGs and other file formats. 

More sophisticated attacks are using email attachments alongside local webpages to spawn self-contained phishing pages on the client-side. 

## Examples

- [Example 1: Academics identified 44 clusters of “Clickbait” PDFs](https://arxiv.org/pdf/2308.01273) — Attackers are distributing malicious PDFs via SEO and email containing links to phishing websites or drive-by downloads. 
- [Example 2: SVG files used in phishing attacks](https://www.cloudflare.com/en-ca/threat-intelligence/research/report/svgs-the-hackers-canvas/) — SVGs are being increasingly used not just as redirectors to credential harvesting sites, but as self-contained phishing pages (SVGs that contain full phishing pages encoded in Base64, rendering fake login portals entirely client-side), and injecting malicious scripts and changing the DOM to run malicious code and hijack inputs. 
- [Example 3: Embedding malicious links inside a Google Drawings image](https://www.menlosecurity.com/blog/google-drawings-and-whatsapp-zero-hour-open-redirection-phish-exposed) — Attackers embedded a Google Drawings image in an email designed to look like a real Amazon security alert, which linked the user to a phishing page impersonating the Amazon login page. 
- [Example 4: High prevalence of HTML attachments in phishing emails](https://assets.barracuda.com/assets/docs/dms/2025-email-threats-report.pdf) — HTML attachments were the most weaponized text-based file found in emails—23 % of HTML files flagged as malicious, and over 75% of malicious attachments were HTML.
- [Example 5: Loading HTML that decodes into blob URLs](https://www.techradar.com/pro/cybercriminals-have-found-a-sneaky-way-of-stealing-tax-accounts-and-even-encrypted-messages-heres-what-you-need-to-know) — Attackers are linking to what appears to be a legitimate page, often hosted on trusted domains such as Microsoft’s OneDrive, which loads malicious HTML that decodes into a blob URL, loading a phishing page (e.g. imitating the Microsoft login page)
