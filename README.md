I have used https://ethereal.email/ for sending verification link and Reset Pin. I have provided the email and password yopu can login and check the data.

Here I have provided all the instruction which one can use this api to check it on POSTMAN. I would request to change the mongoDB url with your own database url so that you can check or verify the data of database.





################## User sing up endpoint########################
POST http://localhost:3001/v1/user
Content-Type: application/json

{
    "name": "SHIVAM",
    "company": "ON8",
    "address": "DELHI",
    "phone": "9430611398",
    "email": "sh@gmail.com",
    "password": "Shivam@2312"
}


################ Verify User##########################
PATCH: http://localhost:3001/v1/user/verify
Content-Type: application/json 

{
    "_id": "6131cd1d807c111860ce35d5",
    "email": "sh@gmail.com"
}

########################### User sing in endpoint##########################
POST http://localhost:3001/v1/user/login
Content-Type: application/json 

{
     "email": "sh@gmail.com",
    "password": "Shivam@2312"
}

############## Password reset request endpoints #####################
POST http://localhost:3001/v1/user/reset-password
Content-Type: application/json 

{
    "email": "sh@gmail.com"
}

############### Update new password endpoint#####################
PATCH  http://localhost:3001/v1/user/reset-password
Content-Type: application/json 

{
    "email": "sh@gmail.com",
    "pin": "874556",
    "newPassword": "Shivam@9135"
}


##################user logout endpoint ####################
DELETE http://localhost:3001/v1/user/logout
Authorization: eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJlbWFpbCI6ImUyQGUuY29tIiwiaWF0IjoxNjA5NjcyNzE0LCJleHAiOjE2MDk3NTkxMTR9.suW36ge23AtBke_-IG8gQOZEuUw_GxbqL177GzEmytM
 


###Token routers
### Get refreshed token
GET http://localhost:3001/v1/tokens
Authorization: eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJlbWFpbCI6ImUyQGUuY29tIiwiaWF0IjoxNjA5NjY5NDcwLCJleHAiOjE2MTIyNjE0NzB9.C92NUOBb-MmyOx2Ipw-w-BjEafSuCot83Cwl3Bmr8Oc


