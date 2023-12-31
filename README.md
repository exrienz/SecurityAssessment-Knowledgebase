# Pentest Checklist
My Personal Common WASA Attack Type Checklist


## Common WASA Attack Type

#### Server Side Request Forgery (SSRF)
In an SSRF attack, the attacker can deceive the server into accessing internal services (e.g. 127.0.0.1, localhost, ) that should be restricted within the organization. [Notes](https://xmind.works/qpyTPkxH) | [PAT](https://github.com/swisskyrepo/PayloadsAllTheThings/tree/master/CSRF%20Injection)

Chainable vulnerability / Requirement:
- Open Redirect
- LFI/RFI

#### CORS Misconfiguration
CORS (Cross-Origin Resource Sharing) Injection is a security issue that happens when a web application wrongly sets its CORS rules, allowing attackers to misuse it. [Notes](https://xmind.works/6DIPUxIm) | [PAT](https://github.com/swisskyrepo/PayloadsAllTheThings/blob/master/CORS%20Misconfiguration/README.md)

Requirement:
- Request > Origin: https://evil.com
- Response > Access-Control-Allow-Credential: true
- Response > Access-Control-Allow-Origin: https://evil.com OR Access-Control-Allow-Origin: null

#### Account Takeover Attack
Exploit a range of vulnerabilities, such as weak password reset tokens, 2FA (two-factor authentication) weaknesses, and inadequate input validation. Through methods like manipulating referrers, utilizing cross-site scripting, or leveraging flaws in password reset processes, attackers maneuver their way into unauthorized account access. [PAT](https://github.com/swisskyrepo/PayloadsAllTheThings/tree/master/Account%20Takeover)

Via:
- [Misconfigured/weak password reset module](https://github.com/swisskyrepo/PayloadsAllTheThings/tree/master/Account%20Takeover#account-takeover-via-jwt)
- [XXS (Leaked cookie)](https://github.com/swisskyrepo/PayloadsAllTheThings/tree/master/Account%20Takeover#account-takeover-via-jwt)
- [HTTP Request Smuggling](https://github.com/swisskyrepo/PayloadsAllTheThings/tree/master/Account%20Takeover#account-takeover-via-jwt)
- [CSRF](https://github.com/swisskyrepo/PayloadsAllTheThings/tree/master/Account%20Takeover#account-takeover-via-jwt)
- [JWT](https://github.com/swisskyrepo/PayloadsAllTheThings/tree/master/Account%20Takeover#account-takeover-via-jwt)
- [2FA Bypasses](https://github.com/swisskyrepo/PayloadsAllTheThings/tree/master/Account%20Takeover#2fa-bypasses)

#### API Key Abuse
APIs are the keys to an organization’s databases, so it’s essential to control who has access to them. Finding Hidden API Keys & How to Use Them. [PAT](https://github.com/swisskyrepo/PayloadsAllTheThings/tree/master/API%20Key%20Leaks)

#### 




