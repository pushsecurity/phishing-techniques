---
layout: technique
title: Single-use links
description: Using links that can only be used once, blocking post-hoc analysis
---

# Single-use links

## Summary

Attackers can generate unique phishing URLs for each target (or each email) that expire after a single use. Once clicked (especially by the intended victim), the link will not show the phishing page again. This frustrates security teams and automated scanners — if a scanner or proxy triggers the link first, the real content disappears when a human checks, and vice versa. It also prevents multiple victims from using the same URL, making detection and takedown harder.

## Examples

- [Example 1: BulletProofLink PhaaS single-use links](https://www.exploitone.com/tutorials/how-bulletprooflink-anthrax-works-famous-deep-web-phishing-as-a-service-phaas-tool/#:~:text=Support%20and%20hosting) - For about $50, a scammer could get phishing hosting where each link works one time only.
- 
— Example 2: Dynamic IP locking — Using a “one IP, one chance” rule. The first visit from a given IP will get the phishing page; any subsequent visits from the same IP get a fake 404 or redirect. This means if a security analyst tries to revisit a URL from their machine (same IP), it won’t show the phish again.
- [Example 3: Evilginx lure URLs in Scattered Spider campaigns] (https://pushsecurity.com/blog/scattered-spider-ttp-evolution-in-2025/#id-scattered-spider-ttp-evolution-in-2025_id-using-commercial-aitm-toolkits-like-evilginx-to-bypass-mfa-and-evade-detection) — Evilginx requires that specific lure URLs are accessed to load the phishing page. Attempting to load the domain natively will redirect you (typically by "Rick Roll") or blocking your IP address permanently.
