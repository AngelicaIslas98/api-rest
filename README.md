# API REST

This API contains different routes to obtain information about a movie application. The information provided includes: title, director, year of release, and rating. Additionally, a connection to an external API was generated to simulate a route for users.

The API allows the use of GET, POST, PUT, and DELETE methods. No client or web application was created, instead a program was used to simulate client application requests.

# System Configuration
- Visual Studio Code
- Node JS
- Postman
- JSON Viewer (browser extension)

Postman Link
(https://blue-star-689981.postman.co/workspace/Team-Workspace~a50bffa0-5f87-4fb3-8347-a5a5d776647d/collection/25919009-ad4bf487-0cc0-4ed6-8cd0-90f7d031b227?action=share&creator=25919009 "Share API's Prueba Postman")

# Dependencies
Creation of JSON package

`npm init -y`

# Modules

Node framework

`npm i express`

Module that allows the display of requests in the console

`npm i morgan`

# Used Libraries

`npm i underscore`

`npm i node-fetch`

# Accessing Routes

### **GET Method.**
Obtain the information of the route

- test route
http://localhost:3000/test
We will receive a text in JSON format.

- movies route
http://localhost:3000/api/movies

`{`

`"title": "Alien",`

`"director": "James Cameron",`

`"year":"1986",`

`"rating":"8.5"`

`}`

# Using Postman

Header: Content-Type
Value: application/json
Body: "raw"

### **POST Method**
Select POST method, place url http://localhost:3000/api/movies

From "body" we write the data that will be sent to the route. The data sent must include:

-Title

-Director

-Year

-Rating

If not all the data is sent, an error message will be received.


### **PUT Method**
Select PUT method, place url http://localhost:3000/api/movies/:id
In "/:id" the movie ID to be updated will be sent. With underscore, the array of movies will be iterated to search for the ID match and update the data.


### **DELETE Method**
Select DELETE method, with url http://localhost:3000/api/movies/:id
In /:id, "1,2,3..." will be sent as the ID of the movie to be deleted. With underscore, the array of movies will be iterated to search for the ID match and delete it.

# Requesting data from another REST API
Through the GET method with url http://localhost:300/api/users, we will obtain a JSON format array from an external API."
