---
layout: technique
title: Device code phishing
description: Abusing device login flows to bypass MFA
---

# Device code phishing

## Summary

To get around phishing-resistant authentication methods, attackers are using device code phishing attacks that take advantage of alternative authentication flows for devices which do not support passkey-based logins, e.g. because they don’t have web browsers, or have limited input capabilities. 

This typically involves phishing a one-time access code from the victim alongside, or instead of, a password-based login, substituting the typical MFA process. 

## Examples

- [Example 1: Device code phishing with Microsoft](https://github.com/pushsecurity/saas-attacks/blob/main/techniques/device_code_phishing/examples/microsoft.md) — Example of spoofing the OneDrive iOS app. 
- [Example 2: Simulating device code phishing in a headless browser](https://denniskniep.github.io/posts/09-device-code-phishing/) — Automating the process of redirecting the victim to the authentication page, directly entering the generate Device Code into the webpage behind the scenes.
- [Example 3: Russian threat actors targeting Microsoft device code authentication](https://www.volexity.com/blog/2025/02/13/multiple-russian-threat-actors-targeting-microsoft-device-code-authentication/)
- [Example 4: Microsoft Threat Intelligence centre tracks Storm-2372 using techniques that abuse device authentication flow](https://www.bleepingcomputer.com/news/security/microsoft-hackers-steal-emails-in-device-code-phishing-attacks/)
- [Example 5: GitHub device code phishing](https://www.praetorian.com/blog/introducing-github-device-code-phishing/)
- [Example 6: Device code phishing in Google Cloud and Azure](https://www.huntress.com/blog/oh-auth-2-0-device-code-phishing-in-google-cloud-and-azure)
- [Example 7: Detecting device code phishing](https://aadinternals.com/post/phishing/)
- [Example 8: OAuth device code phishing with verified apps](https://github.com/secureworks/PhishInSuits)
