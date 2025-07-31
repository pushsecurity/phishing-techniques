---
layout: technique
title: SaaS admins
description: Targeting SaaS admin users
---

# SaaS admins

## Summary

SaaS apps often have local administrator accounts based on the users that adopt and use a given application within an organization. 

Because apps are often self-adopted by individual users or teams, it’s not uncommon for a standard user in the organization belonging to a specific team to administer apps relevant to that team (e.g. finance users often manage finance apps, marketing users manage marketing apps, and so on) — particularly when considering that many apps don’t have fine-grained permissions (you’re either a user or an admin). 

Because these users are often non-technical, non-security personnel, these users are often an easier target from typical sysadmins, cloud admins, and other enterprise admin accounts within the organization’s primary enterprise cloud tenant(s). 

App-level admins present a high-value target for attackers because they typically have the levels of permission required to:
- Access, download, and send data from the company database, across users
- Configure stealthy persistence mechanisms like API keys to backdoor the app/account
- Set up malicious integrations to increase the blast radius of a compromise
- Amend high-risk settings like adjusting the SAML configuration to be used in watering hole-style SAMLjacking attacks to compromise additional users’ SSO credentials

Admin level accounts on SaaS apps are also less likely to have secure authentication methods enabled compared to a typical enterprise cloud admin.

## Examples

- [Example 1: SAMLjacking using Nuclino](https://pushsecurity.com/blog/samljacking-a-poisoned-tenant/)
- [Example 2: Targeting Mailchimp to export mailing list data](https://pushsecurity.com/blog/dissecting-a-recent-mailchimp-phishing-attack/)
