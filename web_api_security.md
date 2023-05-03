
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


__security prevention by using http headers__
1) X-Frame-Options - DENy or sameorigin
2) X-Content-Type-Options nosniff
3) access-control-allow-origin - server your domain use domainname or self
4) content security policy - we can create policy directives i.e. images will be loaded from 'abc.com', styles will be loaded from 'self'. we can block unwanted images/resources to be downloaded. we can avoid non malicious data on website. 
5) stict transport security - site can only be accessed using https and we can set max-age to 1 year etc


__Securing API's__
1) authuntication and authorization
2) request validation and encryption
3) throtle api request
4) log api activity
5) security tests


__Secure Microservice Architecture__
<img width="936" alt="Screenshot 2023-05-03 at 9 10 50 AM" src="https://user-images.githubusercontent.com/11769073/235828640-dcdb605d-68cc-45e2-8045-abc876dd69f4.png">
<img width="927" alt="Screenshot 2023-05-03 at 9 11 07 AM" src="https://user-images.githubusercontent.com/11769073/235828665-efff6f9f-e587-4e98-8f19-d41b465f2b66.png">


