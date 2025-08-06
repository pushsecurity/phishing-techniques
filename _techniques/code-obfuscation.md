---
layout: technique
title: Code obfuscation
description: Using obfuscated page code to prevent analysis
---

# Code obfuscation

## Summary

Attackers are using various techniques to obfuscate the page code in order to prevent analysis, typically through encoding and dynamically generating page code. 

Page code is often obfuscated using encryption libraries or simple XOR encryption. The code must include the decryption keys so that it can load in the browser. But without analysing or running the code, the web payloads look completely random from a network level — making it extremely tough to detect in that way as there are no static signatures. 

By obfuscating the page code, there are fewer elements that can be analysed using signature-based checks searching for indicators of malicious content. 

## Examples

- [Example 1: Tycoon 2FA AitM kit](https://www.trustwave.com/en-us/resources/blogs/spiderlabs-blog/tycoon2fa-new-evasion-technique-for-2025/) — Tycoon uses invisible unicode characters and JavaScript Proxy objects to complicate static analysis and defer script execution until runtime. The phishing page’s script contained what looked like blank space but was actually a binary-encoded payload; a short bootstrap code used a JavaScript Proxy to detect when the hidden property was accessed and then reconstruct the real code at runtime.
- [Example 2: Invisible unicode characters](https://www.bleepingcomputer.com/news/security/phishing-attack-hides-javascript-using-invisible-unicode-trick/) — Attackers are using  unicode characters, specifically Hangul half-width (U+FFA0) and Hangul full-width (U+3164), to make JS payloads invisible.
- [Example 3: Phishing HTML segmentation and encoding](https://www.microsoft.com/en-us/security/blog/2021/08/12/attackers-use-morse-code-other-encryption-methods-in-evasive-phishing-campaign/) — Microsoft identified cases where the phishing HTML was split into segments and encoded with layers of obfuscation, using unusual ciphers like Morse code. 
- [Example 4: Blov HTML Crypter](https://securityboulevard.com/2024/11/blov-html-crypter-phishing-evasion-through-encryption-and-obfuscation/) — Attackers are using tools like Blov HTML Crypter to perform CSS and HTML minification, JavaScript obfuscation, and AES encryption to hide malicious code.
- [Example 5: WOFF obfuscation](https://cloud.google.com/blog/topics/threat-intelligence/phishing-campaign-woff-obfuscation-telegram-communications/) — Using a custom WOFF font as a substitution cipher for page text. This font-based obfuscation broke simple keyword matching, since the real text was never present in the HTML source – only the browser’s rendering after applying the font showed the actual message.
