# MongoDB
MongoDB is a flexible document database.

## Authentication
When using MongoDB on a (multi-user) cluster authentication has to be enabled.

1. Start mongodb:
   ```bash
   mongod --port 27017 --dbpath /path/to/db
   ```

2. Connect to mongo shell:
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
```
