# CPP Module 02

This repository contains exercises focused on fixed-point number implementation in C++.

## Overview

This module introduces the concept of Ad-hoc polymorphism (function overloading), operators overloading, and orthodox canonical form in C++. The exercises revolve around implementing a fixed-point number class that simulates the behavior of floating-point numbers using integer arithmetic.

## Exercises

### Exercise 00: My First Class in Orthodox Canonical Form

A basic introduction to the Orthodox Canonical Form in C++ class implementation.

#### Features:
- Implementation of a simple fixed-point number class
- Proper constructors and destructors
- Copy constructor and assignment operator overload
- Getter and setter for raw bits

#### Implementation Details:
- Private attribute to store the fixed-point number value
- Static constant integer to store the number of fractional bits (8)
- Member functions to get and set the raw value

### Exercise 01: Towards a more useful fixed-point number class

Extends the Fixed class to handle floating-point and integer conversions.

#### Features:
- Constructors for different types (int, float)
- Conversion functions to convert fixed-point value to float and int
- Stream insertion operator (`<<`) overload for display

#### Implementation Details:
- Constructor that takes an integer value
- Constructor that takes a floating-point value
- Member functions to convert between fixed-point and other formats
- Stream insertion operator to display the fixed-point value as a float

### Exercise 02: Now we're talking

Extends the Fixed class further with comparison operators, arithmetic operators, and increment/decrement operators.

#### Features:
- Comparison operators (`>`, `<`, `>=`, `<=`, `==`, `!=`)
- Arithmetic operators (`+`, `-`, `*`, `/`)
- Pre-increment, post-increment, pre-decrement, post-decrement operators
- Static member functions for finding minimum and maximum values

#### Implementation Details:
- Overloaded comparison operators
- Overloaded arithmetic operators
- Increment and decrement operators (both prefix and postfix)
- Static min and max functions with both const and non-const versions

## Compilation

Each exercise comes with a Makefile that supports the following commands:
- `make`: Compile the program
- `make clean`: Remove object files
- `make fclean`: Remove object files and executable
- `make re`: Recompile the entire program

## Requirements

- C++ compiler with C++98 standard support
- Linux/macOS environment
- All code must compile with the following flags:
```
c++ -Wall -Wextra -Werror -std=c++98
```

## Technical Details

### Fixed-point Number Representation

Fixed-point numbers are an alternative to floating-point numbers. In our implementation:
- We use an integer to store the value
- We dedicate 8 bits for the fractional part
- The value is stored as the actual value multiplied by 2^8 (or 256)
- Conversion between fixed-point and floating-point requires scaling

### Orthodox Canonical Form

Classes in Orthodox Canonical Form include:
1. A default constructor
2. A copy constructor
3. A destructor
4. An assignment operator

This ensures proper object lifecycle management, especially when dealing with dynamic memory (though our Fixed class doesn't use dynamic allocation).

## Notes

These exercises demonstrate essential C++ concepts such as:
- Class design and implementation
- Operator overloading
- Type conversion
- The importance of canonical form in C++ classes
- Working with fixed-point arithmetic