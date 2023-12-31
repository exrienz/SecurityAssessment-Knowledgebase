# Pentest Checklist Summarized
My Personal Common WASA Attack Type Checklist


## Common WASA Attack Type

### Server Side Request Forgery (SSRF)
In an SSRF attack, the attacker can deceive the server into accessing internal services (e.g. 127.0.0.1, localhost, ) that should be restricted within the organization. [Notes](https://xmind.works/qpyTPkxH) | [PAT](https://github.com/swisskyrepo/PayloadsAllTheThings/tree/master/CSRF%20Injection)

Chainable vulnerability / Requirement:
- Open Redirect
- LFI/RFI

### CORS Misconfiguration
CORS (Cross-Origin Resource Sharing) Injection is a security issue that happens when a web application wrongly sets its CORS rules, allowing attackers to misuse it. [Notes](https://xmind.works/6DIPUxIm) | [PAT](https://github.com/swisskyrepo/PayloadsAllTheThings/blob/master/CORS%20Misconfiguration/README.md)

Requirement:
- Request > Origin: https://evil.com
- Response > Access-Control-Allow-Credential: true
- Response > Access-Control-Allow-Origin: https://evil.com OR Access-Control-Allow-Origin: null

### Account Takeover Attack
Exploit a range of vulnerabilities, such as weak password reset tokens, 2FA (two-factor authentication) weaknesses, and inadequate input validation. Through methods like manipulating referrers, utilizing cross-site scripting, or leveraging flaws in password reset processes, attackers maneuver their way into unauthorized account access. [PAT](https://github.com/swisskyrepo/PayloadsAllTheThings/tree/master/Account%20Takeover)

Via:
- [Misconfigured/weak password reset module](https://github.com/swisskyrepo/PayloadsAllTheThings/tree/master/Account%20Takeover#account-takeover-via-jwt)
- [XXS (Leaked cookie)](https://github.com/swisskyrepo/PayloadsAllTheThings/tree/master/Account%20Takeover#account-takeover-via-jwt)
- [HTTP Request Smuggling](https://github.com/swisskyrepo/PayloadsAllTheThings/tree/master/Account%20Takeover#account-takeover-via-jwt)
- [CSRF](https://github.com/swisskyrepo/PayloadsAllTheThings/tree/master/Account%20Takeover#account-takeover-via-jwt)
- [JWT](https://github.com/swisskyrepo/PayloadsAllTheThings/tree/master/Account%20Takeover#account-takeover-via-jwt)
- [2FA Bypasses](https://github.com/swisskyrepo/PayloadsAllTheThings/tree/master/Account%20Takeover#2fa-bypasses)

### API Key Abuse
APIs are the keys to an organization’s databases, so it’s essential to control who has access to them. Finding Hidden API Keys & How to Use Them. [PAT](https://github.com/swisskyrepo/PayloadsAllTheThings/tree/master/API%20Key%20Leaks)

### Injection
#### Cross-Site Scripting (XSS)
Cross-Site Scripting (XSS) is a type of security vulnerability that occurs when a web application allows users to input data that is then displayed on the website without proper validation or escaping. XSS attacks enable malicious actors to inject malicious scripts into web pages viewed by other users. These scripts can then run in the context of the victim's browser, potentially stealing sensitive information, defacing the website, or performing other malicious actions.

- Good Source: [Netsec](https://netsec.expert/posts/xss-in-2021/)
#### Code Injection
#### Argument Injection
[Argument injection](https://github.com/swisskyrepo/PayloadsAllTheThings/tree/master/Argument%20Injection#argument-injection) is similar to command injection as tainted data is passed to a command executed in a shell without proper sanitization/escaping.

List of exposed commands
- CURL
- TAR
- FIND
- WGET

### Business Logic Error
Unlike other types of security vulnerabilities like SQL injection or cross-site scripting (XSS), business logic errors do not rely on problems in the code itself (like unfiltered user input). Instead, they take advantage of the normal, intended functionality of the application, but use it in ways that the developer did not anticipate and that have undesired consequences. [Notes](https://github.com/exrienz/PentestChecklist/blob/main/wasa/business-logic.md)

