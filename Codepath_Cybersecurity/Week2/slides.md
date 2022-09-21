# Week 2 Slide Notes

## OSI and TPC Model

OSI Model Layers

- Application
- Presentation
- Session
- Transport Network
- Data Link
- Physical

TCP/IP Model Layers

- Application
  - HTTP
  - SMTP
  - DNS
  - RIP
- Transport
  - TCP (Reliable)
  - UDP (Unreliable)
- Internet
  - IPv4
  - IPv6
- Network Interface
  - Ethernet
  - Wireless
  - Frame Relay
  - ATM

## Very Simplified Network Model

## Cookie Session and CSRF

Cookies - small pieces of data that web server asks client's web browser to store, files left on client machine sent by server to look at what is going on before  
Sessions = alternative to cookies, instead of sending key/value pairs to the browser, these values are stored on the server, and only a reference identifier ("session ID") is sent to the user's browser as a cookie  
Cross-site request forgery = attack that user is tricked to perform actions on another site by inadvertently clicking a link or submitting the form : Phishing

## Background

Connectionless Protocol  
Stateless Protocol  

- do not maintain any information about the previous communication
- web server can't tell if the two requests are from the same client/browser or multiple browsers

Can deliver any type of data  
HTTP = stateless protocol


## HTTP Message

HTTP Request
![HTTP Request](../screenshots/Screen%20Shot%202022-09-14%20at%2010.07.40%20PM.png)
HTTP Messege
![HTTP Response](../screenshots/Screen%20Shot%202022-09-14%20at%2010.07.15%20PM.png)

## Key Value Pair

200 OK - request suceeded
404 - not found

## Cookies and Sessions

