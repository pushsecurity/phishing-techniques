---
layout: technique
title: Identity provider
description: Targeting cloud identity providers to maximize breach impact
---

# Identity provider

## Summary

Attackers commonly target identity provider (IdP) platforms and accounts. The most commonly targeted examples are Microsoft, Google, AWS, Okta given their widespread use, but less common IdP platforms can be targeted in more tailored attack scenarios if an organization is known to use a specific provider. 

Targeting IdP platforms enables attackers to not only compromise in-ecosystem resources (usually enterprise cloud services and data) but also enables attackers to hijack the SSO process to access downstream apps and services that the compromised user has access to — either because the user has an account on those apps, or the organization has a tenant on the app that allows users with the correct email domain to auto-join on creating an account.

The downside to targeting IdPs is that they usually have the widest range of security configuration and conditional access options, and are more likely to be accessed using phishing-resistant authentication mechanisms. 
