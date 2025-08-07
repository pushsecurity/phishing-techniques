---
layout: technique
title: Identity provider accounts
description: Targeting cloud identity providers to maximize breach impact
---

# Identity provider accounts

## Summary

Attackers commonly target identity provider (IdP) platforms and accounts. The most commonly targeted examples are Microsoft, Google, AWS, Okta given their widespread use, but less common IdP platforms can be targeted in more tailored attack scenarios if an organization is known to use a specific provider. 

Targeting IdP platforms enables attackers to not only compromise in-ecosystem resources (usually enterprise cloud services and data) but also enables attackers to hijack the SSO process to access downstream apps and services that the compromised user has access to — either because the user has an account on those apps, or the organization has a tenant on the app that allows users with the correct email domain to auto-join on creating an account.

The downside to targeting IdPs is that they usually have the widest range of security configuration and conditional access options, and are more likely to be accessed using phishing-resistant authentication mechanisms. 

## Examples

There are too many examples to list them all, but here are a few [most of which are also examples of Attacker-in-the-Middle kits](https://phishing-techniques.pushsecurity.com/techniques/aitm-phishing/):

- [Example 1: GreatNess PhaaS platform](https://blog.talosintelligence.com/new-phishing-as-a-service-tool-greatness-already-seen-in-the-wild/) — PhaaS platform with AiTM proxy for MFA bypass. Auto-fills victim’s email & org branding on fake M365 login pages. Delivers HTML attachment lures; steals credentials & session cookies
- [Example 2: EvilProxy AitM kit](https://www.proofpoint.com/us/blog/email-and-cloud-threats/cloud-account-takeover-campaign-leveraging-evilproxy-targets-top-level#:~:text=,Middle%20phishing) — Reverse-proxy AiTM toolkit that intercepts MFA-protected logins to steal credentials and session cookies. Used in large-scale campaigns (e.g. 120,000+ phish emails targeting thousands of accounts) against Microsoft, Google, Okta, and others.
- [Example 3: W3LL Ecosystem](https://cyberscoop.com/phishing-w3ll-microsoft-365-fraud/#:~:text=Group,with%20the%20group%E2%80%99s%20phishing%20campaigns) — Modular phishing kit (W3LL Panel) for Office 365 credentials, with MFA token-stealing capability. Includes 16 tailored tools (phish kits, infrastructure, etc.) in a closed marketplace. Over 56,000 O365 accounts targeted.
- [Example 4: Tycoon 2FA](https://www.proofpoint.com/us/blog/email-and-cloud-threats/tycoon-2fa-phishing-kit-mfa-bypass) — Sophisticated AiTM PhaaS emerged Aug 2023. Bypasses MFA by stealing session cookies in real time. Continuously updated with advanced evasion (obfuscation, custom CAPTCHA challenges, anti-debugging). Sold via Telegram; e.g. ~$120 for 10-day access (ready-to-use pages). Targets M365 and GMail accounts.
- [Example 5: Mamba 2FA](https://www.darkreading.com/cyberattacks-data-breaches/mamba-2fa-cybercrime-kit-microsoft-365-users) — AiTM phishing kit (PhaaS) advertised ~$250/month. Presents very convincing fake Microsoft login pages (OneDrive, SharePoint, generic sign-in, even fake voicemail links), with dynamic enterprise branding (logos/background). Steals credentials & OTP codes; instantly exfiltrates session cookies via Telegram bot. Targets Microsoft 365 (Entra ID/Azure AD, AD FS, SSO)
- [Example 6: Sneaky 2FA](https://thehackernews.com/2025/01/new-sneaky-2fa-phishing-kit-targets.html) — AiTM PhaaS kit active since Oct 2024. Bypasses MFA by capturing 2FA codes and session tokens. Notable for novel lures (e.g. emails with PDF attachments containing QR codes that lead to the phishing page). Implements aggressive anti-bot/analysis: Cloudflare Turnstile CAPTCHAs, traffic filtering, dev-tool detection, and diverting non-victims to a benign Wikipedia page (“WikiKit”). Only licensed users can deploy it (central server checks license key; ~$200/month). Targets M365 / Azure AD. 
