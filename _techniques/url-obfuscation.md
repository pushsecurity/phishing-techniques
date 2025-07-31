---
layout: technique
title: URL obfuscation
description: Using URL obfuscation techniques to prevent detection
---

# URL obfuscation

## Summary

Attackers use various URL obfuscation techniques to prevent URL-based detections from firing when a link is analysed. 

This is typically used alongside [trusted website hosting](https://pushsecurity.github.io/phishing-techniques/techniques/trusted-website-hosting/) and [domain rotation, redirection, and load balancing](https://pushsecurity.github.io/phishing-techniques/techniques/domain-rotation-redirection/) to bypass URL and domain-based checks and serve up a malicious domain to the user.

The most common methods used are:

- Using [unauthorized URL redirects](https://www.trustwave.com/en-us/resources/blogs/spiderlabs-blog/trusted-domain-hidden-danger-deceptive-url-redirections-in-email-phishing-attacks/) from websites allowing open redirects
- Using URL shorteners (in particular custom or uncommon shorteners that are less likely to be blocked by email providers)
- Using obfuscated URL destinations [such as through URL schema obfuscation](https://pushsecurity.com/blog/detecting-phishing-pages-using-obfuscated-url-destinations/)

## Examples

- [Example 1: Unauthorized URL redirects](https://www.trustwave.com/en-us/resources/blogs/spiderlabs-blog/trusted-domain-hidden-danger-deceptive-url-redirections-in-email-phishing-attacks/)
- [Example 2: Using WhatsApp shortened URLs](https://www.menlosecurity.com/blog/google-drawings-and-whatsapp-zero-hour-open-redirection-phish-exposed)
- [Example 3: Using custom URL shorteners](https://alluresecurity.com/link-shortner-services-for-credential-harvesting/)
- [Example 3: URL schema obfuscation](https://cloud.google.com/blog/topics/threat-intelligence/url-obfuscation-schema-abuse/) — Using URL schema obfuscation and encoding to mask phishing URLs by abusing the way that browsers handle addresses including the @ symbol.
