---
layout: technique
title: Email from legitimate app/service
description: Sending automated emails from legitimate apps and services
---

# Email from legitimate app/service

## Summary

Attackers are using legitimate, trusted third-party applications to send phishing lures as part of multi-step attacks requiring user interaction across different sites/mediums. 

+ Attacker sends a message on a third-party platform including a link. This can be to a phishing page, or may direct the user to another site/document before delivering the phishing link. 
+ The in-app message generates an email notification to view the message.
+ Attacker clicks the link and is taken to the legitimate site to view the message (and from there access the phishing page).

This approach is effective because:
- It prevents an email-based solution from intercepting and analysing the phishing link or page.
- It takes advantage of the message being sent from a trusted application to increase legitimacy.

## Examples

- [Example 1: Abusing Google products to send emails] Sending emails from [Google Forms](https://cybersecuritynews.com/google-forms-weaponized/), Using [sites.google.com](https://x.com/nicksdjohnson/status/1912439023982834120) to host a phishing page, luring the victim with an automated email posing as a "Security Alert" sent from Google.
- [Example 2: Abusing DocuSign API to send Paypal phishing emails](https://www.malwarebytes.com/blog/news/2025/03/paypal-scam-abuses-docusign-api-to-spread-phishy-emails) — Cybercriminals set up DocuSign accounts and used DocuSign’s API/templates to send fake PayPal invoices. Because the emails came from DocuSign’s domain, they bypassed filters. 
- [Example 3: Fake security alert on GitHub](https://www.bleepingcomputer.com/news/security/fake-security-alert-issues-on-github-use-oauth-app-to-hijack-accounts/) A widespread phishing campaign targeted nearly 12,000 GitHub repositories with fake "Security Alert" issues, tricking developers into authorizing a malicious OAuth app that grants attackers full control over their accounts and code.
- [Example 4: Malicious use of DropBox in phishing attacks](https://www.darktrace.com/blog/legitimate-services-malicious-intentions-getting-the-drop-on-phishing-attacks-abusing-dropbox) A phishing campaign leveraged Dropbox’s legitimate email infrastructure. Employees received an email from no-reply@dropbox.com with a link to a PDF hosted on Dropbox. The PDF contained a phishing URL. Scanning the QR code or clicking the link led to credential theft pages.
