# 1. **JavaScript Basics – The Language of the Web**

- Introduction to JavaScript and its role in web development
- Understanding variables and data types: `string`, `number`, `boolean`, `object`, `array`, `null`, `undefined`
- Declaring variables with `var`, `let`, `const`
- Understanding scope (Global, Local, Block Scope) and hoisting
- Basic operators: `+`, , , `/`, `%`, `==`, `===`
- Control flow statements: `if`, `else`, `else if`, `switch`, `ternary operator`
- **Key Concepts:** Variables, Data Types, Operators, Conditionals

# 2. **Functions – Building Blocks of JavaScript**

- What is a function and why it’s essential in JavaScript
- Function declaration vs function expression
- Arrow functions and their syntax
- Understanding the `return` statement and function parameters
- Function scope and closures
- **Key Concepts:** Function declaration, Function expression, Arrow functions, Closures, Parameters, Return

# 3. **Arrays and Objects – Working with Data**

- Creating and manipulating arrays: `push`, `pop`, `shift`, `unshift`, `map`, `filter`, `reduce`
- Understanding objects: properties, methods, and prototypes
- Accessing and modifying object properties
- Iterating over arrays and objects using loops (`for`, `for...of`, `for...in`)
- **Key Concepts:** Arrays, Objects, Loops, Array methods, Object methods

# 4. **Asynchronous JavaScript – Handling Time-sensitive Code**

- What is asynchronous programming and why it’s important
- Using `setTimeout` and `setInterval`
- Introduction to callbacks and callback hell
- Promises: What they are, how to create and use them
- `async` and `await` for handling asynchronous code in a more readable way
- **Key Concepts:** Callbacks, Promises, Async/Await, `setTimeout`, `setInterval`

# 5. **JavaScript and the DOM – Interacting with the Browser**

- What is the DOM (Document Object Model)?
- Accessing and modifying HTML elements with `document.getElementById()`, `document.querySelector()`, and `document.querySelectorAll()`
- Changing content using `innerHTML`, `textContent`, `value`
- Manipulating styles with `style` property and changing CSS dynamically
- Adding and removing elements with `appendChild()`, `removeChild()`, `insertBefore()`
- **Key Concepts:** DOM Manipulation, Querying elements, Modifying styles and content

# 6. **Event Handling – Making Web Pages Interactive**

- Introduction to events in JavaScript: `click`, `hover`, `keydown`, `submit`, etc.
- Event listeners and attaching them using `addEventListener()`
- Understanding event bubbling and capturing
- Preventing default behavior and stopping propagation with `event.preventDefault()` and `event.stopPropagation()`
- **Key Concepts:** Event handling, Event listeners, Event propagation

# 7. **Object-Oriented JavaScript – Mastering Objects and Classes**

- Introduction to object-oriented programming (OOP) in JavaScript
- Defining classes and objects in JavaScript
- Using constructors and `this` keyword
- Inheritance and the prototype chain
- Polymorphism and encapsulation
- **Key Concepts:** Classes, Objects, Constructors, Inheritance, Prototypes

# 8. **Advanced JavaScript Concepts – Deep Dive**

- Understanding closures and lexical scoping
- Understanding the `this` keyword in different contexts
- JavaScript `this` binding and call, apply, and bind methods
- JavaScript modules and how to use `import` and `export`
- Error handling in JavaScript with `try...catch` and custom errors
- **Key Concepts:** Closures, `this` keyword, Binding, Modules, Error handling

# 9. **JavaScript ES6+ Features – Modern JavaScript Syntax**

- Destructuring assignment for objects and arrays
- Template literals and string interpolation
- Default parameters, rest parameters, and spread syntax
- Introduction to `Map`, `Set`, `WeakMap`, `WeakSet`
- **Key Concepts:** ES6 syntax, Destructuring, Template literals, Spread/rest operators, `Map` & `Set`

___


# JavaScript Learning Guide
# Part 1: JavaScript Basics – The Language of the Web

---

# What is JavaScript?

JavaScript (JS) is a programming language used to make web pages interactive.

Think of a website as a car:

| Component | Technology |
|------------|------------|
| Car Body | HTML |
| Paint & Design | CSS |
| Engine & Controls | JavaScript |

Without JavaScript:

- Buttons do nothing
- Forms cannot validate
- Dynamic updates are impossible

With JavaScript:

- Buttons respond
- Data loads dynamically
- Animations occur
- Applications become interactive

