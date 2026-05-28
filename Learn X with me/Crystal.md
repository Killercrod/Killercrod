
# Crystal

** Crystal
In this markdown we are going to talk about the basics of Crystal and how to use it to build simple, high-performance programs.

By the end of this guide you will be able to:
- Understand what Crystal is used for
- Read the basic structure of a Crystal file
- Compile and run simple Crystal programs

This guide is for people who are new to Crystal or who want a concise, practical overview.

## Before You Start

You do not need to know everything before learning Crystal. It is enough to:

- Know basic programming concepts (variables, functions)
- Understand that Crystal has a syntax similar to Ruby
- Be comfortable compiling code from the command line

## Basic Structure

This is the basic structure of a Crystal program.

```crystal
# Hello World
puts "Hello, Crystal!"

# Comments
# Single-line comment
"""Multi-line string used as doc/comment"""
```

** puts "Hello, Crystal!"
This prints text to the console.
Why is it necessary? It is the simplest way to see output and test your program.

** Comments
Comments help you document your code and explain intent.

## Variables, Types, and Methods in Simple Words

Crystal is statically typed but offers type inference. You can annotate types when needed.

```crystal
name = "Ana"          # String (inferred)
age : Int32 = 30       # Explicit type
pi = 3.14              # Float64 (inferred)
```

## Methods

```crystal
def greet(name : String)
  "Hello, #{name}!"
end

puts greet("World")
```

## Object-Oriented Programming

```crystal
class Person
  property name : String

  def initialize(@name : String)
  end

  def greet
    puts "Hello, #{@name}"
  end
end

Person.new("Ana").greet
```

## Concurrency

Crystal provides lightweight concurrency with `spawn` and `Channel`.

```crystal
channel = Channel(String).new

spawn do
  channel.send("message from fiber")
end

puts channel.receive
```

## Packages and Shards

- The dependency manager is called `shards`.
- Initialize a project with `shards init` and add dependencies to `shard.yml`.
- Install dependencies with `shards install`.

## Compile and Run

- Run directly: `crystal run file.cr`
- Compile release build: `crystal build file.cr --release`

## Common Beginner Exercises

1. Print a greeting to the console.
   Expected result: The message appears when you run the program.

2. Create a `Person` class with a `greet` method.
   Expected result: Calling `Person.new("Name").greet` prints the greeting.

3. Spawn a fiber that sends a message through a channel.
   Expected result: The main program receives and prints the message.

## Common Beginner Mistakes

- I get a compile error.
  Check the exact error message and the line it points to.

- My type is wrong.
  Add or adjust a type annotation (e.g., `: Int32`).

- My program doesn't run.
  Ensure you used `crystal run` or compiled the binary.

## What to Learn Next

- Macros and metaprogramming
- Foreign Function Interface (FFI) with C libraries
- Concurrency patterns and performance tuning

## Key Points to Remember

- Crystal offers Ruby-like syntax with static types and compiled performance
- Use `shards` to manage dependencies
- `crystal run` for quick tests, `crystal build --release` for optimized binaries

For more examples or a Spanish-translated version, tell me which you'd prefer.
