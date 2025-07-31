# Phishing Techniques Database

**To view the techniques, visit the micro site: [https://pushsecurity.github.io/phishing-techniques/](https://pushsecurity.github.io/phishing-techniques/)**

This project documents a collection of modern phishing detection evasion techniques, breaking down the methods that attackers use at different stages of a phishing attack culminating in account takeover (i.e. stealing sessions, credentials, etc.). Each stage groups the techniques observed against a phase of activity designed to overcome a layer of security control.

The site features an interactive matrix interface where you can click on any cell to learn more about specific phishing techniques across 8 key phases: Targeting, Link Delivery, Link Camouflage, TI Evasion, Anti-Analysis, Page Obfuscation, Defeat MFA & CA, and Account Takeover.

## Adding a New Technique

1. **Copy an existing technique file** from `_techniques/` and rename it
2. **Update the content** with your new technique information
3. **Add to the table configuration** by editing `_data/techniques-table.yml`:

```yaml
columns:
  - name: "Column Name"
    techniques:
      - "existing-technique"
      - "your-new-technique"  # Add your technique reference here
```

The technique reference should match your filename (without the `.md` extension).