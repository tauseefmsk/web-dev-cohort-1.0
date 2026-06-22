### 1. **Introduction to Node.js – The Power of JavaScript on the Server**

- What is Node.js and how it differs from traditional server-side languages
- Understanding the Node.js runtime environment
- The event-driven, non-blocking I/O model in Node.js
- Setting up a simple Node.js application
- Installing and using Node.js with npm (Node Package Manager)
- **Key Concepts:** Event-driven architecture, Non-blocking I/O, npm, Modules

### 2. **Understanding the Event Loop – Node.js Architecture**

- What is the event loop and how does Node.js handle concurrency
- How Node.js uses the event loop to process requests asynchronously
- Blocking vs Non-blocking code execution
- The importance of callbacks and promises in managing asynchronous code
- **Key Concepts:** Event loop, Asynchronous processing, Callbacks, Promises

### 3. **Creating a Basic HTTP Server**

- How to create a basic HTTP server with Node.js using the `http` module
- Setting up routes to handle different HTTP requests (GET, POST, PUT, DELETE)
- Sending and receiving data with the server
- Working with request and response objects
- **Key Concepts:** HTTP server, Request/Response objects, Routing

### 4. **Express.js – Simplifying Backend Development**

- Introduction to Express.js and how it simplifies Node.js backend development
- Setting up an Express app and defining routes
- Handling dynamic data with URL parameters and query strings
- Middleware in Express: What is middleware and how to use it
- Built-in Express middleware functions (e.g., body-parser, cookie-parser)
- **Key Concepts:** Express.js, Routing, Middleware, Request handling

### 5. **RESTful API Design – Building APIs with Express**

- What is a RESTful API and how to structure it
- Designing endpoints and handling HTTP methods (GET, POST, PUT, DELETE)
- Using query parameters and request bodies for passing data
- Returning JSON data and handling status codes in API responses
- **Key Concepts:** REST API design, CRUD operations, Status codes, JSON responses

### 6. **Working with Databases – Connecting Node.js to Databases**

- Introduction to databases (SQL vs NoSQL)
- Using MongoDB with Node.js (Setting up MongoDB, connecting via Mongoose)
- Working with CRUD operations in MongoDB (Create, Read, Update, Delete)
- Introduction to SQL databases (using MySQL/PostgreSQL with Node.js)
- Using ORMs (Object Relational Mappers) like Drizzle, Prisma to interact with SQL databases
- **Key Concepts:** MongoDB, SQL, NoSQL, CRUD, Mongoose, Sequelize, ORMs

### 7. **Authentication and Authorization – Securing Your Application**

- Introduction to user authentication and authorization concepts
- Using JWT (JSON Web Tokens) for stateless authentication
- Setting up user login and registration endpoints
- Password hashing with bcrypt.js
- Role-based access control and securing routes with middleware
- **Key Concepts:** Authentication, Authorization, JWT, bcrypt, Role-based access control

### 8. **Working with File Systems – Reading and Writing Files**

- Introduction to the Node.js `fs` module for file system operations
- Reading files asynchronously and synchronously
- Writing files to the server’s file system
- Handling file uploads (e.g., using `multer` for handling multipart forms)
- **Key Concepts:** File system module, File reading/writing, File uploads

### 9. **Building Real-time Applications – WebSockets with Socket.io**

- What are WebSockets and how they enable real-time communication
- Setting up a WebSocket server using the `ws` module or Socket.io
- Sending and receiving real-time data between the client and server
- Use cases for real-time apps (e.g., chat applications, live notifications)
- **Key Concepts:** WebSockets, Real-time communication, Socket.io

### 10. **Deploying Your Node.js Application**

- Introduction to deployment options for Node.js applications
- Deploying Node.js apps on cloud platforms (Heroku, AWS, DigitalOcean, etc.)
- Setting up environment variables for different environments (production, development)
- Configuring reverse proxies with Nginx or Apache
- **Key Concepts:** Deployment, Cloud services, Reverse proxies, Environment variables

### 11. **API Rate Limiting – Protecting Your Endpoints**

- What is API rate limiting and why it's important
- Implementing rate limiting to prevent abuse of your APIs (e.g., using `express-rate-limit`)
- Configuring custom rate limiters for different endpoints
- Handling rate limit exceeded errors and responses
- **Key Concepts:** Rate limiting, Throttling, API protection, express-rate-limit

### 12. **Logging & Monitoring – Tracking Application Health**

- Introduction to logging and monitoring in Node.js applications
- Using logging libraries like Winston and Morgan for structured logging
- Setting up logging levels (info, warn, error) and storing logs in files or external services
- Integrating monitoring tools like PM2 for process management and performance monitoring
- **Key Concepts:** Logging, Winston, Morgan, PM2, Monitoring, Application health

### 13. GraphQL

- **Introduction to GraphQL**
    - What is GraphQL and how it differs from REST
    - GraphQL architecture: schema, queries, mutations, and subscriptions
    - Setting up a GraphQL server with Apollo Server
    - Writing simple GraphQL queries and mutations
- **Writing GraphQL Queries, Mutations, and Subscriptions**
    - Creating complex queries and mutations
    - Understanding resolvers and schema design
    - Subscriptions for real-time data updates
    - Handling errors in GraphQL

### **14. Monitoring with PM2**

- Introduction to PM2 for Node.js process management
- Setting up PM2 for application monitoring
- Auto-restarting Node.js apps on crashes
- Monitoring performance with PM2 logs and stats
- Log rotations

___


# Node.js Learning Guide
# Part 1: Introduction to Node.js – The Power of JavaScript on the Server

---

# What is Node.js?

