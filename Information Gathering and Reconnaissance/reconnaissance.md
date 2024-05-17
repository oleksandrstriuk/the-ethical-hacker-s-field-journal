# Reconnaissance

Reconnaissance is the initial phase of ethical hacking where information about a target is gathered to identify vulnerabilities. This phase is crucial for understanding the target's infrastructure and potential entry points.

### Passive Reconnaissance
- **OSINT (Open Source Intelligence):** Gathering information from publicly available sources.
  - Examples: Websites, social media, public records.

### Active Reconnaissance
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
  - `whatweb example.com`
- **Wappalyzer:** Browser extension to identify technologies on websites.

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
- **Courses:**
  - [Offensive Security Certified Professional (OSCP)](https://www.offensive-security.com/courses-and-certifications/oscp/)
  - [Certified Ethical Hacker (CEH)](https://www.eccouncil.org/programs/certified-ethical-hacker-ceh/)

## Conclusion
Reconnaissance sets the foundation for successful ethical hacking by identifying potential vulnerabilities and gathering essential information about the target. Always ensure to follow ethical guidelines and legal boundaries during this process.
