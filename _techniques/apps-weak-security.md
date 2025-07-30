---
layout: technique
title: Apps with Weak Security Configs
description: Targeting applications with weak security configuration options
---

# Apps with Weak Security Configs

## Summary

Applications support different account configurations that make them more or less susceptible to phishing attacks. IdP accounts and enterprise cloud platforms typically support the widest range of secure configuration options, including things like:

- Enforcing logins with phishing-resistant authentication
- Mandatory phishing-resistant MFA enforcement
- Disabling backup login and MFA methods

However, many SaaS services don’t provide direct support for phishing-resistant login methods like passkeys, or allow SAML SSO (or require an upgraded subscription to enable). Similarly, most apps do not support native conditional access (CA) which is used to restrict the source of a login (e.g. domain-joined and compliant device, approved geolocation and device IP) and login method (e.g. must use only phishing-resistant MFA).

Coupled with limited account configuration visibility for admins, this makes it difficult for organizations to securely configure wider SaaS app usage compared to core, centrally managed enterprise cloud platforms. 

To increase the success rate of their phishing attacks, attackers have been observed switching targets to apps with a lower security ceiling, but still offering significant return on investment in terms of data theft and lateral movement opportunities.

## Examples

- [Example 1: Further reading on app-level security configuration limitations](https://pushsecurity.com/blog/minimum-viable-identity-security/)
- [Example 2: Phishing attack targeting Mailchimp](https://pushsecurity.com/blog/dissecting-a-recent-mailchimp-phishing-attack/)
- [Example 3: Phishing attack targeting Onfido](https://pushsecurity.com/blog/investigating-a-recent-malvertising-campaign-targeting-onfido-customers/)
- [Example 4: Impact of SaaS attacks — Snowflake] (https://pushsecurity.com/blog/snowflake-retro/)
- [Example 5: Impact of SaaS attacks — Jira] (https://pushsecurity.com/blog/why-attackers-are-targeting-jira-with-stolen-credentials/)
- [Example 6: Impact of SaaS attacks — ServiceNow] (https://pushsecurity.com/blog/learning-from-the-servicenow-disclosure/)
