# Network Scanning and Enumeration

## Enumeration

A crucial phase in the ethical hacking process. It involves gathering information about a target network to identify potential vulnerabilities and targets for further exploitation.

### Basic Concepts

- **Port Scanning**: Port scanning is the process of identifying open ports and services running on a target system.
  
- **Service Enumeration**: Service enumeration involves gathering detailed information about the services running on the identified open ports, including version numbers and configurations.

- **Operating System (OS) Fingerprinting**: OS fingerprinting is the process of identifying the operating system running on a target system based on its responses to network requests.

### Tools and Techniques

#### Nmap

[Nmap](https://nmap.org/) is a powerful open-source tool for network scanning and enumeration. Here are some common Nmap commands:

- **TCP SYN Scan**: `nmap -sS <target>`
  
- **TCP Connect Scan**: `nmap -sT <target>`
  
- **UDP Scan**: `nmap -sU <target>`
  
- **OS Detection**: `nmap -O <target>`
  
- **Service Version Detection**: `nmap -sV <target>`
  
- **Script Scanning**: `nmap --script <script> <target>`

### Manual Enumeration

1. **DNS Enumeration**:
   - `nslookup domain.com`
   - `dig domain.com`
   - `dnsenum domain.com`
   - `dnsrecon -d domain.com`
   - `dig axfr @nameserver domain.com`

2. **Whois Lookup**:
   - `whois domain.com`
   - Online whois lookup tools

3. **Network Scanning**:
   - `nmap -sS -p- target_ip`
   - `nmap -sV -p <ports> target_ip`

4. **Web Enumeration**:
   - `dirb http://target_url`
   - `gobuster dir -u http://target_url -w /path/to/wordlist`

5. **Vulnerability Scanning**:
   - `nessus` (for Nessus)
   - `openvas-start` (for OpenVAS)
   - Manual testing for web vulnerabilities (SQLi, XSS, etc.)

6. **Password Enumeration**:
   - `hydra -L usernames.txt -P passwords.txt target_ip service`
   - `medusa -U usernames.txt -P passwords.txt -h target_ip -M service`

7. **File and Directory Enumeration**:
   - `enum4linux -a target_ip`
   - Explore FTP server: `ftp target_ip`

### Automated Enumeration Tools

- LinPeas: https://github.com/carlospolop/privilege-escalation-awesome-scripts-suite/tree/master/linPEAS
- LinEnum: https://github.com/rebootuser/LinEnum
- LES (Linux Exploit Suggester): https://github.com/mzet-/linux-exploit-suggester
- Linux Smart Enumeration: https://github.com/diego-treitos/linux-smart-enumeration
- Linux Priv Checker: https://github.com/linted/linuxprivchecker 
