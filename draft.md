## Common WASA Attack Type Sorted by Category for Quick Reference


### 1. [Business Logic Attack](https://github.com/swisskyrepo/PayloadsAllTheThings/tree/master/Business%20Logic%20Errors)
> Business logic errors, also known as business logic flaws, are a type of application vulnerability that stems from the application's business logic, which is part of the program that deals with real-world business rules and processes. These rules could include things like pricing models, transaction limits, or the sequences of operations that need to be followed in a multi-step process.


### 2. Social-Engineering Based Attack
- [Tabnabbing](https://github.com/swisskyrepo/PayloadsAllTheThings/tree/master/Tabnabbing)
	> Reverse tabnabbing is an attack where the user was originally routed on the correct page, while it will be changed to a phishing site, especially if the site looks the same as the target.
 	>> **Requirement:** XSS vulnerability (Higher success rate) 
- [Web Cache Deception](https://github.com/swisskyrepo/PayloadsAllTheThings/tree/master/Web%20Cache%20Deception)
	> Web Cache Deception (WCD) is a security issue where attackers trick web servers into storing private content at public URLs, potentially exposing sensitive information to unintended users. <br>
 	> **Source:** [Omergil](https://omergil.blogspot.com/2017/02/web-cache-deception-attack.html) 
 	>> **Requirement:** <br>
 	>> **Test Method:** ```example.com/profile;xx.css``` or ```example.com/profile.php/xx.css```
- [CSRF](https://book.hacktricks.xyz/pentesting-web/csrf-cross-site-request-forgery)
	> Cross-site request forgery (also known as CSRF) is a web security vulnerability that allows an attacker to induce users to perform actions that they do not intend to perform. Chained with Social Engineering attack.
   	>> **Requirement:** Misconfigured/Non-existence of CSRF token 


### 3. Session-Based Attack
- [Randomness](https://github.com/swisskyrepo/PayloadsAllTheThings/tree/master/Insecure%20Randomness)
- [JWT Misconfiguration](https://github.com/swisskyrepo/PayloadsAllTheThings/tree/master/JSON%20Web%20Token)
- [OAuth Misconfiguration](https://github.com/swisskyrepo/PayloadsAllTheThings/tree/master/OAuth%20Misconfiguration)
- [SAML Injection](https://github.com/swisskyrepo/PayloadsAllTheThings/tree/master/SAML%20Injection)


### 4. HTTP Header-Based Attack
- [HTTP Request Smuggling](https://github.com/dhmosfunk/simple-http-smuggler-generator)
- [CORS Misconfiguration](https://github.com/swisskyrepo/PayloadsAllTheThings/tree/master/CORS%20Misconfiguration)
- [Click-jacking](https://book.hacktricks.xyz/pentesting-web/clickjacking)


### 5. Generic Injection Based Attack
- [SSI](https://github.com/swisskyrepo/PayloadsAllTheThings/tree/master/Server%20Side%20Include%20Injection)
 	- > Server Side Includes (SSI) are special instructions placed in HTML pages, which the server processes while delivering the pages, allowing you to add dynamic content to a page without using complex methods like CGI programs or other dynamic technologies. Payload sample : 	```<!--#exec cmd="ls" -->```
- [Command Injection](https://github.com/swisskyrepo/PayloadsAllTheThings/tree/master/Command%20Injection)
	- > Command injection is a security vulnerability that allows an attacker to execute arbitrary commands inside a vulnerable application.
- [Directory Traversal](https://github.com/swisskyrepo/PayloadsAllTheThings/tree/master/Directory%20Traversal)
	- > A directory or path traversal consists in exploiting insufficient security validation/sanitization of user-supplied input file names so that characters representing "traverse to parent directory" are passed through.
- [File Inclusion](https://github.com/swisskyrepo/PayloadsAllTheThings/tree/master/File%20Inclusion)
	- > The File Inclusion vulnerability allows an attacker to include a file, usually exploiting a "dynamic file inclusion" mechanisms implemented in the target application.
- [SSRF](https://github.com/swisskyrepo/PayloadsAllTheThings/tree/master/Server%20Side%20Request%20Forgery)
	- > In an SSRF attack, the attacker can deceive the server into accessing internal services (e.g. 127.0.0.1, localhost, ) that should be restricted within the organization. [Notes](https://xmind.works/qpyTPkxH) | [PAT](https://github.com/swisskyrepo/PayloadsAllTheThings/tree/master/CSRF%20Injection)
	- > Chainable vulnerability / Requirement:
		- > Open Redirect
		- > LFI/RFI
- [SSTI](https://github.com/swisskyrepo/PayloadsAllTheThings/tree/master/Server%20Side%20Template%20Injection)
	- > Template injection allows an attacker to include template code into an existing (or not) template. A template engine makes designing HTML pages easier by using static template files which at runtime replace variables/placeholders with actual values in the HTML pages
- HTML Injection
	- [XSS](https://github.com/swisskyrepo/PayloadsAllTheThings/tree/master/XSS%20Injection)
 		- > Cross-site scripting (XSS) is a type of computer security vulnerability typically found in web applications. XSS enables attackers to inject client-side scripts into web pages viewed by other users.<br/><br/>
   Another source: [NetSec](https://netsec.expert/posts/xss-in-2021/) 	
	- [DOM Cloberring](https://github.com/swisskyrepo/PayloadsAllTheThings/tree/master/Dom%20Clobbering)
		- > DOM Clobbering is a technique where global variables can be overwritten or "clobbered" by naming HTML elements with certain IDs or names. This can cause unexpected behavior in scripts and potentially lead to security vulnerabilities. e.g. ```<form id=x><output id=y>I've been clobbered</output><scriptalert(x.y.value);</script>``` 
- [Insecure Deserilization](https://github.com/swisskyrepo/PayloadsAllTheThings/tree/master/Insecure%20Deserialization)
	- > Serialization is the process of turning some object into a data format that can be restored later. People often serialize objects in order to save them for storage or to send them as part of communications. Deserialization is the reverse of that process -- taking data structured from some format, and rebuilding it into an object
- [IDOR](https://github.com/swisskyrepo/PayloadsAllTheThings/tree/master/Insecure%20Direct%20Object%20References)
	- > Insecure Direct Object References occur when an application provides direct access to objects based on user-supplied input. As a result of this vulnerability, attackers can bypass authorization and access resources in the system directly, for example, database records or files.
- [LDAP Injection](https://github.com/swisskyrepo/PayloadsAllTheThings/tree/master/LDAP%20Injection)
	- > LDAP Injection is an attack used to exploit web-based applications that construct LDAP statements based on user input. When an application fails to properly sanitize user input, it's possible to modify LDAP statements using a local proxy.
- [Mass Assignment](https://github.com/swisskyrepo/PayloadsAllTheThings/tree/master/Mass%20Assignment)
	- > A mass assignment attack is a security problem occurred when a user is able to change things they're not supposed to, like their own permissions or admin status. E.g. Modifying request by adding ```isAdmin:true```
- [Open Redirect](https://github.com/swisskyrepo/PayloadsAllTheThings/tree/master/Open%20Redirect)
	- > Happen when a website lets unsafe input decide where users go. Bad actors can use this to send users to fake sites, steal logins, or access restricted parts of the site. 
- [Race Condition](https://github.com/swisskyrepo/PayloadsAllTheThings/tree/master/Race%20Condition)
	- > Race conditions may occur when a process is critically or unexpectedly dependent on the sequence or timings of other events. In a web application environment, where multiple requests can be processed at a given time, developers may leave concurrency to be handled by the framework, server, or programming language.


### 6. File Upload/Download-Based Attack
- [Insecure File Upload](https://github.com/swisskyrepo/PayloadsAllTheThings/tree/master/Upload%20Insecure%20Files)
	- > Uploaded files may pose a significant risk if not handled correctly. A remote attacker could send a multipart/form-data POST request with a specially-crafted filename or mime type and execute arbitrary code.
- [CSV Injection](https://github.com/swisskyrepo/PayloadsAllTheThings/tree/master/CSV%20Injection)
	- > Many web applications allow the user to download content such as templates for invoices or user settings to a CSV file. Many users choose to open the CSV file in either Excel, Libre Office, or Open Office. When a web application does not properly validate the contents of the CSV file, it could lead to the contents of a cell or many cells being executed.
- [LaTex Injection](https://github.com/swisskyrepo/PayloadsAllTheThings/tree/master/LaTeX%20Injection)
 	- > LaTeX is a typesetting system commonly used for creating documents that require complex formatting containing mathematical equations, scientific notation, tables, and references. LaTeX uses plain text input with markup commands to describe the structure and formatting of the document. The LaTeX system then processes this input and generates high-quality output, typically in ```PDF format```.


### 7. Database Specifically based attack:
- [SQLI](https://github.com/swisskyrepo/PayloadsAllTheThings/tree/master/SQL%20Injection)
	- > A SQL injection attack involves inserting malicious SQL queries through client input to achieve goals such as information leakage, data disclosure/manipulation, and bypassing authorization controls.
- [NoSQL Injection](https://github.com/swisskyrepo/PayloadsAllTheThings/tree/master/NoSQL%20Injection)
	- > NoSQL databases provide looser consistency restrictions than traditional SQL databases. By requiring fewer relational constraints and consistency checks, NoSQL databases often offer performance and scaling benefits. Yet these databases are still potentially vulnerable to injection attacks, even if they aren't using the traditional SQL syntax.
- XML-Based Attack
	- [XPATH Injection](https://github.com/swisskyrepo/PayloadsAllTheThings/tree/master/XPATH%20Injection)
	- [XSLT Injection](https://github.com/swisskyrepo/PayloadsAllTheThings/tree/master/XSLT%20Injection)
	- [XXE](https://github.com/swisskyrepo/PayloadsAllTheThings/tree/master/XXE%20Injection)


### 8. [Account Takeover](https://github.com/swisskyrepo/PayloadsAllTheThings/tree/master/Account%20Takeover)
> In this attack, the attacker aims to gain access to a victim's account by circumventing authentication mechanisms and security measures, essentially "taking over" the account as if they were the legitimate user via various methods.<br/>
- [Cool](https://anugrahsr.github.io/posts/10-Password-reset-flaws/)

### 9. Language Specifically based attack:
- PHP
	- [TypeJuggling](https://github.com/swisskyrepo/PayloadsAllTheThings/tree/master/Type%20Juggling)
 		- > PHP is a loosely typed language, which means it tries to predict the programmer's intent and automatically converts variables to different types whenever it seems necessary. For example, a string containing only numbers can be treated as an integer or a float. However, this automatic conversion (or type juggling) can lead to unexpected results, especially when comparing variables using the '==' operator, which only checks for value equality (loose comparison), not type and value equality (strict comparison).


### 10. Product-Based Specific Injection
- [GraphQL Injection](https://github.com/swisskyrepo/PayloadsAllTheThings/tree/master/GraphQL%20Injection)
- [See more..](https://github.com/swisskyrepo/PayloadsAllTheThings/tree/master/CVE%20Exploits)


### 11. WAF/Blacklist Bypass
- [Parameter Pollution](https://github.com/swisskyrepo/PayloadsAllTheThings/tree/master/HTTP%20Parameter%20Pollution)


### 12. Source-code manager attack
- [git](https://github.com/swisskyrepo/PayloadsAllTheThings/tree/master/Insecure%20Source%20Code%20Management)
	- > The following examples will create either a copy of the .git or a copy of the current commit.
	- > Check for the following files, if they exist you can extract the .git folder.
		- ```.git/config```
		- ```.git/HEAD```
		- ```.git/logs/HEAD```
 
### 13. Prompt Based Injection:
- [jailbreak chat](https://www.jailbreakchat.com/)

 