---

# How JavaScript Works

Example:

```html
<button onclick="sayHello()">
    Click Me
</button>
```

```javascript
function sayHello() {
    alert("Hello World");
}
```

When user clicks:

```text
Button Click
     ↓
JavaScript Runs
     ↓
Alert Appears
```

---

# Variables

Variables store information.

Think of variables as labeled boxes.

```text
Name Box
↓
"Tauseef"
```

---

## Declaring Variables

### var

```javascript
var name = "John";
```

Old way.

---

### let

```javascript
let age = 25;
```

Modern and preferred.

---

### const

```javascript
const country = "India";
```

Cannot be reassigned.

---

## Comparison

```javascript
var city = "Bangalore";

let age = 25;

const pi = 3.14;
```

| Keyword | Reassign Allowed |
|----------|----------------|
| var | Yes |
| let | Yes |
| const | No |

---

# Data Types

Data Types define the kind of value stored.

---

## String

Text data.

```javascript
let name = "Tauseef";
```

---

## Number

```javascript
let age = 39;
```

---

## Boolean

```javascript
let isLoggedIn = true;
```

Values:

```javascript
true
false
```

---

## Array

Collection of values.

```javascript
let skills = [
    "HTML",
    "CSS",
    "JavaScript"
];
```

---

## Object

Stores data as key-value pairs.

```javascript
let user = {
    name: "Tauseef",
    age: 39
};
```

---

## Null

Intentional empty value.

```javascript
let data = null;
```

---

## Undefined

Variable declared but not assigned.

```javascript
let course;
```

Output:

```javascript
undefined
```

---

# Scope

Scope determines where a variable can be accessed.

---

## Global Scope

Accessible everywhere.

```javascript
let company = "Accenture";

function show() {
    console.log(company);
}
```

---

## Local Scope

Accessible only inside function.

```javascript
function show() {

    let city = "Bangalore";

}
```

Outside:

```javascript
console.log(city);
```

Error.

---

## Block Scope

Created by:

```javascript
{
}
```

Example:

```javascript
if(true){

    let score = 100;

}
```

Outside block:

```javascript
console.log(score);
```

Error.

---

# Hoisting

JavaScript moves declarations to top internally.

Example:

```javascript
console.log(name);

var name = "John";
```

Behaves like:

```javascript
var name;

console.log(name);

name = "John";
```

Output:

```javascript
undefined
```

---

# Operators

---

## Arithmetic Operators

```javascript
+
-
*
/
%
```

Example:

```javascript
10 + 5
```

Output:

```javascript
15
```

---

## Modulus Operator

Returns remainder.

```javascript
10 % 3
```

Output:

```javascript
1
```

---

## Equality Operators

### Loose Equality

```javascript
==
```

Converts types.

```javascript
5 == "5"
```

Output:

```javascript
true
```

---

### Strict Equality

```javascript
===
```

Checks value and type.

```javascript
5 === "5"
```

Output:

```javascript
false
```

---

# Conditionals

---

## if

```javascript
let age = 20;

if(age >= 18){
    console.log("Adult");
}
```

---

## if...else

```javascript
if(age >= 18){
    console.log("Adult");
}
else{
    console.log("Minor");
}
```

---

## else if

```javascript
if(score >= 90){
    console.log("A");
}
else if(score >= 75){
    console.log("B");
}
else{
    console.log("C");
}
```

---

## switch

```javascript
let day = 1;

switch(day){

    case 1:
        console.log("Monday");
        break;

    case 2:
        console.log("Tuesday");
        break;

    default:
        console.log("Unknown");
}
```

---

## Ternary Operator

Short form of if-else.

```javascript
let result =
age >= 18 ? "Adult" : "Minor";
```

---

# Key Concepts Summary

| Concept | Description |
|----------|-------------|
| Variable | Stores data |
| Data Type | Type of value |
| Scope | Accessibility of variables |
| Hoisting | Declaration moved up |
| Operator | Performs operation |
| Conditional | Decision making |

---

# Practice Exercise

Create variables for:

```javascript
name
age
city
isStudent
```

Use:

```javascript
if
else
switch
ternary
```

to display different outputs.

---

# Mini Project

## Student Grade Checker

Input:

```javascript
Marks
```

Output:

```text
A
B
C
Fail
```

Using:

```javascript
if
else if
```

---

---

# Part 2: Functions – Building Blocks of JavaScript

---

