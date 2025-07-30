---
layout: technique
title: Domain rotation, redirection, and load balancing
description: Preventing initial seeded links and phishing sites from being discovered
---

# Domain rotation, redirection, and load balancing

## Summary

To maximise the lifespan of a malicious domain, attackers use domain rotation, redirection, and load balancing to deliver different domains to recipients using a single URL. This is achieved by:

- Redirecting through trusted sites or sites that are typically excluded from URL blocklists or scanning tools
- Using several redirections before serving the malicious page to break referrer-based checks that are common in proxy solutions and prevent the initial URLs seeded out from being discovered
- Using load balancing to serve different phishing domains to victims, continually refreshing the pool of phishing URLs

By obfuscating the initial URL delivered to victims, and both masking and rotating the phishing URLs, it is much harder for organizations to blocklist known-bad sites effectively. 

## Examples

- [Example 1: NakedPages load balancing](https://pushsecurity.com/blog/how-aitm-phishing-kits-evade-detection/#id-step-7-loading-balanced-domains) — The NakedPages AitM kit retrieves a new URL along with a suitable JWT authentication parameter. Automating the request brought back around 20 different primary domains used for the final phishing attack. These domains are rotated over time as some are blocked and new ones are created.
- [Example 2: Using server-side redirects](https://unit42.paloaltonetworks.com/rare-phishing-page-delivery-header-refresh/) — Researchers observed large-scale phishing campaigns using a refresh entry in the HTTP response header, which directs the browser to automatically refresh or reload a page without requiring user interaction, loading one of several randomized phishing domains.
- [Example 3: AitM phishing infrastructure using several redirects](https://www.aitm-feed.com/blog/azure-front-door-aitm-phishing) — Researchers identified phishing infrastructure using several rounds of redirects through legitimate domains (including security providers) and various Azure FD hosted domains before serving up the malicious page.
