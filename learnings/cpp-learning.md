---
layout: page
title: C++ Notes
permalink: /learnings/cpp-learning.html
---

### Introduction

- C++ is a platform independent language and it does not “belong” to a single vendor
- It uses functions and classes for just about everything
- It is an object-oriented language (OO is a programming paradigm that organises software around `objects`, which can contain data (known as attributes or properties) and code (known as methods or functions) that manipulate that data

### How source code becomes executable?

Compiler takes `source code` as input and creates `object` files. Then, the linker takes the object files as input and link them to create the `executable file`  which runs on machine.

### What is stream?

A stream is a continous flow of data, like a `sequence of bytes or characters`, that can be read from (input) or written to (output) one by one. It allows data to be processed as it moves, rather than all at once.

```cpp
/*
 * << sends something to stream
 * >> reads something from stream
 *
 * cout is console output
 * cin is console input
 */

// use 'include' keyword to include the library
#include <iostream>

int main() {
    std::cout << "Hello World!" << '\n';
}
```

### Function Overloading

Function overloading means when two functions have the same `name` but different `function signature` (number and types of parameters are different).

```cpp
double add(double x, double y) {
    return x + y;
}

double add(double x, double y, double z) {
    return x + y + z;
}

bool test(bool x) {
    return x;
}

bool test(double x) {
    return x;
}
```