# What is a Function?

A function is a reusable block of code.

Think of a coffee machine.

```text
Press Button
     ↓
Coffee Produced
```

Function:

```text
Call Function
     ↓
Task Performed
```

---

# Function Declaration

```javascript
function greet(){

    console.log("Hello");

}
```

Call:

```javascript
greet();
```

Output:

```text
Hello
```

---

# Function Expression

```javascript
const greet =
function(){

    console.log("Hello");

};
```

---

# Arrow Functions

Modern syntax.

```javascript
const greet = () => {

    console.log("Hello");

};
```

---

# Parameters

Input values.

```javascript
function greet(name){

    console.log(name);

}
```

Call:

```javascript
greet("Tauseef");
```

Output:

```text
Tauseef
```

---

# Return Statement

Returns value.

```javascript
function add(a,b){

    return a + b;

}
```

Usage:

```javascript
let result =
add(10,20);
```

Output:

```javascript
30
```

---

# Function Scope

Variables inside function stay inside.

```javascript
function show(){

    let city = "Bangalore";

}
```

Cannot access outside.

---

# Closures

Closure remembers variables from outer function.

```javascript
function outer(){

    let count = 0;

    return function(){

        count++;

        console.log(count);

    }

}
```

```javascript
const counter =
outer();

counter();
counter();
counter();
```

Output:

```text
1
2
3
```

Even after outer finishes, inner remembers count.

---

# Key Concepts Summary

| Concept | Description |
|----------|-------------|
| Function | Reusable code block |
| Parameter | Input |
| Return | Output |
| Declaration | Standard function |
| Expression | Function stored in variable |
| Arrow Function | Modern syntax |
| Closure | Remembers outer variables |

---

# Practice Exercise

Create functions:

```javascript
add()
subtract()
multiply()
divide()
```

Using:

```javascript
parameters
return
arrow functions
```

---

# Mini Project

## Calculator

Functions:

```javascript
add
subtract
multiply
divide
```

Return results dynamically.

---

---

# Part 3: Arrays and Objects – Working with Data

---

# Arrays

Store multiple values.

```javascript
let courses = [
    "HTML",
    "CSS",
    "JavaScript"
];
```

---

# Array Methods

---

## push()

Adds to end.

```javascript
courses.push("React");
```

---

## pop()

Removes from end.

```javascript
courses.pop();
```

---

## shift()

Removes first item.

```javascript
courses.shift();
```

---

## unshift()

Adds to beginning.

```javascript
courses.unshift("Git");
```

---

# map()

Transforms data.

```javascript
let numbers =
[1,2,3];

let doubled =
numbers.map(
n => n * 2
);
```

Output:

```javascript
[2,4,6]
```

---

# filter()

Filters data.

```javascript
let even =
numbers.filter(
n => n % 2 === 0
);
```

---

# reduce()

Reduces array to one value.

```javascript
let total =
numbers.reduce(
(sum,n)=>sum+n,
0
);
```

Output:

```javascript
6
```

---

# Objects

Objects store related data.

```javascript
const user = {

    name:"Tauseef",
    age:39

};
```

---

# Accessing Properties

Dot notation:

```javascript
user.name
```

Bracket notation:

```javascript
user["name"]
```

---

# Modifying Properties

```javascript
user.age = 40;
```

---

# Methods

Functions inside objects.

```javascript
const user = {

    greet(){

        console.log("Hello");

    }

};
```

---

# Loops

---

## for Loop

```javascript
for(
let i=0;
i<5;
i++
){

    console.log(i);

}
```

---

## for...of

Arrays.

```javascript
for(
let course
of courses
){

    console.log(course);

}
```

---

## for...in

Objects.

```javascript
for(
let key
in user
){

    console.log(key);

}
```

---

# Key Concepts Summary

| Concept | Description |
|----------|-------------|
| Array | List of values |
| Object | Key-value data |
| Loop | Repetition |
| map | Transform |
| filter | Select |
| reduce | Aggregate |

---

# Mini Project

## Course Management App

Features:

```javascript
Add Course
Remove Course
Display Courses
Count Courses
```

Using:

```javascript
arrays
objects
loops
```

---

# JavaScript Learning Path So Far

```text
Variables
    ↓
Data Types
    ↓
Operators
    ↓
Conditionals
    ↓
Functions
    ↓
Closures
    ↓
Arrays
    ↓
Objects
    ↓
Loops
    ↓
Array Methods
```

