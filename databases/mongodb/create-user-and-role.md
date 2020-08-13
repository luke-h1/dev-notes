## CREATE USER & ADD ADMIN ROLE 
```
db.createUser(
{	user: "lukehowsam",
	pwd: "password",

	roles:[{role: "userAdminAnyDatabase" , db:"admin"}]})
  ```