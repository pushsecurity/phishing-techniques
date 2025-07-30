---
layout: technique
title: Mass domain registration
description: Ensuring a steady supply of phishing domains
---

# Mass domain registration

## Summary

Attackers are taking over domains on an industrial scale to enable them to be easily rotated out when burned and added to blocklists. Attackers expect their phishing domains to last for a limited time before they are burned in some capacity — having a steady supply of domains ensures their campaigns can continue. 

This can be achieved by:
- Registering new domains in huge quantities ahead of time.
- Compromising existing domains through website vulnerabilities.
- Re-registering expired domains previously belonging to legitimate companies and services.

## Examples

- [Example 1: Revolver Rabbit Gang registers 500k domains for phishing](https://www.bleepingcomputer.com/news/security/revolver-rabbit-gang-registers-500-000-domains-for-malware-campaigns/)
- [Example 2: Attackers hijacked legitimate domain owners’ DNS to silently place hundreds of subdomains beneath trusted domains](https://unit42.paloaltonetworks.com/domain-shadowing/) — Attackers used a technique the researchers call "domain shadowing", registering hundreds of subdomains under a compromised domain.
- [Example 3: AiTM phishing infrastructure hosted on a lapsed domain](https://sublime.security/blog/aitm-phishing-with-russian-infrastructure-and-detection-evasion-from-a-lapsed-domain/) — Russian infrastructure hosted on an expired domain that was acquired by the attacker.
- [Example 4: Phishing-as-a-Service kit using 300k automatically generated subdomains](https://www.microsoft.com/en-us/security/blog/2021/09/21/catching-the-big-fish-analyzing-a-large-scale-phishing-as-a-service-operation/) — Phishing-as-a-Service operation BulletProof provides a vast number of domains that can be assigned to the operator's phishing site.
