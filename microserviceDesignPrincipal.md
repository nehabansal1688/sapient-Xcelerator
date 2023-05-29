Monolith arch -> n-tier arch -> micro service arch

monolith
<img width="205" alt="Screenshot 2023-05-08 at 9 02 42 AM" src="https://user-images.githubusercontent.com/11769073/236727875-fc7326f0-7280-493d-afd7-35bcc482c3a9.png">

n tier
<img width="789" alt="Screenshot 2023-05-08 at 9 56 33 AM" src="https://user-images.githubusercontent.com/11769073/236733768-a3c83241-74ac-4a90-9720-fa834485d91f.png">


foor odereing - >

__Monolith__

* Build process takes more time in
* failure in one part , whole build fails
* team size- 6-8 dev then monolith makes more sense

__microservice__
* loosely coupled - can be achieved using message broker - services can comminicate with each other using message broker(kafka redis) 
*   or pub sub models or GRPS (google remote procedure )
* single responsibility 


communication ways
 <img width="847" alt="Screenshot 2023-05-08 at 9 36 05 AM" src="https://user-images.githubusercontent.com/11769073/236731555-a3ca007b-cfeb-4769-bc8c-2aec0050acf9.png">

# Decomposing Microservices - citibank
* business capabilities - banking, credit card, nri account, support, MF & equities
* business domains 
   1) generic  - marketing n HR (doesnt generate any bussiness value) (decision on buy vs build)
   2) core - brad n butter, complete focus should be on developing these
   3) support - doesnt gerenarey bussiness value, (decision on buy vs build), chatbot
* bounded context pattern - based on user stories like i as user should be able to login to system , i as user should be able to add product to cart
* Strangler pattern - take existing monolith and convert it to microservices gradually



Resiliance 

* External config pattern - app config reside somewhere else not in the app itself
  1) keeping var in env files - react
  2) nest js has configService
*  Service Discovery Pattern -  keeping all service config like link to product, shipping service in sds and use that to make api calls
  1) decouple code 
  2) easy to scale, no code change in repo when we have to add new service, we just need to make entry in SDS 
* 