---

# Challenge Project

Build a Student Management System.

Requirements:

### Student Object

```javascript
name
age
course
marks
```

### Features

```javascript
Add Student
Remove Student
Display Students
Calculate Average Marks
Filter Passed Students
```

Concepts Used:

- Variables
- Functions
- Arrays
- Objects
- Loops
- map
- filter
- reduce

___

# JavaScript Learning Guide
# Part 4: Asynchronous JavaScript – Handling Time-Sensitive Code

---

# What is Asynchronous Programming?

Normally JavaScript executes code line by line.

```javascript
console.log("Step 1");
console.log("Step 2");
console.log("Step 3");
```

Output:

```text
Step 1
Step 2
Step 3
```

This is called **Synchronous Execution**.

---

## Real World Analogy

Imagine ordering food at a restaurant.

### Synchronous

```text
Order Food
Wait
Wait
Wait
Food Arrives
Then Continue Life
```

Very inefficient.

---

### Asynchronous

```text
Order Food
Continue Talking
Continue Working
Food Arrives Later
```

Much better.

---

# Why Asynchronous Programming Exists

Many tasks take time:

- API Calls
- Database Queries
- File Uploads
- Timers
- Network Requests

Instead of freezing the browser, JavaScript handles them asynchronously.

---

# JavaScript Runtime Model

```text
Call Stack
     ↓
Web APIs
     ↓
Callback Queue
     ↓
Event Loop
     ↓
Call Stack
```

This is how JavaScript appears to do multiple things simultaneously.

---

# setTimeout()

Runs code after a delay.

```javascript
setTimeout(() => {
    console.log("Hello");
}, 2000);
```

Output after 2 seconds:

```text
Hello
```

---

## Example

```javascript
console.log("Start");

setTimeout(() => {
    console.log("Middle");
}, 2000);

console.log("End");
```

Output:

```text
Start
End
Middle
```

Notice JavaScript doesn't wait.

---

# setInterval()

Runs repeatedly.

```javascript
setInterval(() => {
    console.log("Running...");
}, 1000);
```

Output:

```text
Running...
Running...
Running...
```

Every second.

---

# Callbacks

A callback is a function passed into another function.

---

## Example

```javascript
function greet(callback){

    console.log("Hello");

    callback();

}
```

```javascript
greet(() => {
    console.log("World");
});
```

Output:

```text
Hello
World
```

---

# Callback Hell

Nested callbacks become difficult to read.

```javascript
loginUser(user, () => {

    getProfile(() => {

        getOrders(() => {

            getPayments(() => {

                console.log("Done");

            });

        });

    });

});
```

Looks like a pyramid.

Problems:

- Hard to read
- Hard to debug
- Difficult maintenance

---

# Promises

Promises solve callback hell.

---

## What is a Promise?

A Promise represents a future value.

States:

```text
Pending
Resolved
Rejected
```

---

## Creating a Promise

```javascript
const promise =
new Promise((resolve, reject) => {

    let success = true;

    if(success){
        resolve("Success");
    }
    else{
        reject("Failed");
    }

});
```

---

## Consuming a Promise

```javascript
promise
.then(result => {
    console.log(result);
})
.catch(error => {
    console.log(error);
});
```

Output:

```text
Success
```

---

# Async/Await

Makes asynchronous code look synchronous.

---

## Promise Version

```javascript
fetchData()
.then(data => {
    console.log(data);
});
```

---

## Async Await Version

```javascript
async function loadData(){

    const data =
    await fetchData();

    console.log(data);

}
```

Much cleaner.

---

# Example

```javascript
function getUser(){

    return new Promise(resolve => {

        setTimeout(() => {

            resolve("Tauseef");

        },2000);

    });

}
```

```javascript
async function showUser(){

    const user =
    await getUser();

    console.log(user);

}
```

Output:

```text
Tauseef
```

---

# Key Concepts Summary

| Concept | Description |
|----------|-------------|
| Async | Doesn't block execution |
| setTimeout | Run later |
| setInterval | Run repeatedly |
| Callback | Function passed to another function |
| Promise | Future result |
| async/await | Cleaner promise handling |

---

# Practice Exercise

Create:

```javascript
setTimeout()
Promise
async/await
```

Display:

```text
Loading...
Data Loaded
```

after 3 seconds.

---

# Mini Project

## Fake API Simulator

Features:

- Show Loading
- Wait 2 seconds
- Display User Data

