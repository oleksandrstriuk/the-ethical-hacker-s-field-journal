# Privilege Escalation

Privilege escalation is a complex journey with no universal solutions, heavily influenced by the specific configuration of the target system. Factors such as the kernel version, installed applications, supported programming languages, and other users' passwords are critical elements that will shape your path to achieving root or administrative access.

## Concepts

### Vertical Privilege Escalation
- **Definition:** Gaining higher privileges than initially granted (e.g., from a regular user to an administrator).
- **Example:** Exploiting a vulnerability to obtain root access on a Linux system.
  - **Linux Example:** Using the `sudo` command to exploit improper configurations.
    ```sh
    sudo -i
    ```
  - **Windows Example:** Exploiting a vulnerable service to get SYSTEM privileges using Metasploit.
    ```sh
    use exploit/windows/local/bypassuac
    set session 1
    exploit
    ```

### Horizontal Privilege Escalation
- **Definition:** Accessing the same level of privileges but with different or unauthorized resources.
- **Example:** A user accessing another user's data without permission.
  - **Web Application Example:** Exploiting insecure direct object references (IDOR).
    ```sh
    http://example.com/user?id=2
    ```

## Techniques

### Exploiting Software Vulnerabilities
- **Buffer Overflows:** Leveraging coding errors to execute arbitrary code.
  - **Example:** Using a buffer overflow in a custom application.
    ```c
    #include <string.h>
    int main() {
        char buffer[10];
        strcpy(buffer, "AAAAAAAAAAAAAAAAAAAA");
    }
    ```

### Credential Dumping
- **Definition:** Extracting passwords or tokens from memory to use them for privilege escalation.
  - **Windows Example:** Using Mimikatz to extract plaintext passwords.
    ```sh
    mimikatz # sekurlsa::logonpasswords
    ```

### Bypassing Access Controls
- **Definition:** Finding and exploiting flaws in the system's security controls.
  - **Example:** Exploiting weak file permissions on sensitive files.
    ```sh
    cat /etc/shadow
    ```

## Best Practices
- **Authorization:** Always obtain proper authorization before attempting privilege escalation.
- **Documentation:** Document all methods and findings thoroughly.
- **Ethical Guidelines:** Follow ethical guidelines and legal requirements throughout the process.
- **Mitigation:** Identify and suggest mitigations for vulnerabilities discovered.
