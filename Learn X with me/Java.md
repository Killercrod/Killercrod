** Java
In this markdown we are going to talk about the basics of Java and how to use it to build your first programs.

By the end of this guide you will be able to:
- Understand the basic structure of a Java program
- Know the most common Java building blocks
- Practice the first things you should learn before moving on

This guide is for people who are new to Java, or for people who want a simple refresh without too much technical language.

First, we need to understand when we use Java. We use Java when we want to build programs, applications, and logic that can run in many different environments. It is a good idea to learn it step by step and keep things organized.

## Before You Start

You do not need to know everything before learning Java. It is enough to:

- Know how to read simple code
- Understand basic logic like "if this, then that"
- Be comfortable with practice and repetition
- Not be afraid of mistakes, because they are part of learning

## Basic Structure

This is the basic structure of a Java program. It is important to know why it is ordered like this.

```java
// Hello World
public class HelloWorld {
    public static void main(String[] args) {
        System.out.println("Hello, World!");
    }
}

// Comments
// Single-line comment
/* Multi-line comment */
/** Documentation comment */
```

I will explain why it is ordered like this and why it is important to know this.

** public class HelloWorld
This is the class that holds the program.
Why is it necessary? In Java, code usually lives inside classes.

** public static void main(String[] args)
This is the main method.
Why is it necessary? It is the entry point of the program, so Java starts running from here.

** System.out.println("Hello, World!")
This prints text in the console.
Why is it necessary? It is the simplest way to see output and test that your program works.

** Comments
Comments help you write notes inside your code.
Why are they useful? They make code easier to understand when you come back later.

## Data Types

Before we go into the list, it helps to think about variables like small boxes. A variable stores a value, and the data type tells Java what kind of value that box should hold.

### Primitive Types

```java
byte b = 127;           // 8-bit integer
short s = 32767;        // 16-bit integer
int i = 2147483647;     // 32-bit integer
long l = 9223372036854775807L;  // 64-bit integer

float f = 3.14f;         // 32-bit floating point
double d = 3.1415926535; // 64-bit floating point

char c = 'A';            // 16-bit Unicode character
boolean bool = true;     // true or false
```

### Non-Primitive Types

```java
// Strings
String str = "Hello";
String str2 = new String("Hello");

// Arrays
int[] numbers = {1, 2, 3, 4, 5};
String[] names = new String[10];
```

## Variables, Data Types, and Operators in Simple Words

A variable is like a labeled box. You put something inside it so you can use it later.

The data type tells Java what kind of thing is inside the box. For example, a number, a decimal, a letter, or a true/false value.

Operators are the symbols that help you work with those values. Some operators do math, some compare values, and some help you change a variable.

## Operators

If you want a simpler way to remember them:

- Arithmetic operators help you calculate things
- Comparison operators help you ask questions about values
- Logical operators help you combine conditions
- Assignment operators help you update variables

```java
// Arithmetic
int result = 10 + 5;    // +, -, *, /, %

// Assignment
int x = 10;             // =, +=, -=, *=, /=, %=

// Comparison
boolean isEqual = (a == b);     // ==, !=, <, >, <=, >=

// Logical
boolean logicResult = (a > b) && (c < d);  // &&, ||, !

// Ternary
int max = (a > b) ? a : b;
```

## Control Flow

### Conditional Statements

```java
// if-else
if (condition) {
    // code
} else if (anotherCondition) {
    // code
} else {
    // code
}

// switch
switch (variable) {
    case 1:
        // code
        break;
    case 2:
        // code
        break;
    default:
        // code
}
```

### Loops

```java
// for loop
for (int i = 0; i < 10; i++) {
    // code
}

// enhanced for loop
for (String name : names) {
    // code
}

// while loop
while (condition) {
    // code
}

// do-while
do {
    // code
} while (condition);
```

## Object-Oriented Programming

Java is built around this idea a lot, so it is worth slowing down here.

Think of it like this:

- A class is the blueprint
- An object is the real thing created from that blueprint
- A method is something the object can do

### Classes and Objects

```java
// Class definition
public class Car {
    // Fields
    private String brand;
    private int year;

    // Constructor
    public Car(String brand, int year) {
        this.brand = brand;
        this.year = year;
    }

    // Methods
    public void start() {
        System.out.println("Car started");
    }

    // Getters and setters
    public String getBrand() { return brand; }
    public void setBrand(String brand) { this.brand = brand; }
}

// Creating objects
Car myCar = new Car("Toyota", 2020);
```

### Packages and Imports

Packages are like folders for code. They help organize classes so everything does not live in one giant pile.

Imports let you use classes from other packages without writing the full path every time.

```java
import java.util.ArrayList;
import java.util.List;

List<String> names = new ArrayList<>();
```

Why this matters:

- Packages keep code organized
- Imports save time and make code easier to read
- You usually see them at the top of a file

### Inheritance

```java
public class Vehicle {
    protected String brand;

    public void honk() {
        System.out.println("Beep beep!");
    }
}

public class Car extends Vehicle {
    private int doors;

    public Car(String brand, int doors) {
        this.brand = brand;
        this.doors = doors;
    }
}
```

### Interfaces

```java
public interface Drivable {
    void drive();
    void stop();
}

public class Car implements Drivable {
    public void drive() {
        System.out.println("Car is driving");
    }

    public void stop() {
        System.out.println("Car stopped");
    }
}
```

### Abstraction