Node.js is a JavaScript runtime that allows JavaScript to run outside the browser.

Before Node.js:

```text
JavaScript → Browser Only
```

After Node.js:

```text
JavaScript → Browser + Server
```

---

# Real World Analogy

Imagine a restaurant.

### Frontend (Browser)

Waiter takes customer order.

```text
HTML
CSS
JavaScript
```

### Backend (Server)

Kitchen prepares food.

```text
Node.js
Database
Business Logic
```

Node.js acts as the kitchen.

---

# Why Node.js Became Popular

Before Node.js:

```text
Frontend → JavaScript
Backend → Java, PHP, C#, Python
```

Developers had to learn two languages.

With Node.js:

```text
Frontend → JavaScript
Backend → JavaScript
```

One language everywhere.

---

# Node.js Runtime Environment

JavaScript normally runs inside browsers using browser engines.

Examples:

| Browser | Engine |
|----------|---------|
| Chrome | V8 |
| Edge | V8 |
| Firefox | SpiderMonkey |

Node.js uses:

```text
Google V8 Engine
```

outside the browser.

---

# What Node.js Adds

JavaScript alone cannot:

```javascript
Read Files
Create Servers
Access OS
```

Node.js provides:

```javascript
fs
http
path
os
process
```

modules.

---

# Event-Driven Architecture

Traditional servers:

```text
Request
 ↓
Wait
 ↓
Response
```

Node.js:

```text
Request
 ↓
Register Event
 ↓
Continue Working
 ↓
Handle Event Later
```

---

# Non-Blocking I/O

I/O means:

```text
Database Access
File Access
Network Calls
```

---

## Blocking Example

```javascript
Read File
Wait
Wait
Wait
Continue
```

Everything stops.

---

## Non-Blocking Example

```javascript
Read File
Continue Work
File Ready Later
Process Result
```

Much faster.

---

# Installing Node.js

Download:

```text
https://nodejs.org
```

Verify installation:

```bash
node -v
```

Example:

```text
v24.x.x
```

---

# Running JavaScript with Node

Create:

```javascript
app.js
```

```javascript
console.log("Hello Node");
```

Run:

```bash
node app.js
```

Output:

```text
Hello Node
```

---

# What is npm?

npm stands for:

```text
Node Package Manager
```

Largest package repository in the world.

---

# npm Commands

Initialize project:

```bash
npm init
```

Quick initialization:

```bash
npm init -y
```

---

# Installing Packages

Example:

```bash
npm install express
```

Short:

```bash
npm i express
```

---

# package.json

Created by npm.

```json
{
  "name": "lms-app",
  "version": "1.0.0"
}
```

Stores:

- Project Info
- Dependencies
- Scripts

---

# Modules

Modules organize code into files.

---

# Export

```javascript
function add(a,b){
    return a+b;
}

module.exports = add;
```

---

# Import

```javascript
const add =
require("./math");

console.log(
    add(10,20)
);
```

Output:

```text
30
```

---

# Key Concepts Summary

| Concept | Description |
|----------|-------------|
| Node.js | JavaScript Runtime |
| V8 Engine | Executes JS |
| Event Driven | Event-based architecture |
| Non Blocking I/O | Efficient processing |
| npm | Package manager |
| Module | Reusable code |

---

# Practice Exercise

Create:

```javascript
math.js
```

Export:

```javascript
add()
subtract()
multiply()
```

Import into:

```javascript
app.js
```

---

# Mini Project

## CLI Calculator

Features:

```text
Add
Subtract
Multiply
Divide
```

Using:

```javascript
Modules
Node Runtime
npm
```

---

---

# Part 2: Understanding the Event Loop – Node.js Architecture

---

# Why Event Loop Exists

JavaScript is:

```text
Single Threaded
```

Meaning:

```text
One Call Stack
One Task At A Time
```

Question:

```text
How does Node.js handle thousands of users?
```

Answer:

```text
Event Loop
```

---

# Node.js Architecture

```text
Request
   ↓
Event Loop
   ↓
Worker Threads
   ↓
Callback Queue
   ↓
Response
```

---

# Call Stack

Where JavaScript executes code.

Example:

```javascript
function one(){
    two();
}

function two(){
    console.log("Hello");
}

one();
```

Stack:

```text
one()
 ↓
two()
 ↓
console.log()
```

---

# Event Loop

Continuously checks:

```text
Is Call Stack Empty?
```

If yes:

```text
Move Next Callback
To Stack
```

---

# Example

```javascript
console.log("Start");

setTimeout(() => {
    console.log("Timer");
},0);

console.log("End");
```

Output:

```text
Start
End
Timer
```

Why?

Because timer enters callback queue.

---

# Blocking Code

Bad:

```javascript
while(true){

}
```

Server freezes.

---

# Non-Blocking Code

Good:

```javascript
fs.readFile(
    "file.txt",
    callback
);
```

Server continues working.

---

# Callbacks

```javascript
fs.readFile(
    "data.txt",
    (err,data)=>{

    }
);
```

Runs after operation finishes.

---

# Promises

Cleaner async handling.

```javascript
fetchData()
.then(result=>{

});
```

---

# Async Await

Most readable.

```javascript
const data =
await fetchData();
```

---

# Key Concepts Summary

| Concept | Description |
|----------|-------------|
| Event Loop | Handles async execution |
| Call Stack | Executes code |
| Callback Queue | Stores completed callbacks |
| Blocking | Stops execution |
| Non Blocking | Continues execution |
| Promise | Future result |
| Async Await | Cleaner async code |

---

# Mini Project

## File Reader

Read multiple files simultaneously using:

