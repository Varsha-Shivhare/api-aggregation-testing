# Aggregation Test API

[Introduction](https://documenter.getpostman.com/view/1522130/RWaHw8gN#intro)

## API implementation

A web API defines the resources, relationships, and navigation schemes that are accessible to client applications. When you implement and deploy a web API, you should consider the physical requirements of the environment hosting the web API and the way in which the web API is constructed rather than the logical structure of the data. This guidance focusses on best practices for implementing a web API and publishing it to make it available to client applications.

Consider the following points when you implement the code to handle requests:

* POST, GET, and PATCH actions should be unchanged or idempotent

* The code that implements these requests should not impose any side-effects. The same request repeated over the same resource should     result in the same state. 

* POST actions that create new resources should not have unrelated side-effects

* If a POST request is intended to create a new resource, the effects of the request should be limited to the new resource.

* Support content negotiation

* The body of a response message may contain data in a variety of formats.

**Following are the steps to query the data:**

1. POST [add user](https://documenter.getpostman.com/view/1522130/RWaHw8gN#a89157ce-0efa-c5bf-a9cf-9a4db8fdac7b): Add a user to a company

```
  http://localhost:3000/user

```
![image](https://user-images.githubusercontent.com/50067937/56867872-b1654f00-6a08-11e9-9697-617af45801d5.png)


2. POST [add company](https://documenter.getpostman.com/view/1522130/RWaHw8gN#32777c12-5522-7c52-8bc4-4e3265f21216): Add a company

```
  http://localhost:3000/company

```
![image](https://user-images.githubusercontent.com/50067937/56867891-fdb08f00-6a08-11e9-8d51-2305fdab6ab8.png)

3. POST [add lesson](https://documenter.getpostman.com/view/1522130/RWaHw8gN#df2e9395-4b89-4e57-f401-00263c6da9a6): Add a lesson for the company

```
  http://localhost:3000/lesson

```
![image](https://user-images.githubusercontent.com/50067937/56867900-33557800-6a09-11e9-88d1-f0cf2c7da5a1.png)

4. POST [assign lesson](https://documenter.getpostman.com/view/1522130/RWaHw8gN#671a2bac-f03f-fb90-7163-570a52bee067): Assign a lesson to the user

```
  http://localhost:3000/assignLessonToUser

```
![image](https://user-images.githubusercontent.com/50067937/56867913-5ed86280-6a09-11e9-8871-0706a6c2f902.png)

5. GET [welcome](https://documenter.getpostman.com/view/1522130/RWaHw8gN#74eee613-6325-5a29-fc6d-e75ba4618561): The default API health test

```
 http://localhost:3000/
 
```
![image](https://user-images.githubusercontent.com/50067937/56867937-8f200100-6a09-11e9-874d-d8b1ba47af07.png)

6. GET [completion percentage](https://documenter.getpostman.com/view/1522130/RWaHw8gN#e3ac3800-98df-95ba-4a82-0fdf16fccc2c): Divides total number of user assigned a lesson and how many have finished to determine the participation percentage

```
  http://localhost:3000/completionPercentage/MSFT

```
![image](https://user-images.githubusercontent.com/50067937/56867951-b2e34700-6a09-11e9-9287-0a8c2749dc3d.png)

7. PATCH [start lesson](https://documenter.getpostman.com/view/1522130/RWaHw8gN#ad0afb14-5ab2-0331-7fe9-0e400ffbdb70): Starts a lesson for a user

```
  http://localhost:3000/startLesson

```
![image](https://user-images.githubusercontent.com/50067937/56867962-d27a6f80-6a09-11e9-83c0-838fbfabb3af.png)

8. PATCH [end lesson](https://documenter.getpostman.com/view/1522130/RWaHw8gN#87e1dda5-640c-0890-f96e-0e9e13cac4b4): Ends a lesson for a user:

```
  http://localhost:3000/endLesson
  
```
![image](https://user-images.githubusercontent.com/50067937/56867981-005fb400-6a0a-11e9-806c-0f7d95d9d4c4.png)

9. GET [percentage pending](https://documenter.getpostman.com/view/1522130/RWaHw8gN#d47100a1-a34e-460e-47f8-903f3172288c): Divides total number of user assigned a lesson and how many have not finished to determine the pending percentage

```
  http://localhost:3000/pendingPercentage/MSFT

```
![image](https://user-images.githubusercontent.com/50067937/56867993-22593680-6a0a-11e9-8c4e-999f399136d8.png)

10. GET [participation percentage](https://documenter.getpostman.com/view/1522130/RWaHw8gN#542722e2-1eb1-96e0-863e-e636cb58ea08): Divides total number of user assigned a lesson and how many have started to determine the participation percentage

```
  http://localhost:3000/participationPercentage/MSFT

```
![image](https://user-images.githubusercontent.com/50067937/56867998-2e44f880-6a0a-11e9-94f0-a6f9cd2f8d99.png)

## API implementations - including request and response parameters

**Request parameter:**

| Parameter        | Description                                           |
|------------------|-------------------------------------------------------| 
| ` api_key `      |   The public API key                                  |
| ` request_token `| Te one time token obtained after the login flow. This token's lifetime is only a few minutes nd it is meant to be exchanged for an access_token immediately after being obtained             |
| ` checksum `     | SHA-256 hash of (api_key + request_token + api_secret)|


**Request attribute:**

| Attribute           | Type            | Description                                                                                                                                                            |
|---------------------|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------| 
| ` user_id `         | String          |The unique, permanent user ID registered with the broker and the exchanges                                                                                              |
| ` user_name `       | String          |User's real name                                                                                                                                                        |
| ` user_shortname `  | String          | Shortened verion of the user's real name                                                                                                                                |
| ` email `           | String          |User's email                                                                                                                                                            |

## Another important referances

* [Get Postman](https://www.getpostman.com/collection)

* [Get Started with Postman](https://learning.getpostman.com/getting-started/)

* [Postman Concepts](https://learning.getpostman.com/concepts/)

