---
layout: technique
title: QR codes
description: Hiding malicious links in QR codes
---

# AI/LLM poisoning

## Summary

Attackers can embed malicious QR codes in emails, websites, or physical media to trick users into scanning them with their phones to load a malicious page or execute a file/app download. 

Many standard email security tools struggle to detect malicious QR codes hidden within emails. This is because these tools typically scan for malicious links within the email body or attachments, not images for embedded URLs within QR codes. 

The novelty of QR codes as a phishing vector also contributes to their effectiveness, as many users are not yet accustomed to treating them with the same level of suspicion as traditional phishing links.

## Examples

- [Example 1: Parking meter QR code scam](https://www.westsidespirit.com/news/nyc-dot-issues-warnings-of-fraudulent-qr-code-amid-parking-scam-CJ4685271) —  Fraudsters have been placing fake QR code stickers on parking meters in multiple cities (Austin, NYC, etc.). In New York, the DOT warned drivers after discovering bogus QR decals on meters that, when scanned, led to a phoney parking payment site. 
- [Example 2: QR codes in phishing emails](https://cofense.com/blog/major-energy-company-targeted-in-large-qr-code-campaign/) — Email-based “quishing” surged by over 2400% since May 2023 according to Cofense. Attackers embed a QR image (often in a PDF or PNG attachment) instead of a clickable URL. For example, one widespread campaign spoofed Microsoft, emailing users a “secure your account” notice with a QR code. Scanning it on a phone brought up a fake Office 365 login page to steal credentials.
