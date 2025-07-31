---
layout: technique
title: Legitimate OIDC logins
description: Using legitimate OIDC logins to block automated analysis and require user interaction
---

# OIDC logins

## Summary

Attackers are placing their phishing pages behind legitimate OIDC (social) logins by registering OAuth apps on legitimate app stores (e.g. Google and Microsoft) with basic scopes. To access the phishing page, the user has to:

- Authenticate to the service normally
- Accept the OAuth permissions request for basic scopes (equivalent to authorizing a social login)

At this point the user is served the phishing page and their login will be captured if the process is completed. 

Unlike traditional consent phishing, this attack is not designed to capture high-value permissions, but is simply designed to require user interaction to load the phishing page — thereby breaking any automated sandbox-type analysis of the page. 


## Examples

- [Example 1: Using OIDC logins to fake OAuth apps](https://pushsecurity.com/blog/how-consent-phishing-is-evolving/#id-2-not-really-consent-phishing) — Using fake Microsoft OAuth apps impersonating Adobe Drive, Adobe Acrobat, and DocuSign.
