# MongoDB
MongoDB is a flexible document database.

## Authentication
When using MongoDB on a (multi-user) cluster authentication has to be enabled.

1. Start mongodb server:
   ```bash
   mongod --port 27017 --dbpath /path/to/db
   ```

2. Use different terminal to connect to mongo shell:
   ```bash
   mongo --port 27017
   ```

3. Create user with root role/privileges for all databases:
   ```
   use admin
   db.createUser(
     {
       user: "myuser",
       pwd: "mypass123",
       roles: [ { role: "root", db: "admin" } ]
     }
   )
   ```

4. Stop the original mongodb server (`Ctrl-C`).

5. Restart the mongodb server with enabled authentication:
   ```bash
   mongod --auth --port 27017 --dbpath /path/to/db
   ```

* https://docs.mongodb.com/manual/tutorial/enable-authentication/
* https://docs.mongodb.com/manual/reference/built-in-roles/

## PyMongo
PyMongo is a Python package containing tools for working with MongoDB.
`pymongo` and `mongodb` itself are available in conda.

```python
from pymongo import MongoClient


# Connect to MongoDB instance running on localhost.
client = MongoClient(
    username='myuser',
    password='mypass123',
)
db = client.foo  # database
collection = db.bar # collection


# Insert an object
obj = {
    'name': 'User',
    'email': 'user@domain.de',
}
collection.insert_one(obj)

# Query *one* documents.
collection.find_one({'name': 'User'})

# Query *all* documents.
collection.find({'name': 'User'})
```
