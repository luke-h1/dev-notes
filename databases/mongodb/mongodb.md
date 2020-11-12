


* create user + add admin role 
```
db.createUser(
{	user: "username",
	pwd: "password",

	roles:[{role: "userAdminAnyDatabase" , db:"admin"}]})
  ```



* local connection string 
```
mongodb://127.0.0.1:27017/<YOUR_DB_NAME> 
```

* find an item in a given collection: 
```
use <DB_NAME>
db.<COLLECTION-NAME>.find('query goes here')

```


* drop a collection 
db.collection-name.drop() 


* If you're on a VPN you will be unable to connect to MongoDB atlas ()