```javascript
fs.readFile()
Promises
async/await
```

---

---

# Part 3: Creating a Basic HTTP Server

---

# What is an HTTP Server?

An HTTP server:

```text
Receives Request
Processes Request
Returns Response
```

---

# Built-in HTTP Module

```javascript
const http =
require("http");
```

No installation required.

---

# Creating Server

```javascript
const http =
require("http");

const server =
http.createServer(
(req,res)=>{

    res.end("Hello World");

});

server.listen(3000);
```

Run:

```bash
node app.js
```

Open:

```text
http://localhost:3000
```

Output:

```text
Hello World
```

---

# Request Object

Contains incoming request information.

```javascript
req.url
req.method
req.headers
```

Example:

```javascript
console.log(req.url);
```

---

# Response Object

Used to send data back.

```javascript
res.end();
```

Example:

```javascript
res.end("Success");
```

---

# Routing

Handle different URLs.

```javascript
if(req.url === "/"){
    res.end("Home");
}
```

```javascript
if(req.url === "/about"){
    res.end("About");
}
```

---

# Handling Methods

---

## GET

```javascript
req.method === "GET"
```

Retrieve data.

---

## POST

```javascript
req.method === "POST"
```

Create data.

---

## PUT

```javascript
req.method === "PUT"
```

Update data.

---

## DELETE

```javascript
req.method === "DELETE"
```

Delete data.

---

# Example Router

```javascript
if(
req.url === "/users"
&& req.method === "GET"
){
    res.end("Users List");
}
```

---

# Sending JSON

```javascript
res.setHeader(
"Content-Type",
"application/json"
);
```

```javascript
res.end(
JSON.stringify({
    name:"Tauseef"
})
);
```

---

# Status Codes

```javascript
res.statusCode = 200;
```

Common:

| Code | Meaning |
|--------|---------|
| 200 | Success |
| 201 | Created |
| 400 | Bad Request |
| 401 | Unauthorized |
| 404 | Not Found |
| 500 | Server Error |

---

# Key Concepts Summary

| Concept | Description |
|----------|-------------|
| HTTP Server | Processes requests |
| Request Object | Incoming data |
| Response Object | Outgoing data |
| Routing | URL handling |
| GET | Read |
| POST | Create |
| PUT | Update |
| DELETE | Remove |

---

# Mini Project

## Student API

Routes:

```text
GET /students
POST /students
PUT /students
DELETE /students
```

Return JSON responses.

---

# Node.js Learning Roadmap So Far

```text
Node.js Runtime
      ↓
npm
      ↓
Modules
      ↓
Event Loop
      ↓
Callbacks
      ↓
Promises
      ↓
HTTP Server
      ↓
Routing
      ↓
REST APIs
```

---

# Challenge Project

## Course Management Server

Features:

```text
Create Course
Update Course
Delete Course
Get Course
```

Using:

```javascript
Node.js
HTTP Module
Modules
Event Loop
JSON Responses
Routing
```

This prepares you for Express.js, REST APIs, databases, and full backend development.

---

# Next Section

Part 4 → Express.js  
Part 5 → REST APIs  
Part 6 → MongoDB, SQL, Prisma, Drizzle  
Part 7 → Authentication & JWT  
Part 8 → File System & Uploads  
Part 9 → WebSockets & Socket.io  
Part 10–14 → Deployment, Monitoring, PM2, Rate Limiting, GraphQL


____
# Node.js Learning Guide
# Part 4: Express.js – Simplifying Backend Development

---

# Why Express.js?

Creating servers using the built-in HTTP module becomes repetitive.

Example:

```javascript
const http = require("http");

const server = http.createServer((req, res) => {

    if(req.url === "/") {
        res.end("Home");
    }

    if(req.url === "/about") {
        res.end("About");
    }

});
```

As the application grows:

```text
More Routes
More Conditions
More Complexity
```

Express simplifies everything.

---

# What is Express.js?

Express.js is a lightweight web framework built on Node.js.

Think of:

```text
Node.js = Engine
Express.js = Car Body + Controls
```

Node provides the foundation.

Express provides developer-friendly tools.

---

# Installing Express

Initialize project:

```bash
npm init -y
```

Install Express:

```bash
npm install express
```

---

# Creating Express Server

```javascript
const express = require("express");

const app = express();

app.listen(3000, () => {

    console.log("Server Running");

});
```

---

# Creating Routes

```javascript
app.get("/", (req,res) => {

    res.send("Home Page");

});
```

```javascript
app.get("/about", (req,res) => {

    res.send("About Page");

});
```

---

# Route Methods

```javascript
app.get()
app.post()
app.put()
app.delete()
```

Each corresponds to an HTTP method.

---

# Request and Response Objects

Express extends Node's request and response objects.

```javascript
app.get("/", (req,res)=>{

    res.send("Hello");

});
```

---

# Returning JSON

```javascript
app.get("/user",(req,res)=>{

    res.json({
        name:"Tauseef",
        city:"Bangalore"
    });

});
```

Output:

```json
{
  "name":"Tauseef",
  "city":"Bangalore"
}
```

---

# Route Parameters

Dynamic values inside URL.

Route:

```javascript
app.get(
"/users/:id",
(req,res)=>{

});
```

Request:

```text
/users/100
```

Access:

```javascript
req.params.id
```

Output:

```text
100
```

---

# Query Parameters

URL:

```text
/products?page=2
```

Access:

```javascript
req.query.page
```

Output:

```text
2
```

---

# Middleware

Middleware sits between:

```text
Request
   ↓
Middleware
   ↓
Route Handler
   ↓
Response
```

---

# Example Middleware

