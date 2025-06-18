## Set operator
1. When we want to modify a document field we use Set operator. This can be used in multiple ways.
2. Lets start with simple one. When I tried modifying the name inside a document, How I did it:
```
	Initial Data:
	{{
        "interviews": [],
        "_id": "66507320e4b8bbafe8d0598a",
        "name": "Valentine Hopper",
        "college": "Sed molestiae fuga ",
        "status": "not_placed",
        "dsaScore": 4,
        "webDScore": 92,
        "reactScore": 94,
        "__v": 0,
        "results": []
    }, ... }

	MongoDB Query to update the name of a document
	db.collection.findOneAndUpdate({_id: studentId}, {
		$set: {
			'name': studentChanges.name;
		}
	})

	What this is doing? first finding the id using first filteroption of function, then setting the name value to something required changes using $set operator.
```