# OWASP Top 10  
  
### Broken Access Control  
- Bypass authorization safeguards  
- Become privileged users  
- Ability to expose sensitive data  
- Modify or destroy data  
- Perform any network function  
  
### Cryptographic Failures  
- Failures related to cryptography  
- Failures of secure data transfer  
- Useful post-exploit information  
- Advanced persistant threat  
  
### Injection  
- Introducing hostile code to program  
- Changing program execution  
- By injecting code into a web application, an attacker can steal authentication cookies and use them on other online services  
  
### Insecure Design  
- Solarwinds Supply Chain Attack(?)  
  
### Security Misconfiguration  
- Failure to implement security controls  
- Implementing security controls but with errors  
- Mostly occur due to human errors:  
    - Misinterpreting system implementation  
    - Not changing default login credentials  
    - Lack of computer skills  
    - Mistakes made under time pressure  
  
### Vulnerable & Outdated Components  
- According to OWASP, hard to test for this  
- These components include:  
    - Operating systems  
    - Web/Application servers  
    - Database management systems  
    - APIs
    - And all components, runtime environments and libraries  
- An attacker only needs to find **one** vulnerable component to compromise the system, however, approximately 18,000 vulnerabilities are found each year, which means that protecting against known vulnerabilities will always be an ongoing process  
  
### Identification & Authentication Failures  
- Compromise of:  
    - Passwords  
    - Keys  
    - Session Tokens  
    - User Information  
- Processes like Multi-factor authentication(MFA) are integral in authenticating key user information like usernames and passwords  
  
### Software & Data Integrity Failures  
- Code and infrastructure that does not protect against integrity violations  
- Example, an application using untrusted app plugins  
- Compromised plugin = App access like **Wordpress**  
  
### Security Logging & Monitoring Failures  
- Hard to test for due to a lack of representation in CVE/CSS data  
- Serious impact on:  
    - Visibility  
    - Digital forensics  
  
### Server-side Request Forgery  
- Server functionality abuse causing it to access/manipulate inaccessible info that would otherwise not be directly accessible to the attacker  