Use:

```javascript
Promise
async
await
setTimeout
```

---

---

# Part 5: JavaScript and the DOM – Interacting with the Browser

---

# What is the DOM?

DOM stands for:

```text
Document Object Model
```

Browser converts HTML into a tree structure.

---

## Example HTML

```html
<body>

    <h1>Hello</h1>

    <p>Welcome</p>

</body>
```

DOM Tree:

```text
Document
   |
  Body
  /  \
 H1   P
```

JavaScript can manipulate this tree.

---

# Selecting Elements

---

## getElementById()

HTML:

```html
<h1 id="title">
    Welcome
</h1>
```

JavaScript:

```javascript
const title =
document.getElementById("title");
```

---

# querySelector()

Returns first matching element.

```javascript
const heading =
document.querySelector("h1");
```

---

## Using Class

```javascript
document.querySelector(".card");
```

---

## Using ID

```javascript
document.querySelector("#title");
```

---

# querySelectorAll()

Returns multiple elements.

```javascript
const items =
document.querySelectorAll("li");
```

---

# Changing Content

---

## textContent

```javascript
title.textContent =
"JavaScript Mastery";
```

---

## innerHTML

```javascript
title.innerHTML =
"<span>Hello</span>";
```

Allows HTML insertion.

---

## value

Used with form inputs.

```javascript
input.value
```

---

# Changing Styles

---

## Direct Style Manipulation

```javascript
title.style.color =
"blue";
```

---

## Multiple Styles

```javascript
title.style.background =
"yellow";

title.style.fontSize =
"40px";
```

---

# Creating Elements

```javascript
const p =
document.createElement("p");
```

---

# appendChild()

```javascript
document.body.appendChild(p);
```

Adds element.

---

# removeChild()

```javascript
parent.removeChild(child);
```

Removes element.

---

# insertBefore()

```javascript
parent.insertBefore(
newElement,
existingElement
);
```

Adds before another element.

---

# Example

```javascript
const button =
document.createElement("button");

button.textContent =
"Click Me";

document.body.appendChild(button);
```

---

# Key Concepts Summary

| Concept | Description |
|----------|-------------|
| DOM | HTML represented as objects |
| getElementById | Select by ID |
| querySelector | Select first element |
| querySelectorAll | Select multiple |
| innerHTML | Change HTML |
| textContent | Change text |
| appendChild | Add element |

---

# Mini Project

## Dynamic To-Do List

Features:

```text
Add Task
Delete Task
Mark Complete
```

Using:

```javascript
DOM Manipulation
appendChild
removeChild
querySelector
```

---

---

# Part 6: Event Handling – Making Web Pages Interactive

---

# What is an Event?

An event is something that happens in the browser.

Examples:

```text
Click
Hover
Scroll
Submit
Key Press
```

---

# Event Listener

Listens for events.

---

## Example

HTML:

```html
<button id="btn">
    Click
</button>
```

JavaScript:

```javascript
const btn =
document.getElementById("btn");

btn.addEventListener(
    "click",
    () => {
        console.log("Clicked");
    }
);
```

Output:

```text
Clicked
```

---

# Common Events

---

## Click

```javascript
button.addEventListener(
"click",
handler
);
```

---

## Mouse Over

```javascript
button.addEventListener(
"mouseover",
handler
);
```

---

## Keydown

```javascript
document.addEventListener(
"keydown",
handler
);
```

---

## Submit

```javascript
form.addEventListener(
"submit",
handler
);
```

---

# Event Object

Every event provides information.

```javascript
button.addEventListener(
"click",
(event) => {

    console.log(event);

});
```

---

# preventDefault()

Stops default behavior.

Example:

```html
<form>
```

Normally:

```text
Submit
↓
Page Refresh
```

Prevent it:

```javascript
event.preventDefault();
```

---

# Event Bubbling

Events move upward.

Example:

```html
<div>
    <button>
        Click
    </button>
</div>
```

Click button:

```text
Button
   ↓
Div
   ↓
Body
```

---

# stopPropagation()

Stops bubbling.

```javascript
event.stopPropagation();
```

---

# Event Capturing

Opposite of bubbling.

```text
Body
 ↓
Div
 ↓
Button
```

Rarely used.

---

# Key Concepts Summary

| Concept | Description |
|----------|-------------|
| Event | Browser action |
| Listener | Watches event |
| Bubbling | Child → Parent |
| Capturing | Parent → Child |
| preventDefault | Stop default action |
| stopPropagation | Stop bubbling |

