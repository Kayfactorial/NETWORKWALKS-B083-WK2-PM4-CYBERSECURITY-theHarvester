<div align="center">

# 🔐 theHarvester Domain Reconnaissance

**Conducting reconnaissance and footprinting using microsoft.com as a case study**
</div>

<p align="center">
  <img src="https://img.shields.io/badge/Skill-Cybersecurity-404040?style=flat-square&labelColor=C00000" />
  <img src="https://img.shields.io/badge/Ver-Virtualbox%20v7.2-0070C0?style=flat-square&labelColor=000000" />
  <img src="https://img.shields.io/badge/Kali%20Linux-v2026.2-E87500?style=flat-square&labelColor=000000&logo=kalilinux&logoColor=white" />
  <img src="https://img.shields.io/badge/Skill-Linux-404040?style=flat-square&labelColor=C00000" />
  <img src="https://img.shields.io/badge/Network-10.0.0.0%2F24-238F89?style=flat-square&labelColor=000000" />
  <img src="https://img.shields.io/badge/Penetration%20Testing-C00000?style=flatsquare&labelColor=000000&logo=kalilinux&logoColor=white" />
  <img src="https://img.shields.io/badge/Skill-theHarvester-404040?style=flat-square&labelColor=C00000" />
  <img src="https://img.shields.io/badge/GitHub-404040?style=flat-square&labelColor=0070C0&logo=github&logoColor=white" />
  <img src="https://img.shields.io/badge/Kali%20Linux-404040?style=flat-square&labelColor=C00000&logo=kalilinux&logoColor=white" />
  <img src="https://img.shields.io/badge/Ethical%20Hacking-E87500?style=flat-square&labelColor=000000&logo=kalilinux&logoColor=white" />
  <img src="https://img.shields.io/badge/Adio%20Kabiru%20-C00000?style=flat-square" />
</p>

## Project Overview

This project documents a practical domain reconnaissance exercise performed with **theHarvester 4.10.1** as part of the Networkwalks W2-PM4 cybersecurity assignment.

The exercise focused on collecting publicly available information associated with the domain `microsoft.com` and documenting the limitations encountered during multi-source reconnaissance.

> **Authorization and Ethics:** This repository is for cybersecurity education and authorized security assessment only. Do not use these techniques against systems or data outside an approved scope.

## Project Objectives

- Understand passive/public-source reconnaissance.
- Use theHarvester to collect domain-related information.
- Compare a single-source search with a multi-source search.
- Document tool output and limitations.
- Understand how reconnaissance contributes to attack-surface analysis.

## Tools Used

- **theHarvester:** 4.10.1
- **Platform:** Kali Linux
- **Target used in the exercise:** `microsoft.com`

## Command line used

### Baidu-only search

```bash
theHarvester -d microsoft.com --l 1000 -b baidu
```

Result:

- IPs: 0
- Emails: 0
- People: 0
- Hosts: 0

### Multi-source search

```bash
theHarvester -d microsoft.com --l 50 -b all
```

The multi-source run attempted several available data sources.

## Results Summary

| Finding | Result |
|---|---:|
| IP addresses | 142 |
| Email addresses | 3 |
| People | 0 |
| Hosts | 9,978 |
| ASNs | 6 |
| Interesting URLs | 1 |
| Windvane fallback subdomains | 14 |
| Hudson Rock hosts | 43 |
| LinkedIn users | 0 |

### Email addresses returned

- `dotnet-docker-bot@microsoft.com`
- `opencode@microsoft.com`
- `secure@microsoft.com`

These values are reproduced as tool output from the training exercise and are not independently verified.

## Limitations

The multi-source run showed several operational limitations:

- Many sources required API keys that were not configured.
- Some sources returned authentication or invalid-key errors.
- Some services experienced DNS, connection, timeout, or API-response problems.
- A single search source may provide significantly less information than a multi-source run.
- The results should not be treated as a complete inventory because source coverage was incomplete.

## Security Relevance

Reconnaissance helps security professionals understand what information may be publicly discoverable about an organization. Publicly discoverable infrastructure information can contribute to external attack-surface analysis.

The findings in this project are **reconnaissance observations, not confirmed vulnerabilities**.

## Evidence

![theHarvester Baidu Search](https://github.com/adkasu/NETWORKWALKS-B083-WK2-PM4-CYBERSECURITY-theHarvester/blob/9f70ce0b61b4cd4590d9dfffbcab5b7b214e50f2/theHarvester02.png)

*Figure 1: theHarvester 4.10.1 Baidu search against `microsoft.com`.*


![theHarvester all Search](https://github.com/adkasu/NETWORKWALKS-B083-WK2-PM4-CYBERSECURITY-theHarvester/blob/bd7b990271696a643552456aed85224de0e29c97/theHarvester03.png)

*Figure 2: theHarvester 4.10.1 All method search against `microsoft.com`.*


## Lessons Learned

1. Reconnaissance results depend heavily on the sources available to the tool.
2. A zero-result search does not prove that no public information exists.
3. API credentials and service availability affect automated reconnaissance.
4. Tool output must be interpreted carefully rather than treated as verified fact.
5. Good cybersecurity practice requires accurate documentation and clear authorization.

## Author

**Adio Kabiru**  
Network Engineer | Cybersecurity | Telecommunications Engineer | Network Security Engineer

#Cybersecurity #NetworkSecurity #theHarvester #Reconnaissance #KaliLinux #OSINT #EthicalHacking
