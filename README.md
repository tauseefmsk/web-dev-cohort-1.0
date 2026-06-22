# Web Dev Cohort 1.0

---

# Phase 0: Web Warriors

**Objective:** Learn the building blocks of the web, how the internet works, and how protocols enable communication.

## 1. How the Internet Works

### Topics
- Introduction to the Internet
- Overview of the World Wide Web (WWW)
- How data is transferred across networks
- IP addresses, domain names, and routing

### Key Concepts
- Internet Service Providers (ISPs)
- Routers
- DNS

---

## 2. DNS Magic and Internals

### Topics
- What is DNS (Domain Name System)?
- How DNS resolves domain names to IP addresses
- DNS record types:
  - A Record
  - CNAME Record
  - MX Record
- DNS hierarchy:
  - Root DNS Servers
  - Top-Level Domains (TLDs)
  - Authoritative DNS Servers
- Browser DNS lookup process

### Key Concepts
- Recursive Queries
- DNS Caching
- TTL (Time To Live)

---

## 3. Server-Client Architecture

### Topics
- Client-Server model
- Client vs Server responsibilities
- HTTP Request-Response cycle
- Browsers as clients
- Web servers and hosting

### Key Concepts
- Apache
- Nginx
- Client-side vs Server-side
- Request Headers
- Response Codes

---

## 4. Internet Protocols

### 4.1 TCP/IP

#### Topics
- What is TCP/IP?
- TCP and IP fundamentals
- Data segmentation and transmission
- Error checking and retransmission

#### Key Concepts
- IP Addressing
- Port Numbers
- Datagram Transmission

### 4.2 UDP

#### Topics
- What is UDP?
- UDP vs TCP
- Video streaming and gaming use cases
- Reliability vs speed

#### Key Concepts
- Connectionless Communication
- Low Overhead
- Datagram-Based Transmission

---

## 5. TCP 3-Way Handshake

### Topics
- SYN
- SYN-ACK
- ACK
- Reliable connection establishment
- Data transfer after handshake

### Key Concepts
- Sequence Numbers
- Acknowledgments
- Reliable Communication

---

## 6. HTTP & HTTPS

### Topics
- HTTP fundamentals
- HTTPS fundamentals
- Request-Response lifecycle
- SSL/TLS basics

### Common Status Codes
- 200 OK
- 404 Not Found
- 500 Internal Server Error

### Request Methods
- GET
- POST
- PUT
- DELETE

### Key Concepts
- HTTPS Handshake
- SSL/TLS
- Certificate Authorities

---

# Phase 1: Spider-Man

**Objective:** Learn HTML and CSS to build and style websites.

## 1. HTML Basics – The Web's Skeleton

### Topics
- Introduction to HTML
- HTML Tags and Elements
- Building a simple webpage
- Semantic HTML

### Common Elements

```html
<html>
<head>
<body>
<header>
<footer>
<h1>
<p>
<a>
<ul>
<ol>
<li>
<section>
<article>
<nav>
<main>
<aside>
```

### Key Concepts
- Elements
- Tags
- Nesting
- Attributes
- Semantic HTML

---

## 2. HTML Forms and Inputs – User Interaction

### Topics
- Forms and User Input
- Form Submission
- GET and POST Methods
- Input Validation

### Common Elements

```html
<form>
<input>
<textarea>
<select>
<button>
```

### Key Concepts
- Form Elements
- Input Validation
- Accessibility
- Method Types

---

## 3. CSS Basics – Styling the Web

### Topics
- Introduction to CSS
- CSS Box Model
- Typography and Colors
- CSS Selectors
- Specificity

### Key Concepts
- Box Model
- Selectors
- Specificity
- Inline CSS
- Internal CSS
- External CSS

---

## 4. CSS Layouts – Building Responsive Pages

### Topics
- Display
- Position
- Float
- Flexbox
- Grid
- Media Queries

### Key Concepts
- Flexbox
- CSS Grid
- Responsive Design
- Mobile-First Design

---

## 5. Advanced CSS Styling

### Topics
- Pseudo Classes
- Pseudo Elements
- Animations
- Transitions

### Examples

```css
:hover
:focus
:nth-child()
```

### Key Concepts
- Animations
- Transitions
- User Experience (UX)

---

## 6. CSS Frameworks – Speeding Up Development

### Frameworks
- Bootstrap
- Tailwind CSS

### Key Concepts
- Grid Systems
- Utility-First Design
- Responsive Frameworks

---

## 7. HTML5 & CSS3 Features

### HTML5
- Semantic Elements
- Modern Input Types

### CSS3
- border-radius
- box-shadow
- gradients
- transitions

### Key Concepts
- Modern HTML
- Modern CSS
- Cross-Browser Compatibility

---

# Phase 2: JavaScript Surgeons

**Objective:** Master JavaScript fundamentals, advanced concepts, and DOM manipulation.

