[![badge](https://img.shields.io/badge/Push%20Security-Sponsored%20Project-blue.svg?logo=data:image/svg+xml;base64,PHN2ZyB3aWR0aD0nMzExJyBoZWlnaHQ9JzE1Mycgdmlld0JveD0nMCAwIDMxMSAxNTMnIGZpbGw9J25vbmUnIHhtbG5zPSdodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2Zyc+PHBhdGggZD0nTTIzNS4wMjIgMTUyLjEwN0MyNzYuODU2IDE1Mi4xMDcgMzEwLjkwMSAxMTguMDk2IDMxMC45MDEgNzYuMzA0OUMzMTAuOTAxIDM0LjUxMzQgMjc2Ljg3MSAwLjUwMjkzIDIzNS4wMjIgMC41MDI5M0MxOTMuMTc0IDAuNTAyOTMgMTU5LjE0NCAzNC41MTM0IDE1OS4xNDQgNzYuMzA0OUMxNTkuMTQ0IDExOC4wOTYgMTkzLjE4OCAxNTIuMTA3IDIzNS4wMjIgMTUyLjEwN1pNMjAyLjc1IDQ0LjA2NDlDMjExLjM3MyAzNS40NTA3IDIyMi44MjUgMzAuNzA0NyAyMzUuMDIyIDMwLjcwNDdDMjQ3LjIxOSAzMC43MDQ3IDI1OC42NzIgMzUuNDUwNyAyNjcuMjk1IDQ0LjA2NDlDMjc1LjkxOCA1Mi42NzkxIDI4MC42NjkgNjQuMTM0OSAyODAuNjY5IDc2LjMwNDlDMjgwLjY2OSA4OC40NzQ4IDI3NS45MTggOTkuOTMwNyAyNjcuMjk1IDEwOC41NDVDMjU4LjY3MiAxMTcuMTU5IDI0Ny4yMTkgMTIxLjkwNSAyMzUuMDIyIDEyMS45MDVDMjIyLjgyNSAxMjEuOTA1IDIxMS4zNzMgMTE3LjE1OSAyMDIuNzUgMTA4LjU0NUMxOTQuMTI3IDk5LjkzMDcgMTg5LjM5MSA4OC40NzQ4IDE4OS4zOTEgNzYuMzA0OUMxODkuMzkxIDY0LjEzNDkgMTk0LjE0MiA1Mi42NzkxIDIwMi43NSA0NC4wNjQ5WicgZmlsbD0nI0ZENzQ1MicvPjxwYXRoIGQ9J00xNDIuMjg3IDAuNTAyOTNMNTQuNjU3NyAxNTIuMTA3SDg5LjU4MTNMMTc3LjE5NiAwLjUwMjkzSDE0Mi4yODdaJyBmaWxsPScjRkQ3NDUyJy8+PHBhdGggZD0nTTg3LjYyOTEgMC41MDI5M0wwIDE1Mi4xMDdIMzQuOTIzNkwxMjIuNTUzIDAuNTAyOTNIODcuNjI5MVonIGZpbGw9JyNGRDc0NTInLz48L3N2Zz4=)](https://pushsecurity.com)
[![badge](https://img.shields.io/twitter/follow/pushsecurity?style=social)](https://x.com/pushsecurity)

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
