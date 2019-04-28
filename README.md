# Aggregation Test API

[Introduction](https://documenter.getpostman.com/view/1522130/RWaHw8gN#intro)

## API implementation

A web API defines the resources, relationships, and navigation schemes that are accessible to client applications. When you implement and deploy a web API, you should consider the physical requirements of the environment hosting the web API and the way in which the web API is constructed rather than the logical structure of the data. This guidance focusses on best practices for implementing a web API and publishing it to make it available to client applications.

Consider the following points when you implement the code to handle requests:

* POST, GET, and PATCH actions should be unchanged or idempotent

    The code that implements these requests should not impose any side-effects. The same request repeated over the same resource should     result in the same state. 

* POST actions that create new resources should not have unrelated side-effects

    If a POST request is intended to create a new resource, the effects of the request should be limited to the new resource.

* Support content negotiation

    The body of a response message may contain data in a variety of formats.

**Following are the steps to query the data:**

1. POST [add user](https://documenter.getpostman.com/view/1522130/RWaHw8gN#a89157ce-0efa-c5bf-a9cf-9a4db8fdac7b): Add a user to a company

```
  http://localhost:3000/user

```
<a>img src="C:\Users\VARSHA SHIVHARE\Desktop\api_test\1.jpg" alt="Internet of Things Programming Projects" height="256px" align="right"></a>

2. POST [add company](https://documenter.getpostman.com/view/1522130/RWaHw8gN#32777c12-5522-7c52-8bc4-4e3265f21216): Add a company

```
  http://localhost:3000/company

```
3. POST [add lesson](https://documenter.getpostman.com/view/1522130/RWaHw8gN#df2e9395-4b89-4e57-f401-00263c6da9a6): Add a lesson for the company

```
  http://localhost:3000/lesson

```
4. POST [assign lesson](https://documenter.getpostman.com/view/1522130/RWaHw8gN#671a2bac-f03f-fb90-7163-570a52bee067): Assign a lesson to the user

```
  http://localhost:3000/assignLessonToUser

```
5. GET [welcome](https://documenter.getpostman.com/view/1522130/RWaHw8gN#74eee613-6325-5a29-fc6d-e75ba4618561): The default API health test

```
 http://localhost:3000/
 
```
6. GET [completion percentage](https://documenter.getpostman.com/view/1522130/RWaHw8gN#e3ac3800-98df-95ba-4a82-0fdf16fccc2c): Divides total number of user assigned a lesson and how many have finished to determine the participation percentage

```
  http://localhost:3000/completionPercentage/MSFT

```
7. PATCH [start lesson](https://documenter.getpostman.com/view/1522130/RWaHw8gN#ad0afb14-5ab2-0331-7fe9-0e400ffbdb70): Starts a lesson for a user

```
  http://localhost:3000/startLesson

```
8. PATCH [end lesson](https://documenter.getpostman.com/view/1522130/RWaHw8gN#87e1dda5-640c-0890-f96e-0e9e13cac4b4): Ends a lesson for a user:

```
  http://localhost:3000/endLesson
  
```
9. GET [percentage pending](https://documenter.getpostman.com/view/1522130/RWaHw8gN#d47100a1-a34e-460e-47f8-903f3172288c): Divides total number of user assigned a lesson and how many have not finished to determine the pending percentage

```
  http://localhost:3000/pendingPercentage/MSFT

```
10. GET [participation percentage](https://documenter.getpostman.com/view/1522130/RWaHw8gN#542722e2-1eb1-96e0-863e-e636cb58ea08): Divides total number of user assigned a lesson and how many have started to determine the participation percentage

```
  http://localhost:3000/participationPercentage/MSFT

```

###  

