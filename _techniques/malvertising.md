---
layout: technique
title: Malvertising & SEO poisoning
description: Distributing malicious links via ads on search engines, social media, and other websites.
---

# Malvertising & SEO poisoning

## Summary

Attackers are distributing malicious links using paid ads (aka. malvertising) on search engines like Google and social media platforms, as well as conducting SEO poisoning attacks to index their malicious pages on search engines. 

Malvertising takes advantage of the fact that paid ads can be taken out against specific search terms with minimal checks, creating a watering hole-style attack where users searching for a specific term will be delivered a malicious link at the top of their search feed. 

The attacker designs an ad that looks as similar to a legitimate ad as possible and can often appear above the legitimate ads for relevant products. When combined with techniques like rentable subdomains, this makes for the creation of authentic-looking links without many of the usual indicators of a phishing link (e.g. suspicious domain, unusual characters, or incorrect spelling). 

SEO poisoning is a little more convoluted, but can be achieved using malicious tools like [Hacklink](https://www.netcraft.com/blog/how-fraudsters-are-poisoning-search-results-to-promote-phishing-sites) to purchase access to thousands of compromised websites and inject malicious code designed to manipulate search engine algorithms.

This method of link delivery has a number of advantages over traditional email-based phishing:
- The attacker does not have to acquire and build up the reputation for email accounts in order to deliver the link to victims.  
- Users trained to suspect phishing links delivered via email are often unsuspecting of malicious ads — particularly those ranking at the top of their search results. 

While search engines offering paid search (e.g. Google, Bing, etc.) claim to perform checks on the content being advertised, malicious ads have been observed running for extended periods of time before being taken down. 

The introduction of AI overviews is also changing the experience for users, where ads may appear above, within, or below the AI-generated section at the top of a search — further masking the fraudulent nature of the link.

## Examples

- [Example 1: Onfido malvertising attack](https://pushsecurity.com/blog/investigating-a-recent-malvertising-campaign-targeting-onfido-customers/) — Attackers believed to be Scattered Spider registered malicious ads impersonating Onfido, the digital identity verification platform, leading to an AitM phishing page.  
- [Example 2: Google Ads Users targeted via malvertising](https://www.malwarebytes.com/blog/news/2025/01/microsoft-advertisers-phished-via-malicious-google-ads) — Threat actors bought Google search ads for “Microsoft Ads,” tricking users into clicking a cloaked URL that ultimately redirected to a phishing page for Microsoft’s advertising platform. The fake login page prompted password resets and attempted to capture MFA codes.
- [Example 3: Microsoft advertisers phished via malicious Google ads](https://www.malwarebytes.com/blog/news/2025/01/microsoft-advertisers-phished-via-malicious-google-ads) — Attackers ran ads mimicking Google’s, leading to fake Google Ads sign-in pages hosted on Google Sites. Victims’ credentials and 2FA codes were stolen via WebSocket and used to hijack their ad accounts.
- [Example 4: Fake bank promotion ads on Instagram](https://www.bleepingcomputer.com/news/security/instagram-ads-mimicking-bmo-eq-bank-are-finance-scams/) — Sophisticated scams on Instagram have used sponsored posts to pose as banks. For example, ads mimicking EQ Bank offered an unrealistically high 4.5% yield. Tapping the ad led users to a site that spoofed EQ Bank’s login page to steal credentials.
- [Example 5: Malvertising targeting mobile device users searching for their organizational login page](https://reliaquest.com/blog/threat-spotlight-payroll-fraud-attackers-stealing-paychecks-seo-poisoning/) — This attack is described as SEO poisoning but in fact involves sponsored ads directing victims to a Microsoft phishing page. 
