---
layout: technique
title: Anti-sandbox
description: Detecting and blocking security analysis tools from interacting with the page
---

# Anti-sandbox

## Summary

Attackers are implementing anti-debugging techniques to evade manual analysis and sandbox hooking. These techniques are used to detect whether the phishing kit is being analyzed in a sandbox, debugged, or reverse-engineered. Attackers can:

- Check if a debugger is running on the machine with scripts that detect common debuggers.
- Check if the phishing kit is being run in a VM or emulated environment.
- Check for analysis tools or software running in the browser environment.
- Check if dev tools are installed or opened on the page. 
- Detect unusual screen resolutions, browser configurations, or user agent strings that indicate an abnormal configuration for a user. 

## Examples

- [Example 1: Tycoon 2FA AitM kit anti-analysis](https://blog.barracuda.com/2025/01/22/threat-spotlight-tycoon-2fa-phishing-kit#:~:text=If%20developer%20tools%20are%20open%2C,com) — If a visitor has developer tools open (a sign of a researcher or sandbox environment), Tycoon will intentionally slow down – introducing artificial lag in page functionality. If the page detects that operations are taking too long (e.g. due to breakpoints or inspection), it will redirect the user to a harmless site (OneDrive).
- [Example 2: Tycoon 2FA AitM kit anti-analysis](https://www.trustwave.com/en-us/resources/blogs/spiderlabs-blog/tycoon2fa-new-evasion-technique-for-2025/) Tycoon using anti-debugging scripts to hinder researchers and slow down detection.
- [Example 3: Tycoon 2FA visitor screening](https://cybersecuritynews.com/top-3-evasion-techniques-in-phishing-attacks-real-examples-inside/#:~:text=2) — Tycoon profiles visitors by screen resolution, plugins, timezone, etc. when a user hit the link. If the visitor fit the expected profile (e.g. from the right company or geolocation), they were redirected to the phishing site; if not, they were sent to a benign page.
- [Example 4: Using screening "gate" pages before serving malicious pages](https://sublime.security/blog/aitm-phishing-with-russian-infrastructure-and-detection-evasion-from-a-lapsed-domain/) — The phishing infrastructure excluded specific domains, checked if the visitor was a bot through user-agent matching and checking for signs of headless browsers, checking the IP of the visitor against a blocklist, and checking for specific domains in the email field, tested in a server-side fingerprint check.
- [Example 5: Blocking security IPs](https://www.akamai.com/blog/security/catch-me-if-you-can-evasive-and-defensive-techniques-in-phishing#:~:text=match%20at%20L735%20phishing%20kits%2C,known%20researchers%2C%20universities%2C%20and%20more) — Blocking IP ranges belonging to security vendors, cloud providers, known scanners (like VirusTotal, urlscan, etc.), and even university research labs. They place these in .htaccess or server rules so that any request from those IPs is refused.