```javascript
app.use((req,res,next)=>{

    console.log("Request Received");

    next();

});
```

`next()` passes control forward.

---

# Built-in Middleware

---

## JSON Parser

```javascript
app.use(express.json());
```

Allows:

```json
{
   "name":"John"
}
```

to be accessed via:

```javascript
req.body
```

---

## URL Encoded Parser

```javascript
app.use(
express.urlencoded({
    extended:true
})
);
```

Used with HTML forms.

---

# Multiple Middleware

```javascript
app.use(logger);
app.use(auth);
app.use(validate);
```

Request passes through each.

---

# Key Concepts Summary

| Concept | Description |
|----------|-------------|
| Express | Node.js framework |
| Route | URL handler |
| Middleware | Intercepts requests |
| Params | Dynamic URL values |
| Query | URL query values |
| req | Request object |
| res | Response object |

---

# Practice Exercise

Create routes:

```text
GET /courses
GET /courses/:id
POST /courses
```

Return JSON.

---

# Mini Project

## Course Management API

Routes:

```text
GET Courses
Create Course
Update Course
Delete Course
```

Use:

```javascript
Express
Routing
Middleware
JSON
```

---

---

# Part 5: RESTful API Design – Building APIs with Express

---

# What is an API?

API stands for:

```text
Application Programming Interface
```

Allows applications to communicate.

Example:

```text
Frontend
   ↓
REST API
   ↓
Database
```

---

# What is REST?

REST stands for:

```text
Representational State Transfer
```

A standard way of designing APIs.

---

# REST Resource Example

Resource:

```text
Students
```

Endpoints:

```text
GET    /students
GET    /students/1
POST   /students
PUT    /students/1
DELETE /students/1
```

---

# CRUD Operations

| Operation | HTTP Method |
|------------|------------|
| Create | POST |
| Read | GET |
| Update | PUT |
| Delete | DELETE |

---

# GET Example

```javascript
app.get("/students",(req,res)=>{

    res.json(students);

});
```

---

# POST Example

```javascript
app.post("/students",(req,res)=>{

    const student =
    req.body;

});
```

---

# PUT Example

```javascript
app.put(
"/students/:id",
(req,res)=>{

});
```

Updates record.

---

# DELETE Example

```javascript
app.delete(
"/students/:id",
(req,res)=>{

});
```

Deletes record.

---

# Request Body

```json
{
  "name":"Tauseef",
  "course":"Node.js"
}
```

Access:

```javascript
req.body
```

---

# JSON Responses

```javascript
res.json({
    success:true
});
```

---

# Status Codes

---

## Success

```javascript
200 OK
201 Created
```

---

## Client Errors

```javascript
400 Bad Request
401 Unauthorized
403 Forbidden
404 Not Found
```

---

## Server Errors

```javascript
500 Internal Server Error
```

---

# Example

```javascript
res.status(201).json({

    message:"Student Created"

});
```

---

# REST Best Practices

Use nouns:

Good:

```text
/students
/courses
/users
```

Bad:

```text
/getStudents
/deleteStudent
```

---

# Key Concepts Summary

| Concept | Description |
|----------|-------------|
| REST | API architecture |
| CRUD | Create Read Update Delete |
| Endpoint | API URL |
| JSON | Data format |
| Status Code | Response status |

---

# Mini Project

## LMS API

Resources:

```text
Courses
Students
Enrollments
```

Implement:

```text
GET
POST
PUT
DELETE
```

---

---

# Part 6: Working with Databases – MongoDB, SQL & ORMs

---

# Why Databases?

Without databases:

```text
Application loses data
after restart
```

Databases provide persistence.

---

# Types of Databases

---

# SQL Databases

Examples:

```text
MySQL
PostgreSQL
SQL Server
```

Data stored in tables.

Example:

| ID | Name |
|----|------|
| 1 | Tauseef |
| 2 | John |

---

# NoSQL Databases

Example:

```text
MongoDB
```

Stores JSON-like documents.

```json
{
   "name":"Tauseef",
   "course":"Node.js"
}
```

---

# MongoDB + Mongoose

Install:

```bash
npm install mongoose
```

---

# Connect Database

```javascript
const mongoose =
require("mongoose");

mongoose.connect(
"mongodb://localhost/lms"
);
```

---

# Schema

Blueprint of document.

```javascript
const studentSchema =
new mongoose.Schema({

    name:String,

    age:Number

});
```

---

# Model

```javascript
const Student =
mongoose.model(
"Student",
studentSchema
);
```

---

# Create

```javascript
await Student.create({

    name:"Tauseef"

});
```

---

# Read

```javascript
const students =
await Student.find();
```

---

# Update

```javascript
await Student.findByIdAndUpdate(
id,
{
   name:"Updated"
}
);
```

---

# Delete

```javascript
await Student.findByIdAndDelete(
id
);
```

---

# SQL with Node.js

Popular databases:

```text
MySQL
PostgreSQL
```

---

# ORM

ORM means:

```text
Object Relational Mapper
```

Converts:

```javascript
Objects
```

to

```text
Database Records
```

---

# Popular ORMs

| ORM | Database |
|-------|---------|
| Prisma | SQL |
| Drizzle | SQL |
| Sequelize | SQL |
| Mongoose | MongoDB |

---

# Prisma Example

Install:

```bash
npm install prisma
```

---

# Create Record

```javascript
await prisma.user.create({

    data:{
        name:"Tauseef"
    }

});
```

---

# Why ORMs?

Without ORM:

```sql
SELECT * FROM users
```

With ORM:

```javascript
User.findMany()
```

Cleaner and safer.

---

