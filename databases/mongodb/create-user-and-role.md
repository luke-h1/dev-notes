## CREATE USER & ADD ADMIN ROLE 
```
db.createUser(
{	user: "username",
	pwd: "password",

	roles:[{role: "userAdminAnyDatabase" , db:"admin"}]})
  ```
