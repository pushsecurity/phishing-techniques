---
layout: technique
title: Instant messenger (IM)
description: Using IM platforms to distribute phishing links
---

# Instant messenger

## Summary

Instant messenger (IM) platforms are now the core of corporate communications and the place where most work-related communication takes place. Attackers are targeting both business IM platforms like Slack and Teams, as well as IM platforms like WhatsApp and Signal that are used for both business and personal purposes. 

Delivering phishing links via IM platform evades traditional email-based controls while also taking advantage of the fact that users do not expect to be served phishing links via IM platforms — particularly business IM like Slack or Teams. 

It is no longer possible to message Slack and Teams users as an external user without first configuring external/guest access and issuing an invitation to join either the tenant or specific channels/workspaces within the tenant. However, attackers have successfully leveraged IM by:

Creating an attacker-owned Slack or Teams tenant and inviting target users to join your tenant. 
- Social engineering a target employee to invite you to their tenant (which may or may not require admin approval depending on the configuration and level of access granted). 
- Using IM as the delivery mechanism for a malicious link as part of a multi-step social engineering attack. 
- Taking over an IM account (e.g. via credential stuffing) and using the compromised account to deliver phishing links and expand the scope of the breach. 

## Examples

- [Example 1: Storm-0324 distributes malware using TeamsPhisher](https://www.microsoft.com/en-us/security/blog/2023/09/12/malware-distributor-storm-0324-facilitates-ransomware-access/) - Beginning in July 2023, Storm-0324 was observed distributing payloads using an open-source tool to send phishing lures through Microsoft Teams chats.
- [Example 2: Black Basta ransomware poses as IT support on Microsoft Teams to breach networks](https://www.bleepingcomputer.com/news/security/black-basta-ransomware-poses-as-it-support-on-microsoft-teams-to-breach-networks/) - — A Black Basta social engineering campaign flooded targeted employees' inboxes with thousands of emails. The threat actors would then call the overwhelmed employee, posing as their company's IT help desk to help them with their spam problems. The attackers trick the person into installing the AnyDesk remote support tool or providing remote access to their Windows devices by launching the Windows Quick Assist remote control and screen-sharing tool.
- [Example 3: How hackers targeted Slack to break into EA Games](https://www.vice.com/en/article/how-ea-games-was-hacked-slack/) - Hackers breached Electronic Arts by tricking an IT support employee on Slack. After stealing an EA Slack login token (bought for $10), they entered an internal Slack channel and posed as an employee who “lost his phone.” The hackers convinced IT to provide multi-factor login codes, twice, which let them into EA’s network.
- [Example 4: "Urgent Zoom meeting" credential phish](https://onlineacademiccommunity.uvic.ca/phishbowl/2025/05/21/urgent-zoom-meeting/) — A campaign targeted university staff with fake Zoom invite emails that appeared to come from colleagues and implied urgent HR issues. The invite link opened what looked like a live Zoom meeting with “real” participants (actually pre-recorded video feeds) to build legitimacy. It then presented a spoofed Zoom login page to harvest the user’s Office 365 credentials. 
- [Example 5: Russian threat actors target victims over Signal](https://www.volexity.com/blog/2025/02/13/multiple-russian-threat-actors-targeting-microsoft-device-code-authentication/) - Russian threat actors aimed at compromising Microsoft 365 (M365) accounts via spear-phishing via Signal.

## Further reading

- [Slack Attack: A phisher's guide to initial access](https://pushsecurity.com/blog/slack-phishing-for-initial-access/)
- [Slack Attack: A phisher's guide to persistence and lateral movement](https://pushsecurity.com/blog/phishing-slack-persistence/)
- [Phishing Microsoft Teams for initial access](https://pushsecurity.com/blog/phishing-microsoft-teams-for-initial-access/)
