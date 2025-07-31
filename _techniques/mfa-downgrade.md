---
layout: technique
title: MFA downgrade
description: Downgrading authentication so it can be phished
---

# MFA downgrade

## Summary

To get around phishing-resistant authentication methods, attackers are using downgrade attacks that force the login to use an alternative, phishable method enabled for the account.

Often referred to as a “passkey”, passwordless authentication typically consists of a hardware security device that is built-into your laptop (e.g. the fingerprint sensor on a laptop) or something you plug into your device (e.g. a Yubikey). Because passkey-based logins are domain-bound, trying to use a passkey for microsoft.com on phishing.com simply won’t generate the correct value to pass the authentication check, even when proxied using an AitM kit.

However, attackers have realized that even as these new phishing-resistant methods are starting to become used, most users still have alternative MFA methods active. The attacker can then do a downgrade attack to force the account to use a less secure login method registered to the account.

## Examples

- [Example 1: Examples of Evilginx and Tycoon 2FA supporting MFA downgrade functionality](https://pushsecurity.com/blog/mfa-downgrade-attacks/)
- Example 2: Phishing Windows Hello for Business using a downgrade attack [Article](https://medium.com/@yudasm/bypassing-windows-hello-for-business-for-phishing-181f2271dc02), [BlackHat talk](https://www.youtube.com/watch?v=UnudlFeHlrU)
