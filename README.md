# Social-Network-API

## Description:
This assignment was designed to create and demonstrate a social network api. This is a set of API for a social network that uses a MongoDB database so that the website can handle large amounts of unstructured data, Express.js for routing, Mongoose ODM, and the moment package to format time stamps.

 ## Table of Contents:  
[1. Description](#Description)  
[2. Acceptance Criteria](#Acceptance-Criteria)  
[3. Walkthrough Videos](#Walkthrough-Videos)  
[4. Installation](#Installation)  
[5. Tests](#Tests)  
[6. License Details](#License-Details)  
[7. Submission](#Submission)   
[8. Questions](#Questions)  

## Acceptance Criteria:

- When you enter the command to invoke the application then the server is started and the Mongoose models are synced to the MongoDB database.  
- Testing API POST, PUT, and DELETE routes in Insomnia Core are able to successfully create, update, and delete users and thoughts
- Testing API POST and DELETE routes in Insomnia Core are able to successfully create and delete reactions to thoughts and add and remove friends to a user’s friend list.

## Walkthrough Video
[Walkthrough Demo](https://youtu.be/Az0YOhdVFVo)

## Installation:

There are some simple steps when starting this API.
This repo is not to be deployed, if you wanted to, you could by doing the following:  
- Download the repo files from the link below
- You must have mongoDB installed
- Run the following at the command line
```
    - npm init -y
    - npm install express
    - npm install mongoose
    - npm install moment
```
- Start the server
```
    $ npm start
```
- Open Insomnia Core to test API routes

## Tests:  

Testing restful API calls with Insomnia Core  

---
**`/api/users`**
* `GET` all users
* `POST` a new user:
    ```json
    // example data
    {
        "username": "johnwick",
        "email": "johnwick@gmail.com"
    }
    ```
---
**`/api/users/:userid`**
* `GET` a single user by its `_id` 
* `PUT` to update a user by its `_id`
* `DELETE` to remove user by its `_id`
---
**`/api/users/:userId/friends/:friendId`**
* `POST` to add a new friend to a user's friend list
* `DELETE` to remove a friend from a user's friend list
---
**`/api/thoughts`** 
* `GET` to get all thoughts
* `POST` to create a new thought
    ```json
    // example data
    {
    "thoughtText": "Here's a cool thought...",
    "username": "johnwick",
    "userId": "5edff358a0fcb779aa7b118b"
    }
    ```
---
**`/api/thoughts/:thoughtId`**
* `GET` to get a single thought by its `_id`
* `PUT` to update a thought by its `_id`
* `DELETE` to remove a thought by its `_id`
---

**`/api/thoughts/:thoughtId/reactions`**

* `POST` to create a reaction 
    ```json
    // example data
    {
    "reactionBody":"Hell Yeah!!",
    "username":"johnwick"
    }
    ```
---
**`/api/thoughts/:thoughtId/reactions/:reactionId`**
* `DELETE` remove a reaction by the `reactionId` 

## License Details: 
 This project is under no license.  

## Submission:
 [Github repository](https://github.com/sultansiddiqi)

## Questions:
 Here is a link to my github:  
https://github.com/sultansiddiqi  
 Email me at:  
sultan.siddiqi@gmail.com
for additional questions