# Key Concepts Summary

| Concept | Description |
|----------|-------------|
| SQL | Table-based database |
| NoSQL | Document database |
| MongoDB | Popular NoSQL DB |
| Mongoose | MongoDB ODM |
| Prisma | SQL ORM |
| CRUD | Database operations |

---

# Practice Exercise

Build:

```text
Student Collection
Course Collection
Enrollment Collection
```

Perform:

```text
Create
Read
Update
Delete
```

---

# Mini Project

## LMS Database Layer

Collections/Tables:

```text
Students
Courses
Enrollments
```

Implement:

```javascript
MongoDB
Mongoose
CRUD APIs
```

---

# Node.js Backend Roadmap So Far

```text
Node.js
    ↓
npm
    ↓
Modules
    ↓
Event Loop
    ↓
HTTP Server
    ↓
Express.js
    ↓
REST APIs
    ↓
MongoDB
    ↓
SQL
    ↓
Prisma / Drizzle
```

---

# Challenge Project

## Learning Management System Backend

Features:

### Authentication

```text
Register
Login
```

### Courses

```text
Create
Update
Delete
View
```

### Students

```text
Enroll
Track Progress
```

### Database

```text
MongoDB
or
PostgreSQL + Prisma
```

This foundation prepares you for:

```text
JWT Authentication
Authorization
File Uploads
WebSockets
Deployment
GraphQL
Microservices
```

---

# Next Section

Part 7 → Authentication & Authorization (JWT, bcrypt)

Part 8 → File System & File Uploads

Part 9 → Real-Time Apps with Socket.io

Part 10 → Deployment & Environment Variables

Part 11 → Rate Limiting

Part 12 → Logging & Monitoring

Part 13 → GraphQL

Part 14 → PM2 Process Management

___


# Node.js Learning Guide
# Part 7: Authentication & Authorization – Securing Your Application

---

# Why Security Matters

Imagine a Learning Management System (LMS).

Without security:

```text
Anyone can:
- View Courses
- Delete Courses
- Access Admin Pages
- Change User Data
```

This is dangerous.

Authentication and Authorization solve this problem.

---

# Authentication vs Authorization

Many developers confuse these terms.

---

## Authentication

Verifies:

```text
Who are you?
```

Example:

```text
Username + Password
```

Result:

```text
User Identity Confirmed
```

---

## Authorization

Verifies:

```text
What can you do?
```

Example:

```text
Student → View Courses

Instructor → Create Courses

Admin → Delete Users
```

---

# Real World Analogy

Airport Security

### Authentication

```text
Show Passport
```

Identity verified.

---

### Authorization

```text
Business Class Ticket?
```

Determines accessible areas.

---

# User Registration Flow

```text
Register
    ↓
Validate Data
    ↓
Hash Password
    ↓
Store User
    ↓
Success
```

---

# Password Hashing

Never store passwords like this:

```json
{
  "username":"john",
  "password":"123456"
}
```

Very insecure.

---

# bcrypt.js

Install:

```bash
npm install bcrypt
```

---

# Hash Password

```javascript
const bcrypt =
require("bcrypt");
```

```javascript
const hashedPassword =
await bcrypt.hash(
    "mypassword",
    10
);
```

Output:

```text
$2b$10$...
```

Cannot be reversed easily.

---

# Compare Password

```javascript
const match =
await bcrypt.compare(
    "mypassword",
    hashedPassword
);
```

Output:

```javascript
true
```

---

# JWT (JSON Web Token)

JWT allows stateless authentication.

---

# Traditional Session Authentication

```text
Login
 ↓
Server Stores Session
 ↓
Client Sends Session ID
```

Requires session storage.

---

# JWT Authentication

```text
Login
 ↓
Server Generates Token
 ↓
Client Stores Token
 ↓
Token Sent With Requests
```

Server doesn't store sessions.

---

# Install JWT

```bash
npm install jsonwebtoken
```

---

# Generate Token

```javascript
const jwt =
require("jsonwebtoken");
```

```javascript
const token =
jwt.sign(
{
    id:1,
    role:"student"
},
"secretKey",
{
    expiresIn:"1h"
}
);
```

---

# Verify Token

```javascript
jwt.verify(
    token,
    "secretKey"
);
```

Returns payload.

---

# JWT Structure

```text
Header
.
Payload
.
Signature
```

Example:

```text
xxxxx.yyyyy.zzzzz
```

---

# Authentication Middleware

```javascript
function auth(
req,
res,
next
){

    const token =
    req.headers.authorization;

    if(!token){

        return res
        .status(401)
        .json({
            message:"Unauthorized"
        });

    }

    next();

}
```

---

# Protect Routes

```javascript
app.get(
"/profile",
auth,
(req,res)=>{

});
```

Only authenticated users allowed.

---

# Role-Based Access Control (RBAC)

User Roles:

```text
Student
Instructor
Admin
```

---

# Authorization Middleware

```javascript
function authorize(role){

    return (
        req,
        res,
        next
    ) => {

        if(
            req.user.role !== role
        ){

            return res
            .status(403)
            .json({
                message:"Forbidden"
            });

        }

        next();

    };

}
```

---

# Example

```javascript
app.delete(
"/users",
auth,
authorize("admin"),
handler
);
```

Only admins can delete users.

---

# Key Concepts Summary

| Concept | Description |
|----------|-------------|
| Authentication | Verify identity |
| Authorization | Verify permissions |
| JWT | Stateless authentication |
| bcrypt | Password hashing |
| Middleware | Route protection |
| RBAC | Role-based access |

---

# Practice Exercise

Build:

```text
Register
Login
Protected Route
Admin Route
```

