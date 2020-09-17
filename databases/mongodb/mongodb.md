


* create user + add admin role 
```
db.createUser(
{	user: "username",
	pwd: "password",

	roles:[{role: "userAdminAnyDatabase" , db:"admin"}]})
  ```



* local connect string 
mongodb://127.0.0.1:27017/<YOUR_DB_NAME>