
It is query languague for api's

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
5) Apollo server helps in managing graph ql, defnening type def, defining schema, host graphs on node js, gives capability to host node.
6) apollo server takes two argument - ype defination and resolver
7) Resolvers - what should query returns. For every qyery there has to be a resolver. type def name has to be same that of resolver
8) Create server.js and add typedef and resolver and run using node server.js
