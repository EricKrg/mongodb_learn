# CRUD in MongoDB

- **Databases > Collections > Documents**
	- all of the above are created implicitlyi/on demand
	- if a db/coll./doc is not created yet, it gets created if called

### Create Data 

- switch to db  
	` use test-db`
- insert a **single doc** to collection
	`db.testCollection.insertOne({test: 1})`

- insert with **custom id** (has to be unique and on field `_id`)
	`db.testcollection.insertOne({test:2, _id:2})`

- insert **multiple docs** to a collection

	```
		
	```

### Read

### Update

- update a **single doc** :
	`db.flightData.updateOne({"distance":1200}, {$set: {"marker": "del"}})`
	- updates the first matching flightData.doc  --> updateOne({FILTER}, {UPDATE}) 
	- `$set` --> sets new field/obj, mongo reserved if starting with $
- update **multiple docs**:
	`db.flightData.updateMany({}, {$set: {"marker":"toDelete"}})`
	- {} as filter selects all docs

### Delete

- delete a single document
	`db.flightData.deleteOne({"departureAirport":"FRA"})`
	- deletes the first document with matching departureAirport

- delete **multiple docs** in a collection


- delete **all docs** of an collection, **without filter**:
	`db.flightData.deleteMany({})`

	