---

# Mini Project

## Interactive Counter

Features:

```text
Increase
Decrease
Reset
```

Using:

```javascript
Events
DOM
Functions
```

---

# JavaScript Roadmap So Far

```text
Variables
   ↓
Functions
   ↓
Arrays
   ↓
Objects
   ↓
Async JS
   ↓
DOM
   ↓
Events
```

---

# Challenge Project

## Notes Application

Features:

- Add Note
- Delete Note
- Search Note
- Auto Save

Concepts Used:

```javascript
Functions
Arrays
Objects
DOM
Events
Promises
```

This project combines everything learned from Parts 1–6.

___


# JavaScript Learning Guide
# Part 7: Object-Oriented JavaScript – Mastering Objects and Classes

---

# What is Object-Oriented Programming (OOP)?

Object-Oriented Programming is a way of organizing code around **objects**.

Instead of thinking about functions only:

```text
Function
Function
Function
Function
```

We group related data and behavior together.

---

# Real World Analogy

Imagine a Car.

A car has:

### Properties (Data)

```text
Brand
Color
Speed
Fuel
```

### Behaviors (Actions)

```text
Start()
Stop()
Accelerate()
Brake()
```

In JavaScript:

```javascript
Car Object
{
    brand,
    color,
    start(),
    stop()
}
```

---

# Objects

JavaScript objects store data and methods together.

```javascript
const car = {

    brand: "Toyota",

    color: "White",

    start() {
        console.log("Car Started");
    }

};
```

Access property:

```javascript
console.log(car.brand);
```

Output:

```text
Toyota
```

Call method:

```javascript
car.start();
```

Output:

```text
Car Started
```

---

# Why Classes?

Imagine creating 100 cars.

Without classes:

```javascript
const car1 = {...}
const car2 = {...}
const car3 = {...}
```

Lots of duplicate code.

Classes act like blueprints.

---

# Classes

A class defines how objects should be created.

```javascript
class Car {

}
```

---

# Creating a Class

```javascript
class Car {

    constructor(brand, color){

        this.brand = brand;

        this.color = color;

    }

}
```

---

# Creating Objects

```javascript
const car1 =
new Car("Toyota", "White");

const car2 =
new Car("Honda", "Black");
```

Output:

```javascript
Car {
   brand: "Toyota",
   color: "White"
}
```

---

# Constructor

A constructor runs automatically when object is created.

```javascript
constructor(name){

    this.name = name;

}
```

Think of it as object initialization.

---

# The `this` Keyword

Refers to the current object.

Example:

```javascript
class Student {

    constructor(name){

        this.name = name;

    }

}
```

```javascript
const s1 =
new Student("Tauseef");
```

Internally:

```javascript
s1.name = "Tauseef";
```

---

# Methods in Classes

```javascript
class Student {

    constructor(name){

        this.name = name;

    }

    greet(){

        console.log(
            `Hello ${this.name}`
        );

    }

}
```

Usage:

```javascript
s1.greet();
```

Output:

```text
Hello Tauseef
```

---

# Inheritance

Inheritance allows one class to reuse another class.

---

# Parent Class

```javascript
class Animal {

    speak(){

        console.log("Animal Sound");

    }

}
```

---

# Child Class

```javascript
class Dog extends Animal {

}
```

Usage:

```javascript
const dog =
new Dog();

dog.speak();
```

Output:

```text
Animal Sound
```

Dog inherited the method.

---

# Overriding Methods

Child class can replace parent behavior.

```javascript
class Dog extends Animal {

    speak(){

        console.log("Bark");

    }

}
```

Output:

```text
Bark
```

---

# Prototype Chain

JavaScript inheritance works through prototypes.

```text
dog
 ↓
Dog Prototype
 ↓
Animal Prototype
 ↓
Object Prototype
 ↓
null
```

When JavaScript can't find a property:

```javascript
dog.speak()
```

it searches upward.

---

# Encapsulation

Protecting data from direct access.

Example:

```javascript
class BankAccount {

    #balance = 0;

    deposit(amount){

        this.#balance += amount;

    }

}
```

Cannot access:

```javascript
account.#balance
```

Error.

---

# Polymorphism

Same method behaves differently.

```javascript
class Animal {

    speak(){

        console.log("Sound");

    }

}
```

