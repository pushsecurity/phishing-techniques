---
layout: technique
title: Credential theft
description: Steal credentials to compromise accounts without MFA
---

# Credential theft

## Summary

Capturing stolen credentials is a useful outcome of modern phishing attacks, even in the era of widespread MFA usage. 
Stolen credentials can be used to:

- Spray across business apps to take advantage of password reuse and the absence of MFA on apps without MFA enforcement aka. [credential stuffing](https://github.com/pushsecurity/saas-attacks/blob/main/techniques/credential_stuffing/description.md).
- Use alongside SIM swapping and [MFA fatigue](https://github.com/pushsecurity/saas-attacks/blob/main/techniques/mfa_fatigue/description.md) attacks to bypass MFA for accounts without phishing-resistant MFA enrolled. 

## Examples

- [Example 1: Using stolen credentials to compromise hundreds of Snowflake tenants without MFA](https://pushsecurity.com/blog/snowflake-retro/)
- [Example 2: Using stolen credentials to compromise Jira tenants across multiple businesses](https://pushsecurity.com/blog/why-attackers-are-targeting-jira-with-stolen-credentials/)
