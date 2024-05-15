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