```javascript
class Dog extends Animal {

    speak(){

        console.log("Bark");

    }

}
```

```javascript
class Cat extends Animal {

    speak(){

        console.log("Meow");

    }

}
```

Same method:

```javascript
speak()
```

Different behavior.

---

# Key Concepts Summary

| Concept | Description |
|----------|-------------|
| Class | Blueprint |
| Object | Instance of class |
| Constructor | Initializes object |
| this | Current object |
| Inheritance | Reuse parent code |
| Prototype | Inheritance mechanism |
| Encapsulation | Hide data |
| Polymorphism | Same method, different behavior |

---

# Practice Exercise

Create:

```javascript
Vehicle
Car
Bike
Truck
```

Use:

```javascript
class
constructor
inheritance
methods
```

---

# Mini Project

## Employee Management System

Class:

```javascript
Employee
```

Properties:

```javascript
name
department
salary
```

Methods:

```javascript
displayInfo()
calculateBonus()
```

---

---

# Part 8: Advanced JavaScript Concepts – Deep Dive

---

# Closures

One of the most important JavaScript concepts.

---

# Definition

A closure occurs when a function remembers variables from its outer scope even after the outer function has finished executing.

---

# Example

```javascript
function outer(){

    let counter = 0;

    return function(){

        counter++;

        console.log(counter);

    };

}
```

```javascript
const increment =
outer();

increment();
increment();
increment();
```

Output:

```text
1
2
3
```

---

# Why Does It Work?

Normally:

```javascript
outer()
```

finishes execution.

But inner function remembers:

```javascript
counter
```

through closure.

---

# Lexical Scope

JavaScript determines scope based on where code is written.

Example:

```javascript
function outer(){

    let name = "Tauseef";

    function inner(){

        console.log(name);

    }

    inner();

}
```

Output:

```text
Tauseef
```

Inner can access outer variables.

---

# Understanding `this`

One of the most confusing JavaScript topics.

---

# Rule 1: Global Context

Browser:

```javascript
console.log(this);
```

Output:

```javascript
window
```

---

# Rule 2: Object Method

```javascript
const user = {

    name: "Tauseef",

    greet(){

        console.log(this.name);

    }

};
```

Output:

```text
Tauseef
```

Here:

```javascript
this = user
```

---

# Rule 3: Regular Function

```javascript
function show(){

    console.log(this);

}
```

In strict mode:

```javascript
undefined
```

---

# Rule 4: Arrow Functions

Arrow functions do NOT have their own `this`.

They inherit from parent.

```javascript
const user = {

    name:"Tauseef",

    greet(){

        const fn = () => {

            console.log(this.name);

        }

        fn();

    }

}
```

Output:

```text
Tauseef
```

---

# call()

Invokes function immediately with custom `this`.

```javascript
function greet(){

    console.log(this.name);

}
```

```javascript
greet.call({
    name:"Tauseef"
});
```

Output:

```text
Tauseef
```

---

# apply()

Same as call but arguments passed as array.

```javascript
function add(a,b){

    console.log(a+b);

}
```

```javascript
add.apply(null,[10,20]);
```

Output:

```text
30
```

---

# bind()

Creates new function.

```javascript
const greetUser =
greet.bind({
    name:"Tauseef"
});
```

Later:

```javascript
greetUser();
```

Output:

```text
Tauseef
```

---

# Modules

Modules split code into multiple files.

Benefits:

- Better organization
- Reusability
- Maintainability

---

# Export

math.js

```javascript
export function add(a,b){

    return a+b;

}
```

---

# Import

app.js

```javascript
import { add }
from "./math.js";
```

Usage:

```javascript
console.log(add(10,20));
```

Output:

```text
30
```

---

# Error Handling

Applications fail.

Good developers handle failures gracefully.

---

# try...catch

```javascript
try {

    let result =
    10 / 0;

}
catch(error){

    console.log(error);

}
```

---

# Throwing Custom Errors

```javascript
function validateAge(age){

    if(age < 18){

        throw new Error(
            "Age must be 18+"
        );

    }

}
```

---

# Key Concepts Summary

| Concept | Description |
|----------|-------------|
| Closure | Function remembers variables |
| Lexical Scope | Scope based on location |
| this | Current execution context |
| call | Execute with custom this |
| apply | Call using array arguments |
| bind | Create new function |
| Module | Separate files |
| try/catch | Handle errors |

---

# Practice Exercise

Create:

