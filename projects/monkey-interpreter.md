---
layout: page
title: Monkey Interpreter
permalink: /projects/monkey-interpreter.html
---

<em>Credit: building while following <a href="https://interpreterbook.com/">Writing an Interpreter in Go</a> by Thorsten Ball — work in progress.</em><br>
<em>Repo: <a href="https://github.com/bhomik005/monkey">github.com/bhomik005/monkey</a></em>

### Difference Between Interpreters and Compilers
Interpreters take the source code as input and execute it line by line. They produce results immediately without generating intermediary files or binaries. Compilers, on the other hand, translate the source code into another language (often machine code) that the underlying system can execute directly.

### What We Are Going to Build
We will build a tree-walking interpreter that parses source code, constructs an abstract syntax tree (AST), and evaluates that tree. To accomplish this we need:

- a lexer
- a parser
- a tree representation
- an evaluator

### Planned Features
- C-like syntax
- variable bindings
- integers and booleans
- arithmetic expressions
- built-in functions
- first-class and higher-order functions
- closures
- a string data structure
- an array data structure
- a hash data structure

### Monkey Syntax

#### Binding Values to Names

```
let age = 1;
let name = "Monkey";
let result = 10 * (20 / 2);
```

#### Array and Hash Data Structures

```
let myArray = [1, 2, 3, 4, 5]; // array declaration
let thorsten = {"name": "Thorsten", "age": 28};  // key-value pairs

// Accessing the elements in arrays and hashes is done with index expressions
myArray[0]       // => 1
thorsten["name"] // => "Thorsten"
```

#### Binding Functions to Names

```
// func to add two numbers
let add = fn(a, b) { return a + b; };

// monkey also supports implicit return statements as well
let add = fn(a, b) { a + b; };

// calling a function
add(1, 2);
```

#### Recursion

```
// recursive function
let fibonacci = fn(x) {
  if (x == 0) {
    0
  } else {
    if (x == 1) {
      1
    } else {
      fibonacci(x - 1) + fibonacci(x - 2);
    }
  }
};
```

#### Higher-Order Functions

```
let twice = fn(f, x) {
  return f(f(x));
}

let addTwo = fn(x) {
  return x + 2;
}

twice(addTwo, 2); // => 6
```

### Architecture
- `Lexer`
- `Parser`
- `Abstract Syntax Tree (AST)`
- `Internal object system`
- `Evaluator`

