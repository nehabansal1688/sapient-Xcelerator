
GraphQL It is query languague for api's and apollo server is implementation of graphQL

# Triditional approach

web + mobile -> rest api calls -> get response back

rest api intract with db and does operation

__cons__
1) multiple network calls
2) overfetching and under fetching of data
3) more bandwidth comsumption as unwanted data is sent to clinet too

# using GraphQL
1) enable user to fetch only required data with whatsoever shape they want with statically defining the type
2) faster than restAPI
3) It handle data transformation(eg db return text and ui needs it in compoText)
4) we can get result from multiple api's in just one call i.e. get posts, get users, get all can be clubbed and replaced with just one n/w call
5) Apollo server helps in managing graph ql, defining type def, defining schema, host graphs on node js, gives capability to host node.






10) apollo server takes two argument - type defination and resolver
11) Resolvers - what should query returns. For every qyery there has to be a resolver. type def name has to be same that of resolver
12) Create server.js and add typedef and resolver and run using node server.js
13) all query types wil be post, content type will be application-json


* graph ql provides scaler(int, float, string, boolean, ID- GUID, list, enum, array, ) and custom type data

type query {
  hello: string!
 }
 ! here marks as it cannot be null()mandatory field)
 
 
 * apollo server ships diff packages for express, next, nest etc.
 * apollo server can be run on top of express by using apolloSevr. applymiddleware(appServer)
 * queries can be parametried using variables
 
 
 __Mutations__
 mutations are for write operations.  
 use below to declate mutations and implemenattion muattaion inside resolver object
 type Mutations {
 addCompany(input:createInoputCompany):Company
 }
 
input createInputCompany {
name: string!
description: string}


__mutation in resolver__

Mutation{
addCompany: async(root, {input}) => {

//add logic to craate new record
return company
}