```javascript
Counter Closure
Custom Error
Module
call()
apply()
bind()
```

---

# Mini Project

## Banking Application

Features:

```text
Deposit
Withdraw
Balance Check
Validation
```

Concepts:

```javascript
Closures
Classes
Error Handling
Modules
```

---

---

# Part 9: JavaScript ES6+ Features – Modern JavaScript Syntax

---

# Why ES6?

Before ES6:

```javascript
More Code
More Complexity
```

After ES6:

```javascript
Cleaner
Shorter
More Readable
```

---

# Destructuring

Extract values from arrays and objects.

---

# Array Destructuring

```javascript
const skills = [
    "HTML",
    "CSS",
    "JavaScript"
];
```

Old:

```javascript
const first =
skills[0];
```

ES6:

```javascript
const [
    first,
    second
] = skills;
```

Output:

```text
HTML
CSS
```

---

# Object Destructuring

```javascript
const user = {

    name:"Tauseef",
    age:39

};
```

```javascript
const {
    name,
    age
} = user;
```

---

# Template Literals

Old:

```javascript
"Hello " + name
```

ES6:

```javascript
`Hello ${name}`
```

Example:

```javascript
const name =
"Tauseef";

console.log(
`Hello ${name}`
);
```

Output:

```text
Hello Tauseef
```

---

# Default Parameters

```javascript
function greet(
    name="Guest"
){

    console.log(name);

}
```

```javascript
greet();
```

Output:

```text
Guest
```

---

# Rest Parameters

Collect multiple values.

```javascript
function total(...numbers){

    console.log(numbers);

}
```

Call:

```javascript
total(
1,2,3,4
);
```

Output:

```javascript
[1,2,3,4]
```

---

# Spread Operator

Expands arrays and objects.

---

# Array Spread

```javascript
const arr1 =
[1,2,3];

const arr2 =
[...arr1,4,5];
```

Output:

```javascript
[1,2,3,4,5]
```

---

# Object Spread

```javascript
const user = {
    name:"Tauseef"
};

const updated = {

    ...user,
    city:"Bangalore"

};
```

---

# Map

Stores key-value pairs.

---

# Creating Map

```javascript
const users =
new Map();
```

```javascript
users.set(
1,
"Tauseef"
);
```

Retrieve:

```javascript
users.get(1);
```

Output:

```text
Tauseef
```

---

# Set

Stores unique values.

```javascript
const numbers =
new Set([
1,2,2,3,3
]);
```

Output:

```javascript
{1,2,3}
```

Duplicates removed.

---

# WeakMap

Keys must be objects.

```javascript
const wm =
new WeakMap();
```

Allows garbage collection.

Used for private data.

---

# WeakSet

Stores object references only.

```javascript
const ws =
new WeakSet();
```

---

# Key Concepts Summary

| Concept | Description |
|----------|-------------|
| Destructuring | Extract values |
| Template Literal | String interpolation |
| Default Parameter | Default values |
| Rest | Collect values |
| Spread | Expand values |
| Map | Advanced key-value storage |
| Set | Unique values |
| WeakMap | Object keys only |
| WeakSet | Object storage |

---

# Complete JavaScript Roadmap

```text
JavaScript Basics
        ↓
Variables & Data Types
        ↓
Operators & Conditionals
        ↓
Functions
        ↓
Arrays & Objects
        ↓
DOM Manipulation
        ↓
Event Handling
        ↓
Asynchronous JavaScript
        ↓
Classes & OOP
        ↓
Closures
        ↓
this Keyword
        ↓
call / apply / bind
        ↓
Modules
        ↓
Error Handling
        ↓
ES6+
        ↓
Modern Frontend Development
        ↓
React
        ↓
Node.js
        ↓
Full Stack JavaScript
```

---

# Final Challenge Project

## Learning Management System (LMS)

Build a complete LMS using all JavaScript concepts.

### Features

#### User Management

```javascript
Register
Login
Logout
```

#### Course Management

```javascript
Add Course
Edit Course
Delete Course
```

#### Student Management

```javascript
Enroll Student
Track Progress
Generate Reports
```

#### Technical Concepts Used

```javascript
Variables
Functions
Arrays
Objects
DOM
Events
Promises
Async/Await
Classes
Inheritance
Modules
Error Handling
ES6+
```

This single project will reinforce nearly every JavaScript concept from beginner to advanced level and prepare you for learning React, Node.js, and modern full-stack development.