Using:

```javascript
JWT
bcrypt
Middleware
```

---

# Mini Project

## LMS Authentication System

Features:

```text
Student Registration
Instructor Registration
Login
JWT Authentication
Role-Based Access
```

---

---

# Part 8: Working with File Systems – Reading and Writing Files

---

# What is the File System Module?

Node.js provides:

```javascript
fs
```

module.

Used for:

```text
Reading Files
Writing Files
Deleting Files
Uploading Files
```

---

# Import fs

```javascript
const fs =
require("fs");
```

---

# Read File (Async)

```javascript
fs.readFile(
    "data.txt",
    "utf8",
    (
        err,
        data
    ) => {

        console.log(data);

    }
);
```

---

# Read File (Sync)

```javascript
const data =
fs.readFileSync(
    "data.txt",
    "utf8"
);
```

---

# Difference

### Synchronous

```text
Read File
Wait
Continue
```

---

### Asynchronous

```text
Read File
Continue
File Ready Later
```

Preferred in production.

---

# Write File

```javascript
fs.writeFile(
    "data.txt",
    "Hello Node",
    (err)=>{

    }
);
```

Creates file if missing.

---

# Append File

```javascript
fs.appendFile(
    "data.txt",
    "\nNew Line",
    ()=>{}
);
```

---

# Delete File

```javascript
fs.unlink(
    "data.txt",
    ()=>{}
);
```

---

# File Uploads

Users often upload:

```text
Images
PDFs
Videos
Documents
```

---

# Multer

Popular upload middleware.

Install:

```bash
npm install multer
```

---

# Configure Multer

```javascript
const multer =
require("multer");
```

```javascript
const upload =
multer({
    dest:"uploads/"
});
```

---

# Upload Route

```javascript
app.post(
"/upload",
upload.single("file"),
(req,res)=>{

    res.send(
        "Uploaded"
    );

});
```

---

# Upload Form

```html
<form
 enctype="multipart/form-data"
>

<input
 type="file"
 name="file"
/>

</form>
```

---

# Key Concepts Summary

| Concept | Description |
|----------|-------------|
| fs | File system module |
| readFile | Read file |
| writeFile | Create/update file |
| appendFile | Add content |
| unlink | Delete file |
| multer | File uploads |

---

# Mini Project

## Assignment Submission System

Features:

```text
Upload PDF
Store Files
View Uploaded Files
Delete Files
```

---

---

# Part 9: Building Real-Time Applications – WebSockets with Socket.io

---

# Why Real-Time Communication?

Normal HTTP:

```text
Request
 ↓
Response
 ↓
Connection Closed
```

Good for:

```text
Forms
Pages
APIs
```

Not ideal for:

```text
Chat Apps
Live Scores
Notifications
```

---

# What are WebSockets?

WebSockets create a persistent connection.

```text
Client
 ↕
 Server
```

Communication in both directions.

---

# HTTP vs WebSocket

### HTTP

```text
Client → Server
```

---

### WebSocket

```text
Client ↔ Server
```

Both can send messages anytime.

---

# Real World Examples

```text
WhatsApp
Slack
Teams
Stock Market Apps
Live Sports Scores
```

---

# Socket.io

Popular library for WebSockets.

Install:

```bash
npm install socket.io
```

---

# Server Setup

```javascript
const io =
require("socket.io")(
server
);
```

---

# Connection Event

```javascript
io.on(
"connection",
(socket)=>{

    console.log(
        "User Connected"
    );

});
```

---

# Send Message

```javascript
socket.emit(
"message",
"Hello User"
);
```

---

# Receive Message

```javascript
socket.on(
"message",
(data)=>{

    console.log(data);

});
```

---

# Broadcast Message

```javascript
io.emit(
"message",
"New Announcement"
);
```

Sent to all clients.

---

# Chat Flow

```text
User A Sends Message
        ↓
Server Receives
        ↓
Server Broadcasts
        ↓
User B Receives
```

---

# Rooms

Useful for:

```text
Course Discussion
Private Chat
Team Channels
```

---

# Join Room

```javascript
socket.join(
"course-101"
);
```

---

# Send to Room

```javascript
io.to(
"course-101"
).emit(
"message",
"Class Starts"
);
```

---

# Key Concepts Summary

| Concept | Description |
|----------|-------------|
| WebSocket | Persistent connection |
| Socket.io | WebSocket library |
| emit | Send event |
| on | Listen event |
| Broadcast | Send to everyone |
| Rooms | Group communication |

---

# Practice Exercise

Build:

```text
Join Chat
Send Message
Receive Message
```

Using:

```javascript
Socket.io
Express
Events
```

---

# Mini Project

## Real-Time LMS Notifications

Features:

```text
Course Announcements
Assignment Alerts
Live Chat
Instructor Notifications
```

---

# Node.js Roadmap So Far

```text
Node.js Runtime
      ↓
npm
      ↓
Modules
      ↓
Event Loop
      ↓
HTTP Server
      ↓
Express.js
      ↓
REST APIs
      ↓
Databases
      ↓
Authentication
      ↓
File Uploads
      ↓
WebSockets
```

---

# Challenge Project

## LMS Backend (Phase 2)

Implement:

### Authentication

```text
Register
Login
JWT
Roles
```

### File Management

```text
Upload Assignments
Store PDFs
Delete Files
```

### Real-Time Features

```text
Live Notifications
Course Chat
Instructor Broadcasts
```

Concepts Used:

```javascript
Express
MongoDB
JWT
bcrypt
Middleware
fs
multer
Socket.io
```

---

# Next Section

Part 10 → Deploying Node.js Applications

