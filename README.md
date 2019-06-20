# Tips and Tricks
+++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

Run MongoDB with replSet 

> sudo mongod --port 27017 --dbpath ./data --replSet rs0

Open another terminal 

> $ mongo --eval 'rs.initiate();'

+++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

MongoDB is running on localhost but not connected with other system on same network 

For that you need to bind IP

> sudo mongod --port 27017 --dbpath ./data --replSet rs0 --bind_ip 0.0.0.0

+++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

// Get Running Node Process 
> ps -aef | grep node

// Search by nested json object and display specific field
> db.getCollection('gamelogs').find({"body.UserId":"Xhr2LAvXMreP8fqrpqBs6aDAuoF2"}, {"body.Data.eventcount" : 1})
