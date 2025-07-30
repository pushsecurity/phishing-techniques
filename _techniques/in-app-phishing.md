---
layout: technique
title: In-app phishing
description: Distributing links inside SaaS apps
---

# In-app phishing

## Summary

It’s possible to conduct phishing and other social engineering attacks using the native features of SaaS apps. While in some cases this will [generate an automated email sent from the app](https://pushsecurity.github.io/phishing-techniques/techniques/email-legitimate-app/) in other cases the victim will simply be notified inside the target app.

Users will typically treat activity within legitimate apps with a much higher level of trust than they would traditional phishing emails and therefore they are more likely to fall victim.

This can be used as both an initial access method, using SaaS apps that allow communication with external users, or as a lateral movement method once a foothold has been established on a legitimate tenant for the target organization.

For example, a malicious document could be shared with a target using a document sharing app in an attempt to gain a foothold elsewhere. A different example involving lateral movement might be a ticketing system where comments and ticket creation functionality could be abused to spread malicious links aimed at harvesting further user credentials.

## Examples

- [Example 1: North Korean-affiliated attacks using GitHub repository collaboration](https://github.blog/security/vulnerability-research/security-alert-social-engineering-campaign-targets-technology-industry-employees/) — GitHub identified a low-volume social engineering campaign targeting the personal accounts of employees of technology firms, using a combination of repository invitations and malicious npm package dependencies.
- [Example 2: Phishing lures embedded within shared documents](https://www.proofpoint.com/uk/blog/cloud-security/community-alert-ongoing-malicious-campaign-impacting-azure-cloud-environments) — Attackers crafted targeted phishing lures in embedded links in shared documents.