## 1. JavaScript Basics – The Language of the Web

### Topics
- Variables
- Data Types
- Scope
- Hoisting
- Operators
- Conditional Statements

### Data Types
- String
- Number
- Boolean
- Object
- Array
- Null
- Undefined

### Variable Declarations

```javascript
var
let
const
```

### Key Concepts
- Variables
- Data Types
- Operators
- Conditionals

---

## 2. Functions – Building Blocks of JavaScript

### Topics
- Function Declaration
- Function Expression
- Arrow Functions
- Parameters
- Return Values
- Closures

### Key Concepts
- Functions
- Closures
- Parameters
- Return Statements

---

## 3. Arrays and Objects – Working with Data

### Array Methods

```javascript
push()
pop()
shift()
unshift()
map()
filter()
reduce()
```

### Topics
- Objects
- Properties
- Methods
- Loops

### Key Concepts
- Arrays
- Objects
- Iteration

---

## 4. Asynchronous JavaScript – Handling Time-Sensitive Code

### Topics
- Callbacks
- Callback Hell
- Promises
- Async/Await

### APIs

```javascript
setTimeout()
setInterval()
```

### Key Concepts
- Asynchronous Programming
- Promises
- Async/Await

---

## 5. JavaScript and the DOM

### Topics
- DOM Basics
- Element Selection
- Content Manipulation
- Style Manipulation
- DOM Creation and Removal

### Common Methods

```javascript
document.getElementById()
document.querySelector()
document.querySelectorAll()
appendChild()
removeChild()
insertBefore()
```

### Key Concepts
- DOM Manipulation
- Dynamic Content Updates

---

## 6. Event Handling – Making Web Pages Interactive

### Events
- Click
- Hover
- Keydown
- Submit

### Methods

```javascript
addEventListener()
event.preventDefault()
event.stopPropagation()
```

### Key Concepts
- Event Listeners
- Event Bubbling
- Event Capturing

---

## 7. Object-Oriented JavaScript

### Topics
- Classes
- Objects
- Constructors
- Inheritance
- Prototypes

### Key Concepts
- OOP
- Encapsulation
- Polymorphism
- Inheritance

---

## 8. Advanced JavaScript Concepts

### Topics
- Closures
- Lexical Scope
- this Keyword
- call()
- apply()
- bind()
- Modules
- Error Handling

### Key Concepts
- Closures
- Context
- Modules
- Error Handling

---

## 9. ES6+ Features

### Topics
- Destructuring
- Template Literals
- Rest Parameters
- Spread Operator
- Map
- Set
- WeakMap
- WeakSet

### Key Concepts
- Modern JavaScript
- ES6 Syntax
- Collections

---

# Phase 3: Node Ninja

**Objective:** Learn backend development with Node.js and databases.

## Modules

1. Introduction to Node.js
2. Event Loop
3. HTTP Server
4. Express.js
5. REST APIs
6. Databases
7. Authentication & Authorization
8. File System Operations
9. WebSockets & Socket.io
10. Deployment
11. API Rate Limiting
12. Logging & Monitoring
13. GraphQL
14. PM2 Monitoring

### Technologies
- Node.js
- Express.js
- MongoDB
- MySQL
- PostgreSQL
- JWT
- bcrypt
- Socket.io
- GraphQL
- PM2

---

# Phase 4: React Alchemist

**Objective:** Build dynamic and scalable frontend applications.

## Modules

1. Introduction to React
2. Components and Props
3. State Management
4. Lifecycle Methods
5. Event Handling
6. React Hooks
7. React Router
8. Context API
9. Forms
10. Styling in React
11. Performance Optimization
12. Deployment
13. Advanced Patterns
14. Scalable Architecture
15. Next.js

### Technologies
- React
- JSX
- Hooks
- React Router
- Context API
- Redux
- Zustand
- Next.js
- Tailwind CSS
- ShadCN UI

---

# Phase 5: Deploy and AI Squad

**Objective:** Deploy applications to the cloud and build AI-powered solutions.

## Cloud Deployment Modules

1. Cloud Deployment Fundamentals
2. AWS EC2
3. Security Groups
4. Load Balancers
5. CloudFront
6. Docker
7. AWS ECS
8. AWS ECR
9. Target Groups
10. IAM & Security
11. Auto Scaling
12. CI/CD Pipelines
13. Monitoring & Logging
14. Cost Optimization
15. Security Best Practices

### AWS Services
- EC2
- ECS
- ECR
- CloudFront
- Elastic Load Balancer
- IAM
- CloudWatch
- CloudTrail

---

## Master AI

### Topics
- What is AI?
- Impact of AI
- Vector Databases
- Model Training
- AI Platforms
- Text Generation
- Image Generation
- Image Background Removal
- Text Summarization
- RAG Systems
- AI Application Development
- AI Project Work

### Technologies
- LLMs
- Vector Databases
- RAG
- Generative AI
- AI APIs

---
