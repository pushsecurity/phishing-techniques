---
layout: technique
title: Consent phishing
description: Using consent phishing to abuse OAuth consent grants
---

# Consent phishing

## Summary

One way of compromising an account without going through the standard phishing flow of stealing credentials and/or session tokens is to trick the victim into performing a malicious OAuth consent grant. 

This removes the need to phish the user's credentials and grants the attacker a level of access and control over the target account depending on the scopes authorized, while also bypassing mitigating controls such as MFA and conditional access. 

## Examples

- [Example 1: Consent phishing GitHub accounts](https://pushsecurity.com/blog/how-consent-phishing-is-evolving/#id-1-classic-consent-phishing) — Authorizing an attacker controlled app with risky scopes, granting full access to the user’s account and repositories. 
- [Example 2: Microsoft consent phishing campaign](https://thehackernews.com/2023/02/hackers-abused-microsofts-verified.html) — Attackers abused the OAuth app consent mechanism to gain persistent access to cloud email accounts. Threat actors registered fake applications with names like “Single Sign-On (SSO)” and “Meeting,” and even obtained Microsoft’s “Verified Publisher” badge by using fraudulent partner accounts.
- [Example 3: Google consent phishing attacks](https://www.valencesecurity.com/resources/blogs/the-rising-threat-of-consent-phishing-how-oauth-abuse-bypasses-mfa) — Security researchers identified consent phishing attacks requesting extensive access to Google Workspace data. Once approved, the attacker (as the app developer) can retrieve an access token and refresh token for the victim’s account, granting long-term access to emails, Drive files, contacts, etc.

## Further reading

- [Understanding OAuth scopes in third-party integrations](https://pushsecurity.com/blog/the-risky-terrain-of-oauth-scopes-in-third-party/)
