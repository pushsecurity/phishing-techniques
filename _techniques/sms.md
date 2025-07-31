---
layout: technique
title: SMS
description: Distributing malicious links via SMS
---

# SMS

## Summary

Attackers exploit text messages to send phishing links or social engineer victims (aka. "smishing"), taking advantage of the typically lower security protection available on mobile devices and browsers, and the use of both managed and BYOD personal devices for work purposes. 

In this scenario, links are delivered via SMS leading to a phishing page in order to capture credentials or other sensitive information (e.g. bank details, complete a fraudulent payment, etc.), or leading to the download of a malicious application. 

## Examples

- [Example 1: Twilio employee smishing](https://techcrunch.com/2022/08/08/twilio-breach-customer-data/) —  Communications firm Twilio was breached after employees fell for SMS messages posing as IT support. The texts, sent in early August 2022, told staff their passwords had expired or schedules changed, and urged them to log in via a provided link. The link went to a spoofed Okta SSO page under the attackers’ (Scattered Spider) control. 
- [Example 2: Royal Mail payment info text scam](https://www.malwarebytes.com/blog/news/2021/03/the-human-impact-of-a-royal-mail-phishing-scam) — In the UK, scammers mass-texted people claiming a package was awaiting delivery with a small fee due (e.g. “Your package has a £2.99 shipping fee, pay now: [phishing URL]”). Payment information was captured and used to steal funds from the target bank account. 
