
GraphQL It is query languague for api's and apollo server is implementation of graphQL

# Triditional approach

web + mobile -> rest api calls -> get response back

rest api intract with db and does operation

__cons__
1) multiple network calls
2) overfetching and under fetching of data
3) more bandwidth comsumption as unwanted data is sent to clinet too
4) custom api to get desired query response

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



**Caching Strategy in apolloclient**

apollo client caches data by default. one can specify fetchPolicy to cache-only, cache-and-network, network-only, no-cache

cache-first - make query -> if response is cached then return that, if not cached then hit api and get data and cache it n then return to the user.
cache-and-network -> make query -> if response is cached then use it but still make api call to get latest data
network-only - make query -> api call -> update cache -> return response

no-cache - just like network but does not update cache
cache-only- no req to api just calls cache and return data from cache if found/not

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


use InMemoryCache in apollo client to cache the results of queries.
in case you always to fetch real time data then set Fetchpolicy as 'network-only'

use apolloClinet.query or apolloclient.mutate to get or add records

Data can be writted directly to apollo client cache.

apolloClinet.mutate({
mutation,
variables:{ input: {title,description }},
update: (cache, {data}) => {
  cache.writeQuery({
    query: add gql query here,
    variables: pass any variables if needed,
    data
  
  });
}



use UseQuery and useMutation Hooks for get and put actions.

useQuery accept query and variable object and returns data, loading and error.

useMutation accept mutation and returns function, loading,error. returned function has to be called onSubit, onClick actions etc.
