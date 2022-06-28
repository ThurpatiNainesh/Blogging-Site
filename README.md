# TOPIC: Authentication

## Authentication with JWT
- Token generation
- Token verification

## Assignment
- For this assignment you have to create a new branch - assignment/auth-1
- Your user document should look like this
```
 	{
    "_id" : ObjectId("6226e3d2b98f22b349ca58be"),
    "firstName" : "Sabiha",
    "lastName" : "Khan",
    "mobile" : "9898909087",
    "emailId" : "sk@gmail.com",
    "password" : "password123",
    "gender" : "female",
	"isDeleted": false, //default value is false 
    "age" : 12,
    "createdAt" : ISODate("2022-03-08T05:04:18.737Z"),
    "updatedAt" : ISODate("2022-03-08T05:04:18.737Z"),
    "__v" : 0
}
```


- Write a **POST api /users** to register a user from the user details in request body. 
- Write a ***POST api /login** to login a user that takes user details - email and password from the request body. If the credentials don't match with any user's data return a suitable error.
On successful login, generate a JWT token and return it in response body. Example 
```
{
 token: "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJzdWIiOiIxMjM0NTY3ODkwIiwibmFtZSI6IkpvaG4gRG9lIiwiaWF0IjoxNTE2MjM5MDIyfQ.SflKxwRJSMeKKF2QT4fwpMeJf36POk6yJV_adQssw5c"
}
```
- Write a **GET api /users/:userId** to fetch user details. Pass the userId as path param in the url. Check that request must contain **x-auth-token** header. If absent, return a suitable error.
If present, check that the token is valid.
- Write a **PUT api /users/:userId** to update user details. Pass the userId as path param in the url and update the attributes received in the request body. Check that request must contain **x-auth-token** header. If absent, return a suitable error.
- Write a **DELETE api /users/:userId** that takes the userId in the path params and marks the isDeleted attribute for a user as true. Check that request must contain **x-auth-token** header. If absent, return a suitable error.
- Once, all the apis are working fine, move the authentication related code in a middleware called auth.js
- Add this middleware at route level in the routes where applicable.



eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJhdXRob3JJZCI6IjYyYjUyY2FmMjE5OTM5YjQ1YzE1YjkxMiIsImlhdCI6MTY1NjA1MDU2NH0.2w5TgubcyLojDKsN_9WjxGAtSGS-WSHDQEmS91n84Ok{shoeb}

eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJhdXRob3JJZCI6IjYyYjUyY2U3MjE5OTM5YjQ1YzE1YjkxNCIsImlhdCI6MTY1NjA1MTA0Mn0.5afpskjN-O14d8FtocGWVad8_dbtlehB6gcMxbiu3ss{ajay sai}

eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJhdXRob3JJZCI6IjYyYjUyZDE1MjE5OTM5YjQ1YzE1YjkxNiIsImlhdCI6MTY1NjA1MTI0N30.7_R0_ETGzVva2P-XE47j_99xhyqHt-KWg_ri9Ly1irA{manoj kumar}

np{nikhil raj}

eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJhdXRob3JJZCI6IjYyYjUyYzZmMjE5OTM5YjQ1YzE1YjkxMCIsImlhdCI6MTY1NjA1MTY2OX0.9UNkdQYsRULu8VAaoyRFaF_l3GKM2KmmF3kzjs7DK20{nainesh}