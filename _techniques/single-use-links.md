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