Part 11 → API Rate Limiting

Part 12 → Logging & Monitoring

Part 13 → GraphQL

Part 14 → PM2 Process Management

___

# Node.js Learning Guide
# Part 10: Deploying Your Node.js Application

---

# What is Deployment?

Deployment means moving your application from:

```text
Your Laptop
     ↓
Internet Accessible Server
```

So real users can access it.

---

# Development vs Production

## Development

```text
localhost:3000
```

Only you can access.

---

## Production

```text
https://myapp.com
```

Anyone can access.

---

# Deployment Options

Popular platforms:

| Platform | Difficulty |
|-----------|------------|
| Railway | Easy |
| Render | Easy |
| AWS | Advanced |
| DigitalOcean | Intermediate |
| Azure | Intermediate |
| Google Cloud | Advanced |

---

# Deployment Flow

```text
Code
 ↓
GitHub
 ↓
Cloud Platform
 ↓
Build
 ↓
Deploy
 ↓
Live Website
```

---

# Environment Variables

Never hardcode secrets.

Bad:

```javascript
const password =
"my-secret-password";
```

---

# Using .env

Install:

```bash
npm install dotenv
```

---

# .env File

```env
PORT=3000

DB_URL=mongodb://localhost/lms

JWT_SECRET=mysecret
```

---

# Load Variables

```javascript
require("dotenv").config();
```

Access:

```javascript
process.env.PORT
```

---

# Why Environment Variables?

Different values for:

```text
Development
Testing
Production
```

---

# Reverse Proxy

Users don't directly connect to Node.js.

Instead:

```text
User
 ↓
Nginx
 ↓
Node.js
```

---

# Why Use Nginx?

Benefits:

```text
SSL
Load Balancing
Caching
Security
```

---

# Example Nginx Flow

```text
https://myapp.com
         ↓
      Nginx
         ↓
 localhost:3000
```

---

# Production Checklist

```text
Environment Variables
HTTPS
Error Handling
Logging
Database Backup
Rate Limiting
Monitoring
```

---

# Key Concepts Summary

| Concept | Description |
|----------|-------------|
| Deployment | Making app public |
| Cloud Hosting | Server provider |
| .env | Configuration file |
| process.env | Read variables |
| Nginx | Reverse proxy |

---

# Mini Project

Deploy LMS API to:

```text
Railway
Render
Azure
```

---

---

# Part 11: API Rate Limiting – Protecting Your Endpoints

---

# Why Rate Limiting?

Imagine:

```text
Login API
```

Without limits:

```text
1 User
↓
1 Million Requests
```

Server crashes.

---

# What is Rate Limiting?

Controls:

```text
How many requests
A user can make
Within a time period
```

Example:

```text
100 requests
per 15 minutes
```

---

# Benefits

Prevents:

```text
DDoS Attacks
Brute Force Attacks
API Abuse
Server Overload
```

---

# Install express-rate-limit

```bash
npm install express-rate-limit
```

---

# Create Limiter

```javascript
const rateLimit =
require("express-rate-limit");

const limiter =
rateLimit({

    windowMs:
    15 * 60 * 1000,

    max:100

});
```

---

# Apply Globally

```javascript
app.use(limiter);
```

---

# Custom Login Limiter

```javascript
const loginLimiter =
rateLimit({

    windowMs:
    15 * 60 * 1000,

    max:5

});
```

---

# Protect Login Route

```javascript
app.post(
"/login",
loginLimiter,
handler
);
```

---

# Custom Response

```javascript
const limiter =
rateLimit({

    windowMs:
    60000,

    max:10,

    message:
    "Too many requests"

});
```

---

# Key Concepts Summary

| Concept | Description |
|----------|-------------|
| Rate Limiting | Restrict requests |
| Throttling | Slow request rate |
| windowMs | Time period |
| max | Maximum requests |
| express-rate-limit | Popular package |

---

# Mini Project

Protect:

```text
Login
Registration
Password Reset
```

with rate limiting.

---

---

# Part 12: Logging & Monitoring – Tracking Application Health

---

# Why Logging Matters

Without logs:

```text
Something Broke
↓
No Idea Why
```

With logs:

```text
Error
↓
Timestamp
↓
Cause
↓
Fix
```

---

# Logging Types

---

## Info

```text
Server Started
User Logged In
```

---

## Warning

```text
High Memory Usage
Slow Query
```

---

## Error

```text
Database Connection Failed
```

---

# Morgan

HTTP request logger.

Install:

```bash
npm install morgan
```

---

# Setup

```javascript
const morgan =
require("morgan");

app.use(
morgan("dev")
);
```

Logs:

```text
GET /users 200
```

---

# Winston

Advanced logging library.

Install:

```bash
npm install winston
```

---

# Logger Example

```javascript
const winston =
require("winston");
```

```javascript
const logger =
winston.createLogger({

    level:"info",

    transports:[

        new winston
        .transports.Console()

    ]

});
```

---

# Logging Messages

```javascript
logger.info(
"Server Started"
);
```

```javascript
logger.warn(
"High CPU Usage"
);
```

```javascript
logger.error(
"Database Failed"
);
```

---

# Log Files

```javascript
new winston
.transports.File({

    filename:"app.log"

});
```

---

# Monitoring

Monitoring answers:

```text
Is Server Running?
How Much Memory?
How Much CPU?
How Fast?
```

---

# What Should Be Monitored?

```text
CPU Usage
Memory Usage
Requests
Response Times
Errors
Database Health
```

---

# Key Concepts Summary

