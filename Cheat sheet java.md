Java Cheat Sheet

Table of Contents

Basic Syntax
Data Types
Operators
Control Flow
Object-Oriented Programming
Collections Framework
Exception Handling
Input/Output
Useful Methods
Basic Syntax

java
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
Data Types

Primitive Types

java
byte b = 127;           // 8-bit integer
short s = 32767;        // 16-bit integer
int i = 2147483647;     // 32-bit integer
long l = 9223372036854775807L;  // 64-bit integer

float f = 3.14f;        // 32-bit floating point
double d = 3.1415926535; // 64-bit floating point

char c = 'A';           // 16-bit Unicode character
boolean bool = true;    // true or false
Non-Primitive Types

java
// Strings
String str = "Hello";
String str2 = new String("Hello");

// Arrays
int[] numbers = {1, 2, 3, 4, 5};
String[] names = new String[10];
Operators

java
// Arithmetic
int result = 10 + 5;    // +, -, *, /, %

// Assignment
int x = 10;             // =, +=, -=, *=, /=, %=

// Comparison
boolean isEqual = (a == b);     // ==, !=, <, >, <=, >=

// Logical
boolean result = (a > b) && (c < d);  // &&, ||, !

// Ternary
int max = (a > b) ? a : b;
Control Flow

Conditional Statements

java
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
Loops

java
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
Object-Oriented Programming

Classes and Objects

java
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
Inheritance

java
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
Interfaces

java
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
Abstraction

java
public abstract class Animal {
    public abstract void makeSound();
    
    public void sleep() {
        System.out.println("Sleeping...");
    }
}
Polymorphism

java
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
Collections Framework

Common Collections

java
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
Iterating Collections

java
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
Exception Handling

java
try {
    // code that might throw exception
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
Input/Output

Basic I/O

java
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
Useful Methods

String Methods

java
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
Array Methods

java
int[] numbers = {1, 2, 3, 4, 5};

Arrays.sort(numbers);
Arrays.toString(numbers);
Arrays.copyOf(numbers, numbers.length);
Arrays.fill(numbers, 0);
Math Methods

java
Math.max(10, 20);       // 20
Math.min(10, 20);       // 10
Math.abs(-10);          // 10
Math.sqrt(25);          // 5.0
Math.pow(2, 3);         // 8.0
Math.round(3.14);       // 3
Key Points to Remember

Java is case-sensitive
Every statement ends with a semicolon
Code blocks are enclosed in curly braces {}
The main method is the entry point of any Java application
Java uses garbage collection for memory management
All Java objects are stored in the heap memory
Java supports multithreading
Use final for constants and to prevent inheritance/method overriding
This cheat sheet covers the essential Java concepts. Keep practicing and referring to the official Java documentation for more detailed information!
