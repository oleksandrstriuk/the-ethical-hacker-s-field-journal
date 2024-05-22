# Reconnaissance

Reconnaissance is the initial phase of ethical hacking where information about a target is gathered to identify vulnerabilities. This phase is crucial for understanding the target's infrastructure and potential entry points.

# Passive Information Gathering

- Identifying IP addresses & DNS information.
- Identifying domain names and domain ownership information.
- Identifying email addresses and social media profiles.
- Identifying web technologies being used on target sites.
- Identifying subdomains.

# Active Information Gathering

- Discovering open ports on target systems.
- Learning about the internal infrastructure of a target network/organization.
- Gathering information from target systems.

### Passive
- **OSINT (Open Source Intelligence):** Gathering information from publicly available sources.
  - Examples: Websites, social media, public records.

### Active
- **Scanning and Probing:** Direct interaction with the target to gather information.
  - Examples: Network scanning, port scanning.

### OSINT Tools
- **Maltego:** Data visualization tool for link analysis.
  - `maltego`
- **theHarvester:** Email, subdomain, and name gathering tool.
  - `theharvester -d example.com -b all`

### Network Scanning Tools
- **Nmap:** Network mapping and vulnerability scanning.
  - `nmap -A example.com`
- **Masscan:** High-speed port scanner.
  - `masscan -p1-65535 example.com --rate=10000`

### Web Reconnaissance Tools
- **WhatWeb:** Identify websites and technologies used.
  - `whatweb somewebsite.com`
- **Wappalyzer:** Browser extension to identify technologies on websites.
- **BuiltWith:** Browser extension to find out what websites are built with, filter by location, traffic, vertical and more.
- **DNSdumpster:** DNS recon & research, find & lookup dns records.
- **Sublist3r:** Python tool designed to enumerate subdomains of websites using OSINT; available [here](https://github.com/aboul3la/Sublist3r).
- **Exploit DB:** Website that provides exploits, shellcode, 0days, remote exploits, local exploits, web apps, vulnerability reports, security articles, tutorials and more.

### Firewall Detectors
- **WAFW00F:** Web application firewall fingerprinting tool; available [here](https://github.com/EnableSecurity/wafw00f).

## Resources
- [OWASP Testing Guide](https://owasp.org/www-project-web-security-testing-guide/)
- [Nmap Documentation](https://nmap.org/book/man.html)
- [theHarvester GitHub](https://github.com/laramies/theHarvester)

## Best Practices
- Always obtain proper authorization before conducting reconnaissance.
- Document all findings meticulously.
- Use a combination of passive and active reconnaissance techniques for comprehensive information gathering.

## References
- **Books:** 
  - "The Web Application Hacker's Handbook" by Dafydd Stuttard and Marcus Pinto
  - "Hacking: The Art of Exploitation" by Jon Erickson
