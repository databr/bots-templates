bots-templates
==============

Quick-start Bots templates for multiple programming languages.

# Configuring MongoDB

prompt:~$ sudo mkdir /data/db # used by Mongodb
prompt:~$ sudo apt-get install mongodb # install mongodb
prompt:~$ mongo # test the connection

## Usefull commands on Mongodb:

	show dbs
	use databr 		 // 	switch between databases.
	show collections //     show all the "tables"  
 	
	db.collection.findOne() // 			shows the first document saved on database
	db.collection.find().limit(10) // 	limits the query results
	db.collection.find({}, {some_property : 1}).limit(10) // 	shows only the specified fields
	db.collection.find({"some_property.some_sub_property": some_value}).count() // count all collection from some_value
	
	db.collection.distinct("some_property.some_sub_property") // distinct of a specific field.
	db.collection.distinct("some_property") 
	
	// Mongodb uses a "javascript" interface to access the documents persisted on the database.
	Object.keys(db.collection.findOne()) // shows the fields of a document.

For more informations access the [oficial documentation](http://docs.mongodb.org/manual/core/crud-introduction/)