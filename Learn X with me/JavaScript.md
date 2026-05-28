** JavaScript
In this markdown we are going to talk about the basics of JavaScript and how to use it to make webpages interactive.

By the end of this guide you will be able to:
- Understand what JavaScript is used for
- Read the basic structure of a JavaScript file
- Practice the first things you should learn before moving on

This guide is for people who are new to JavaScript, or for people who want a simple refresher without too much technical language.

First, we need to understand when we use JavaScript. We use JavaScript when we want to add behavior to a webpage. HTML gives the structure, CSS gives the style, and JavaScript gives the interaction. It is a good idea to keep those parts separate so the project stays organized.

## Before You Start

You do not need to know everything before learning JavaScript. It is enough to:

- Know the basics of HTML and CSS
- Understand that JavaScript makes things happen
- Be comfortable with practice and repetition
- Not be afraid of mistakes, because they are part of learning

## Basic Structure

This is the basic structure of a simple JavaScript file. It is important to know why it is written like this.

```javascript
// Hello World
console.log("Hello, World!");

// Comments
// Single-line comment
/* Multi-line comment */
```

I will explain why it is written like this and why it is important to know this.

** console.log("Hello, World!")
This prints text in the console.
Why is it necessary? It is the simplest way to see output and test that your code works.

** Comments
Comments help you write notes inside your code.
Why are they useful? They make code easier to understand when you come back later.

## Variables, Data Types, and Operators in Simple Words

A variable is like a labeled box. You put something inside it so you can use it later.

The data type tells JavaScript what kind of thing is inside the box. For example, a number, text, or a true/false value.

Operators are the symbols that help you work with those values. Some operators do math, some compare values, and some help you change a variable.

## Variables and Data Types

```javascript
// Variables
let name = "Ana";
const age = 20;
var city = "Madrid";

// Strings
let message = "Hello";

// Numbers
let integerNumber = 10;
let decimalNumber = 3.14;

// Booleans
let isActive = false;
```

If you want a simple way to remember them:

- Text values are strings
- Whole numbers are numbers
- Decimal numbers are also numbers
- True or false values are booleans

## Let, Const, and Var

These are used to create variables.

- `let` is for values that can change
- `const` is for values that should stay the same
- `var` is the older way and you will usually see it less in modern code

```javascript
let score = 10;
score = 15;

const pi = 3.1416;
```

## Operators

If you want a simpler way to remember them:

- Arithmetic operators help you calculate things
- Comparison operators help you ask questions about values
- Logical operators help you combine conditions
- Assignment operators help you update variables

```javascript
// Arithmetic
let result = 10 + 5;   // +, -, *, /, %

// Assignment
let x = 10;
x += 2;

// Comparison
let isEqual = (a === b);   // ===, !==, <, >, <=, >=

// Logical
let logicResult = (a > b) && (c < d);   // &&, ||, !

// Ternary
let maxValue = a > b ? a : b;
```

## Basic Structure of a JavaScript File

JavaScript can start very simply and still work.

```javascript
console.log("First line");
console.log("Second line");
```

If you want to organize bigger programs, you can use functions.

```javascript
function greet(name) {
	console.log(`Hello, ${name}!`);
}

greet("Ana");
```

## Functions

A function is a reusable piece of code. Instead of writing the same logic many times, you put it in one place and call it when you need it.

```javascript
function add(a, b) {
	return a + b;
}

let result = add(3, 5);
console.log(result);
```

Why functions are useful:

- They keep code cleaner
- They help you reuse logic
- They make programs easier to read

## Control Flow

### Conditional Statements

```javascript
if (condition) {
	// code
} else if (anotherCondition) {
	// code
} else {
	// code
}
```

### Loops

```javascript
// for loop
for (let i = 0; i < 5; i++) {
	console.log(i);
}

// for...of loop
let names = ["Ana", "Luis", "Maria"];
for (let name of names) {
	console.log(name);
}

// while loop
let count = 0;
while (count < 3) {
	console.log(count);
	count++;
}
```

