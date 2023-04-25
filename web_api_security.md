
Security is one of NFR's(non functional requirement) apart from performance,accesibility, SEO.

__Security prinipal__
1) zero trust - all users shd be authorized and authenticated.
2) least priviledge - give access to resources depending upon type of user and its access.
3) Defence in Depth - multipl layers of sceurity - use waf(web application firewall) for entring into cloud, multi factor authentication.
4) Simpler is secure - system shd be less complex so that it can be protected easily.
5) minimize attack surface area - remove app which you are not using in the system.
6) security is obscurity - give only required info to user without exposing internal details. error response and heade shd nt reveal unwanted info


# Types of security attack
1) XSS - cross site scripting 
    a) stored/persisted xss - script is stored in db and once it is injected then it affects multiple users , important to sanitize/validate inputs before        storing it in db
    b) reflected xss - script is not stored in db. example - search input , added script in search and same is executed on client. important to use                escaping
    c) DOM based xss - url query param script injection - important to escape
    
    **Prevention of XSS**
    a) santize all inputs
    b) escape values
    c) use innerText instead of inerHTML as innertext does auto escape
    d) use DOMpurify or other tools - to sanitize before rendering inerhtml
    e) use HTTPOnly cookies as it cane be then read by js
    f) 
3) Click Jacking - user might be clicking on iframe which looks like it belongs to site but it was malicious link
   **Prevention**
   a) use CSP - content sceurity policy 'frame-ancestor: none' - avoid loading page in iframe
   b) x frame options - http response header - deny or same origin
   
4)  Type squatting
5)  DDOS
6)  REDOS - reg ex denial of service
7)  SQL injection
8)  CSRF - cross site request forgery
9)  
