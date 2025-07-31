---
layout: technique
title: Rentable subdomains
description: Using dynamic DNS services and rentable subdomains to evade domain-based detections
---

# Rentable subdomains

## Summary

Attackers are using rentable subdomains such as us.com and it.com. This technique essentially means that security feeds cannot gather WHOIS information on the subdomain, while the availability of these rentable subdomains (with tens of thousands of dynamic DNS providers) means attackers have an abundance of possible domains that look and feel legitimate compared to many traditional URLs. 

## Examples

- Example 1: Scattered Spider leverages rentable subdomains — Scattered Spider have been observed using [it.com](https://www.silentpush.com/blog/scattered-spider-2025/) and [us.com](https://pushsecurity.com/blog/scattered-spider-ttp-evolution-in-2025/#id-scattered-spider-ttp-evolution-in-2025_id-using-custom-subdomains-that-allow-public-registrations) 
- [Example 2: Free dynamic DNS services like DuckDNS and ChangeIP used by attackers](https://alluresecurity.com/fraudsters-abuse-dynamic-dns-subdomains/)