```java
public abstract class Animal {
    public abstract void makeSound();

    public void sleep() {
        System.out.println("Sleeping...");
    }
}
```

### Polymorphism

```java
// Method overloading
public class Calculator {
    public int add(int a, int b) {
        return a + b;
    }

    public double add(double a, double b) {
        return a + b;
    }
}

// Method overriding
public class Animal {
    public void makeSound() {
        System.out.println("Animal sound");
    }
}

public class Dog extends Animal {
    @Override
    public void makeSound() {
        System.out.println("Woof woof!");
    }
}
```

## Collections Framework

### Common Collections

```java
import java.util.*;

// List
List<String> list = new ArrayList<>();
list.add("Apple");
list.add("Banana");

// Set
Set<Integer> set = new HashSet<>();
set.add(1);
set.add(2);

// Map
Map<String, Integer> map = new HashMap<>();
map.put("Apple", 1);
map.put("Banana", 2);

// Queue
Queue<String> queue = new LinkedList<>();
queue.add("First");
queue.add("Second");
```

### Arrays and ArrayList

These two are easy to mix up, so here is a simple way to remember them.

- An array is fixed in size
- An ArrayList can grow or shrink more easily
- Arrays are useful when you already know the exact amount of items
- ArrayList is useful when the list may change

```java
// Array
int[] fixedNumbers = {1, 2, 3};

// ArrayList
ArrayList<String> flexibleList = new ArrayList<>();
flexibleList.add("Apple");
flexibleList.add("Banana");
```

If you want the shortest version:

- Use an array when the size is simple and fixed
- Use ArrayList when you need to add or remove items often

### Iterating Collections

```java
// For-each loop
for (String item : list) {
    System.out.println(item);
}

// Iterator
Iterator<String> iterator = list.iterator();
while (iterator.hasNext()) {
    System.out.println(iterator.next());
}

// For loop with index
for (int i = 0; i < list.size(); i++) {
    System.out.println(list.get(i));
}
```

## Exception Handling

```java
try {
    // code that might throw an exception
    int result = 10 / 0;
} catch (ArithmeticException e) {
    System.out.println("Cannot divide by zero!");
} catch (Exception e) {
    System.out.println("Something went wrong!");
} finally {
    System.out.println("This always executes");
}

// Throwing exceptions
public void checkAge(int age) throws IllegalArgumentException {
    if (age < 0) {
        throw new IllegalArgumentException("Age cannot be negative");
    }
}
```

## Input and Output

### Basic I/O

```java
import java.util.Scanner;

// Reading input
Scanner scanner = new Scanner(System.in);
System.out.print("Enter your name: ");
String name = scanner.nextLine();
System.out.print("Enter your age: ");
int age = scanner.nextInt();

// File I/O
import java.io.*;

// Writing to file
try (FileWriter writer = new FileWriter("file.txt")) {
    writer.write("Hello World!");
}

// Reading from file
try (BufferedReader reader = new BufferedReader(new FileReader("file.txt"))) {
    String line = reader.readLine();
    System.out.println(line);
}
```

## Useful Methods

### String Methods

```java
String str = "Hello World";

str.length();           // 11
str.charAt(1);          // 'e'
str.substring(6);       // "World"
str.substring(0, 5);    // "Hello"
str.indexOf("World");   // 6
str.toUpperCase();      // "HELLO WORLD"
str.toLowerCase();      // "hello world"
str.trim();             // removes whitespace
str.split(" ");         // ["Hello", "World"]
```

### Array Methods

```java
int[] numbers = {1, 2, 3, 4, 5};

Arrays.sort(numbers);
Arrays.toString(numbers);
Arrays.copyOf(numbers, numbers.length);
Arrays.fill(numbers, 0);
```

### Math Methods

```java
Math.max(10, 20);       // 20
Math.min(10, 20);       // 10
Math.abs(-10);          // 10
Math.sqrt(25);          // 5.0
Math.pow(2, 3);         // 8.0
Math.round(3.14);       // 3
```

## Basic Exercises

1. Create a class that prints your name.
Expected result: You should see your name in the console.

2. Create two variables and add them.
Expected result: You should see the sum printed in the console.

3. Use an if statement to check if a number is positive.
Expected result: The program should tell you if the number is positive or not.

4. Create a list and print all its values.
Expected result: You should see every item printed one by one.

5. Create a simple import and use it in your program.
Expected result: Your code should compile without saying the class cannot be found.

## Common Beginner Mistakes

- My program does not run.
Check if the class name and file name match.

- My main method does not seem to work.
Check if it is written exactly as public static void main(String[] args).

- I get an error in main.
Check if the main method is written exactly as Java expects it.

- My output does not appear.
Check if you used System.out.println correctly.

- My imports are failing.
Check if you imported the correct package.

- My ArrayList gives an error.
Check if you imported java.util.ArrayList or java.util.*.

## What to Learn Next

- Java syntax basics (practice with small programs)
- Object-oriented programming in more depth
- Collections and arrays
- Exception handling with real examples
- File handling and user input

## Key Points to Remember

- Java is case-sensitive
- Every statement ends with a semicolon
- Code blocks are enclosed in curly braces {}
- The main method is the entry point of any Java application
- Java uses garbage collection for memory management
- All Java objects are stored in heap memory
- Java supports multithreading
- Use final for constants and to prevent inheritance or method overriding

This cheat sheet covers the essential Java concepts. Keep practicing and referring to the official Java documentation for more detailed information.