## Data Collections

JavaScript uses simple structures to store multiple values.

### Arrays

```javascript
let fruits = ["apple", "banana", "orange"];
fruits.push("grape");
console.log(fruits);
```

### Objects

```javascript
let person = {
	name: "Ana",
	age: 20
};

console.log(person.name);
```

### Arrays and Objects Compared Simply

- An array is a list of values
- An object is a group of named values
- Use an array when order matters more
- Use an object when names matter more

## DOM Basics

The DOM is how JavaScript reads and changes what you see on the page.

```javascript
const title = document.querySelector("h1");
title.textContent = "New Title";
```

Why this matters:

- It lets JavaScript change the page
- It helps create buttons, forms, menus, and interactions
- It is one of the most important parts of frontend JavaScript

## Events

Events happen when the user does something.

```javascript
const button = document.querySelector("button");

button.addEventListener("click", function () {
	console.log("Button clicked!");
});
```

Simple idea:

- A click is an event
- A key press is an event
- A form submit is an event

## Classes and Objects

JavaScript also uses classes.

Think of it like this:

- A class is the blueprint
- An object is the real thing created from that blueprint
- A method is something the object can do

```javascript
class Car {
	constructor(brand, year) {
		this.brand = brand;
		this.year = year;
	}

	start() {
		console.log("Car started");
	}
}

const myCar = new Car("Toyota", 2020);
myCar.start();
```

## Exceptions

Sometimes things go wrong, and JavaScript gives you a way to handle that without breaking the whole program.

```javascript
try {
	let result = 10 / 0;
	console.log(result);
} catch (error) {
	console.log("Something went wrong!");
} finally {
	console.log("This always runs");
}
```

## Basic Browser Storage

JavaScript can store small values in the browser.

```javascript
localStorage.setItem("name", "Ana");
let savedName = localStorage.getItem("name");
console.log(savedName);
```

## Useful Methods

### String Methods

```javascript
let text = "Hello World";

text.length;
text.toLowerCase();
text.toUpperCase();
text.trim();
text.split(" ");
text.replace("World", "JavaScript");
```

### Array Methods

```javascript
let numbers = [1, 2, 3, 4, 5];

numbers.push(6);
numbers.pop();
numbers.sort();
numbers.includes(3);
numbers.map(num => num * 2);
```

### Math Examples

```javascript
Math.sqrt(25);
Math.pow(2, 3);
Math.floor(3.8);
Math.ceil(3.2);
Math.random();
```

## Basic Exercises

1. Print your name in the console.
Expected result: You should see your name in the console.

2. Create two variables and add them.
Expected result: You should see the sum printed in the console.

3. Use an if statement to check if a number is positive.
Expected result: The program should tell you if the number is positive or not.

4. Create an array and print all its values.
Expected result: You should see every item printed one by one.

5. Change the text of an element on the page.
Expected result: The text on the page should update.

6. Add a click event to a button.
Expected result: Something should happen when you click the button.

## Common Beginner Mistakes

- My program does not run.
Check if your syntax is correct.

- My function does not work.
Check if you wrote the function name correctly and called it the right way.

- My DOM code does not work.
Check if the element exists before you try to select it.

- My output does not appear.
Check if you used console.log() correctly.

- My code gives an error in the browser.
Check the browser console for the message.

## What to Learn Next

- JavaScript syntax basics (practice with small programs)
- Functions and parameters in more depth
- Arrays and objects
- DOM manipulation
- Events and event listeners
- Async JavaScript and fetch

## Key Points to Remember

- JavaScript adds behavior to webpages
- Variables store values you can reuse
- Functions help you organize code
- Arrays and objects are very common
- DOM lets JavaScript change the page
- Events help users interact with the page
- Practice is the best way to learn JavaScript

This guide covers the essential JavaScript concepts. Keep practicing and referring to the official JavaScript documentation for more detailed information.
