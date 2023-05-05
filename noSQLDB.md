To store unstructure data.

RDBMS - in future if table structure has to be changed, new col has to be added then it is a huge amount iof work, we have to recreate schema.
update older fields with dummy or default data. Lots of joins required to fetch data from tables. Joins are slow when run on more data.
we create index to improve data fetching
- designed for verticle scaling
- horizontal scaling is not possible as joins b/w diffrenet are not possible
- need ORM- object relation map to convert row col to objects(some latency added)
- ACID properties - atomicity, consistentcy, isolation, durability


No SQL - Changes/updation can be handeled in no sql can be handeled easily
- has dynamic schema
- schema are defined in middleware
- provides horizontal scaling
- does not need ORM as data is in json format
- BASE properties - basically available, soft state, evantually consistent
