---
layout: technique
title: Abuse mobile user agent exceptions
description: Abusing mobile user agents to bypass conditional access restrictions
---

# Abuse mobile user agent exceptions

## Summary

Attackers can take advantage of conditional access (CA) policy exceptions for mobile user agents to bypass MFA and CA checks.

## Examples

- [Example 1: Using a legacy mobile client to evade MFA](https://www.kroll.com/en/publications/cyber/securing-microsoft-365-avoiding-multi-factor-authentication-bypass-vulnerabilities) — Attackers leveraged email protocols and mobile user-agent strings to bypass conditional access policies on Microsoft 365 tenants by identifying an Outlook on iOS/Android client that uses basic authentication. Because legacy mobile clients were exempt from modern auth in that organization, the attacker was able to sign in with just the password (no MFA). 
- [Example 2: Spoofing device platform in conditional access](https://www.mantra.ms/blog/how-hackers-bypass-microsoft-azure-ad-conditional-access) — Many conditional access policies determine access based on device platform (e.g. only allow mobile iOS/Android apps for certain resources). Attackers have exploited this by spoofing the user-agent in their browser or tool to appear as an allowed device. Since Azure AD policy relies on the client’s user-agent string to identify OS, a hacker can edit their agent string to mimic a mobile device and meet the policy criteria. 
