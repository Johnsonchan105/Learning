# Unit 1

Focus  
-web-app security, to and from the browser  
-Offensive security  
-OWASP Top 10 - top 10 of the most common attacks/vunerabilities of web-app

## Week 1 - sensitive data exposure

By the end of the week understand fundamentals

- Burp
- Sensitive Data Exposure
- URL Manipulation and IDOR

Sensitive Data: information meant to be protected from unauthorized acess  
Information Disclosure: organization/website discloses sensitive information of its users unintentionally

Impacting:

- Confidentiality
  - information is not disclosed to unauthorized individuals, processes, or devices
    - threat:
      - data disclosure
      - masquerading
      - priviledge escalation
    - how to achieve
      - access control
      - authentication
      - authorization
      - encryption
      - data minimization
- Integrity
  - protection against unauthorized creation, modification, or destruction of information
    - threat
      - alteration / data modification
    - how to achieve
      - authorization
      - testing and validation
      - monitoring
      - hashing algorithms
      - messege digests
- Availiability
  - timely, reliabile access to data and information services for authorized users
    - threat
      - disruption
      - DOS
    - how to achieve
      - redundancy
      - monitoring
      - incident response capability
      - operational excellence

CIA triad

Acess Control

- fundamental component of data security that dictates who's allowed to access and use company information and resources
- 

access control types

- Discretionary Acess Control (DAC)
  - done by security admin, owner of data defines rules and controls access
- Mandatory Access Control 
- _
- _

implement access control based on:

- Authentication
  - identifies users
  - confirms they are who they say they are
- Session Management
  - identifies which subsequent HTTP requests are being made by that same user
- Access control
  - determines whether the user is allowed to carry out the action that they are attempting to perform

Sensitive Data Exposure : application, company, or other entity inadvertently exposes personal data

- information
  - credit card data
  - medical history
  - session tokens
  - or other authentication credentials
- most common flaw is failing to encrypt data

Insecure Direct Object Reference (IDOR) : type of access control vulnerbility that arises when an application uses user-supplied input to access objects directly

- allows attackers to bypass authorization and access resources in the system directly, for example database records or files
- allows attackers to bypass authorization and access resources directly by modifying 
- _
- _
- _

changing url allows you to access documents that you are not supposed to  
involves session management ___  

IDOR Types:

- Body manipulation
  - modify value ot checkbox, radio buttons, and form fields. allows attackers to access information from other users with ease
- URL Tampering
  - _

Sensitive Data Exposure Mitigation:

- Data classification
- Encrypt the data at rest and data in motion
- use strong ciphers
- alert on errors
- auditing
- gather only required data

IDOR Mitigation

- change direct reference to indirect reference
- authorization and access control
- _
- _
- alerts - log access control failures, alert admins when appropriate (e.g. repeated failures)
- Indirect Object Reference: _

