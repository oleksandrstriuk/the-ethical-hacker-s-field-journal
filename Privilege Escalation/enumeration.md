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
