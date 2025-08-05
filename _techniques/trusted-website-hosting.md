---
layout: technique
title: Trusted website hosting
description: Using legitimate websites and hosting providers to host phishing content
---

# Trusted website hosting

## Summary

Attackers are using trusted websites to house their phishing links, as well as using trusted hosting providers (e.g. Azure, Google, AWS, Cloudflare) to host the phishing pages themselves. 

Legitimate services are less likely to be flagged by link analysis tools and effectively cloak the initial URL delivered to the victim to increase the chance of successful delivery of and access to the link. 

This prevents many link-based analysis techniques from flagging the malicious page. It also provides the link a level of authenticity that may increase the likelihood of a victim falling for the lure.

## Examples

- Example 1: Abusing highly trusted sources like Google by: [abusing script.google.com to host phishing pages](https://www.bleepingcomputer.com/news/security/threat-actors-abuse-google-apps-script-in-evasive-phishing-attacks/); [creating Google Forms to host phishing links](https://cybersecuritynews.com/google-forms-weaponized/); [abusing sites.google.com to host phishing pages](https://x.com/nicksdjohnson/status/1912439023982834120); and [abusing Google AMP](https://cofense.com/blog/google-amp-the-newest-of-evasive-phishing-tactic/)
- [Example 2: Using Cloudflare developer domains to host phishing sites](https://pushsecurity.com/blog/how-aitm-phishing-kits-evade-detection/#id-step-1-cloudflare-workers-for-the-initial-gateway) — Cloudflare’s pages.dev and workers.dev domains are increasingly used by attackers for phishing domains. Cloudflare Workers are a serverless execution environment (a bit like AWS Lambdas) to prevent checks based on uncategorized/rare domains.
- [Example 3: Azure Front Door used to host AiTM sites](https://www.aitm-feed.com/blog/azure-front-door-aitm-phishing) — Azure FD used to host AiTM phishing pages, using multiple redirect stages e.g. page1.azurefd.net to page2.azurefd.net, etc.), targeting the World Food Programme, UNICEF, major news outlets, and even U.S. government email accounts.
- [Example 4: Multiple cloud storage phishing links used to obfuscate malicious sites used in phishing campaigns](https://radicl.com/radicl-blog/cloudy-with-a-chance-of-cc-theft) — Methods include distributing a HTML file hosted on a Linode Object Storage URL.

## Further reading
— [Useful resource of sites that allow attackers to “live off trusted sites”](https://lots-project.com/)