| Concept | Description |
|----------|-------------|
| Logging | Recording events |
| Morgan | HTTP logs |
| Winston | Structured logs |
| Monitoring | Health tracking |
| Error Logs | Troubleshooting |

---

# Mini Project

Track:

```text
User Logins
API Requests
Errors
Server Startup
```

---

---

# Part 13: GraphQL

---

# What is GraphQL?

GraphQL is an API query language developed by
:contentReference[oaicite:0]{index=0}.

---

# REST Problem

Suppose client needs:

```text
User Name
Course Name
```

REST may require:

```text
GET /users
GET /courses
```

Multiple requests.

---

# GraphQL Solution

Single query:

```graphql
{
    user {
        name
    }

    course {
        title
    }
}
```

---

# REST vs GraphQL

| REST | GraphQL |
|--------|---------|
| Multiple Endpoints | Single Endpoint |
| Fixed Response | Custom Response |
| Over-fetching | Avoided |
| Under-fetching | Avoided |

---

# GraphQL Architecture

```text
Schema
 ↓
Resolvers
 ↓
Database
```

---

# Schema

Defines available data.

```graphql
type User {

    id: ID

    name: String

}
```

---

# Query

Fetch data.

```graphql
query {

    users {

        name

    }

}
```

---

# Mutation

Modify data.

```graphql
mutation {

    createUser(
        name:"Tauseef"
    ){

        id

    }

}
```

---

# Subscription

Real-time updates.

```graphql
subscription {

    userCreated {

        id

    }

}
```

---

# Apollo Server

Popular GraphQL server.

Install:

```bash
npm install
@apollo/server
graphql
```

---

# Resolver

Connects schema to actual data.

```javascript
const resolvers = {

    Query: {

        users(){

            return users;

        }

    }

};
```

---

# Error Handling

```javascript
throw new Error(
"User Not Found"
);
```

---

# Key Concepts Summary

| Concept | Description |
|----------|-------------|
| GraphQL | API query language |
| Schema | Data structure |
| Query | Read data |
| Mutation | Modify data |
| Subscription | Real-time updates |
| Resolver | Fetch data |

---

# Mini Project

Create GraphQL LMS API:

```text
Students
Courses
Enrollments
```

Operations:

```text
Query
Mutation
Subscription
```

---

---

# Part 14: Monitoring with PM2

---

# What is PM2?

PM2 is a production process manager for Node.js.

Without PM2:

```text
Node App Crashes
↓
App Stops
```

With PM2:

```text
Node App Crashes
↓
PM2 Restarts App
```

---

# Install PM2

```bash
npm install -g pm2
```

---

# Start Application

```bash
pm2 start app.js
```

---

# View Running Apps

```bash
pm2 list
```

---

# Application Status

```bash
pm2 status
```

---

# Restart App

```bash
pm2 restart app
```

---

# Stop App

```bash
pm2 stop app
```

---

# Delete App

```bash
pm2 delete app
```

---

# View Logs

```bash
pm2 logs
```

---

# Monitoring Dashboard

```bash
pm2 monit
```

Displays:

```text
CPU
Memory
Restarts
Requests
```

---

# Auto Restart

PM2 automatically restarts:

```text
Crash
Server Restart
Unexpected Failure
```

---

# Cluster Mode

Use all CPU cores.

```bash
pm2 start app.js -i max
```

Example:

```text
4 Core CPU
↓
4 Node Processes
```

Better performance.

---

# Log Rotation

Without rotation:

```text
Logs Grow Forever
```

Install:

```bash
pm2 install
pm2-logrotate
```

Automatically rotates logs.

---

# PM2 Ecosystem File

```javascript
module.exports = {

    apps:[{

        name:"lms",

        script:"app.js",

        instances:"max"

    }]

};
```

Start:

```bash
pm2 start ecosystem.config.js
```

---

# Key Concepts Summary

| Concept | Description |
|----------|-------------|
| PM2 | Process manager |
| Auto Restart | Recover from crashes |
| Logs | Application records |
| Cluster Mode | Multiple CPU cores |
| Log Rotation | Manage log size |

---

# Complete Node.js Backend Roadmap

```text
Node.js Fundamentals
          ↓
Event Loop
          ↓
HTTP Module
          ↓
Express.js
          ↓
REST APIs
          ↓
MongoDB / PostgreSQL
          ↓
Prisma / Drizzle
          ↓
Authentication (JWT)
          ↓
Authorization (RBAC)
          ↓
File Uploads
          ↓
Socket.io
          ↓
Deployment
          ↓
Rate Limiting
          ↓
Logging
          ↓
Monitoring
          ↓
GraphQL
          ↓
PM2
          ↓
Production Backend Development
```

---

# Ultimate Capstone Project

## Learning Management System (LMS) Backend

### Authentication

```text
Register
Login
JWT
RBAC
```

### Courses

```text
Create
Update
Delete
View
```

### Students

```text
Enroll
Track Progress
```

### File Uploads

```text
Assignments
Certificates
Profile Pictures
```

### Real-Time Features

```text
Notifications
Live Chat
Announcements
```

### Security

```text
JWT
bcrypt
Rate Limiting
Protected Routes
```

### Database

```text
MongoDB + Mongoose

OR

PostgreSQL + Prisma
```

### Monitoring

```text
Winston
Morgan
PM2
```

### Deployment

```text
Render
Railway
Azure
AWS
DigitalOcean
```

### Optional Advanced Features

```text
GraphQL API
Socket.io Chat
Microservices
Docker
CI/CD
```

This project combines nearly every Node.js concept from beginner to production-ready backend development and is an excellent bridge to advanced topics such as Docker, Kubernetes, Microservices, and Cloud Architecture.
