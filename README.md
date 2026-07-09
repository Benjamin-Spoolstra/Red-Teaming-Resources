# Red Team & CTF Toolkit

A curated collection of tools, cheatsheets, guides, and reference material for CTF competitions, penetration testing, and red team engagements.

> ⚠️ **Ethical Use Only**
> Everything in this repository is intended strictly for **authorized** security testing — CTFs, bug bounty programs with defined scope, and engagements covered by a signed rules of engagement (RoE) or penetration testing agreement. Do not use these resources against systems you do not own or have explicit written permission to test.

---

## Table of Contents

- [General / Productivity](#general--productivity)
- [Red Team TTPs & Guides](#red-team-ttps--guides)
- [C2 Infrastructure & Redirectors](#c2-infrastructure--redirectors)
- [OSINT & Reconnaissance](#osint--reconnaissance)
- [Web Application Pentesting & Payloads](#web-application-pentesting--payloads)
- [WAF Bypass](#waf-bypass)
- [Active Directory & Windows Internals](#active-directory--windows-internals)
- [Wordlists & Fuzzing](#wordlists--fuzzing)
- [Cloud Security (AWS / Azure / GCP)](#cloud-security-aws--azure--gcp)
- [CTF General Resources](#ctf-general-resources)
- [Contributing](#contributing)

---

## General / Productivity

- [tmux Cheatsheet](https://tmuxcheatsheet.com/) — Quick reference for tmux keybindings and commands, essential for managing multiple sessions during engagements.

## Red Team TTPs & Guides

- [Red-Teaming-TTPs](https://github.com/RoseSecurity/Red-Teaming-TTPs/tree/main) — Collection of red team tactics, techniques, and procedures.
- [Red Team Guide](https://redteam.guide/) — Field-tested notes and command references for red team operators.

## C2 Infrastructure & Redirectors

- [Azure Static Web App C2 Redirector](https://rosesecurity.gitbook.io/red-teaming-ttps/guides/azurestaticwebapplicationc2redirectors) — Guide for setting up C2 redirection using Azure Static Web Apps.

## OSINT & Reconnaissance

- [OSINT Framework](https://osintframework.com/) — Interactive directory of OSINT tools organized by category.
- [Awesome-OSINT-List](https://github.com/Astrosp/Awesome-OSINT-List) — Curated list of OSINT resources and tools.
- [bbot](https://github.com/blacklanternsecurity/bbot) — Recursive internet scanner for automated OSINT and attack surface mapping.
- [Google Dorks for Bug Bounty](https://taksec.github.io/google-dorks-bug-bounty/) — Curated Google dork queries for recon and bug bounty hunting.

## Web Application Pentesting & Payloads

- [HackTricks](https://hacktricks.wiki/en/index.html) — Extensive wiki covering pentesting techniques, tricks, and methodology across many attack surfaces.
- [PayloadsAllTheThings](https://github.com/swisskyrepo/PayloadsAllTheThings) — Comprehensive list of payloads and bypass techniques for web app pentesting.
- [coffinxp/payloads](https://github.com/coffinxp/payloads) — Additional payload collection for web application testing.

## WAF Bypass

- [WAF Bypass](https://waf-bypass.com/) — Techniques and payloads for evading web application firewalls.
- [waf.secmy.app](https://waf.secmy.app/) — WAF bypass reference and testing resource.

## Active Directory & Windows Internals

> Add your preferred resources here — some well-known starting points if useful:
- [BloodHound](https://github.com/SpecterOps/BloodHound) — AD attack path mapping and analysis.
- [ADRecon](https://github.com/adrecon/ADRecon) — Active Directory recon tool that generates a detailed report.
- [LOLBAS](https://lolbas-project.github.io/) — Living Off the Land Binaries, Scripts, and Libraries for Windows.
- [GTFOBins](https://gtfobins.github.io/) — Unix binaries usable to bypass local security restrictions (Linux counterpart to LOLBAS).

## Wordlists & Fuzzing

> Add your preferred resources here — some well-known starting points if useful:
- [SecLists](https://github.com/danielmiessler/SecLists) — The security tester's companion: usernames, passwords, URLs, fuzzing payloads, and more.
- [FuzzDB](https://github.com/fuzzdb-project/fuzzdb) — Attack patterns, predictable resource locations, and other fuzzing dictionaries.
- [ffuf](https://github.com/ffuf/ffuf) — Fast web fuzzer written in Go.

## Cloud Security (AWS / Azure / GCP)

- See [Azure Static Web App C2 Redirector](#c2-infrastructure--redirectors) above for Azure-specific offensive infrastructure.
> Add your preferred resources here — some well-known starting points if useful:
- [Prowler](https://github.com/prowler-cloud/prowler) — Cloud security assessment tool for AWS, Azure, and GCP.
- [Pacu](https://github.com/RhinoSecurityLabs/pacu) — AWS exploitation framework.
- [ScoutSuite](https://github.com/nccgroup/ScoutSuite) — Multi-cloud security auditing tool.

## CTF General Resources

> Add your preferred resources here — some well-known starting points if useful:
- [CTFtime](https://ctftime.org/) — CTF event calendar, team rankings, and post-event writeups.
- [CTF101](https://ctf101.org/) — Beginner-friendly introduction to common CTF categories and techniques.
- [pwn.college](https://pwn.college/) — Free hands-on training platform covering binary exploitation and systems security.

---

## Contributing

Suggestions and pull requests are welcome. Please ensure any submitted resource is relevant to authorized security testing, CTFs, or ethical red teaming, and does not promote unauthorized access to systems.
