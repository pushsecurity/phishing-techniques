---
layout: technique
title: Attacker-in-the-Middle (AiTM) Phishing
description: Using reverse-proxy phishing kits to steal user sessions
---

# Attacker-in-the-Middle (AiTM) Phishing

## Summary

MFA-bypassing Attacker-in-the-Middle phishing kits are the standard choice for attackers today. These work by intercepting the authenticated session created when a victim enters their password and completes an MFA check. To do this, the phishing website simply passes messages between the user and the real website — hence “Attacker-in-the-Middle”.

Attackers are using both criminal platforms and commodity, publicly available kits like Evilginx. 

There are a few different variations of AitM, including Browser-in-the-Middle (BitM), a technique using remote desktop technologies like VNC and RDP, where the victim is tricked into directly authenticating via the attacker’s browser. 

## Examples

- Example 1: [How phishing kits are evolving with AitM](https://pushsecurity.com/blog/phishing-2-0-how-phishing-toolkits-are-evolving-with-aitm/) — [Evilginx demo](https://www.youtube.com/watch?v=octo3ye8SwI)
- Example 2: Analysis of NakedPages AitM kit — [Part 1](https://www.youtube.com/watch?v=octo3ye8SwI), [Part 2](https://pushsecurity.com/blog/how-aitm-phishing-kits-evade-detection-p2/)
- Example 3: Scattered Spider use of AitM phishing — (1)[https://pushsecurity.com/blog/scattered-spider-ttp-evolution-in-2025/], (2)[https://www.silentpush.com/blog/scattered-spider-2025/#h-new-scattered-spider-ttps-for-2025]
- Example 4: [2025 surge in Tycoon 2FA attacks](https://www.proofpoint.com/us/blog/email-and-cloud-threats/aitm-phishing-attacks-evolving-threat-microsoft-365)
- Example 5: [EvilProxy BEC attack results in redirecting large financial transaction](https://thomasmurray.com/insights/evilproxy-deep-dive-outlook-teams-ps1m-heist)
- Example 6: [AitM attack on Mailchimp](https://pushsecurity.com/blog/dissecting-a-recent-mailchimp-phishing-attack/)
- Example 7: [AitM attack on Onfido](https://pushsecurity.com/blog/investigating-a-recent-malvertising-campaign-targeting-onfido-customers/)
