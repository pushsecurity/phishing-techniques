---
layout: technique
title: Conditional loading
description: Failing to load the phishing content unless certain conditions are met
---

# Conditional loading

## Summary

Phishing kits often include logic to only deliver the malicious payload under specific conditions — for example, only if the visitor came from a particular email campaign link, or only if they are in a certain organization, using a certain browser, etc. If the conditions aren’t met, the phish might show benign content or nothing at all. This selective targeting helps evade detection by unwanted parties (like security researchers or untargeted users).

## Examples

- [Example 1: NakedPages AitM kit](https://pushsecurity.com/blog/how-aitm-phishing-kits-evade-detection/#id-step-3-required-url-parameters-and-custom-auth-headers) — Requires specific URL parameters and headers, as well as B2B targeting where visitors entering a personal email address would be redirected to a benign page. 
- [Example 2: Using screening "gate" pages before serving malicious pages](https://sublime.security/blog/aitm-phishing-with-russian-infrastructure-and-detection-evasion-from-a-lapsed-domain/) — The phishing infrastructure excluded specific domains, checked if the visitor was a bot through user-agent matching and checking for signs of headless browsers, checking the IP of the visitor against a blocklist, and checking for specific domains in the email field, tested in a server-side fingerprint check.
- [Example 3: Evilginx lure URLs in Scattered Spider campaigns](https://pushsecurity.com/blog/scattered-spider-ttp-evolution-in-2025/#id-scattered-spider-ttp-evolution-in-2025_id-using-commercial-aitm-toolkits-like-evilginx-to-bypass-mfa-and-evade-detection) — Evilginx requires that specific lure URLs are accessed to load the phishing page. Attempting to load the domain natively will redirect you (typically by "Rick Roll") or blocking your IP address permanently.
- [Example 4: Precision-validated targeting](https://cofense.com/blog/the-rise-of-precision-validated-credential-theft-a-new-challenge-for-defenders) — When a user attempts to access the phishing page, their email address is checked against the attacker’s database before the fraudulent credential phishing login form is displayed. If the email address entered does not match any from the pre-collected list, the phishing page either returns an error or redirects to a legitimate, benign-looking, page preventing security teams from doing further analysis and investigation.
- [Example 5: Tycoon 2FA AitM kit](https://cybersecuritynews.com/top-3-evasion-techniques-in-phishing-attacks-real-examples-inside/#:~:text=2) — Tycoon profiles visitors by screen resolution, plugins, timezone, etc. when a user hit the link. If the visitor does not fit the target profile (e.g. from the right company or geolocation) they are sent to a benign site. 
- [Example 6: Blocking security IPs](https://www.akamai.com/blog/security/catch-me-if-you-can-evasive-and-defensive-techniques-in-phishing#:~:text=match%20at%20L735%20phishing%20kits%2C,known%20researchers%2C%20universities%2C%20and%20more) — Blocking IP ranges belonging to security vendors, cloud providers, known scanners (like VirusTotal, urlscan, etc.), and even university research labs. They place these in .htaccess or server rules so that any request from those IPs is refused.
- Example 7: Dynamic IP locking — Using a “one IP, one chance” rule. The first visit from a given IP will get the phishing page; any subsequent visits from the same IP get a fake 404 or redirect. This means if a security analyst tries to revisit a URL from their machine (same IP), it won’t show the phish again.
