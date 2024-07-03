# C---Basic

# Cpp-Language-Examples

## Description

This repository provides a comprehensive collection of examples and explanations for the C++ programming language. It covers the basics, advanced topics, and best practices to help you master C++.

## Directory Structure
Cpp-Language-Examples/
├── LICENSE
├── README.md
├── basics/
│ ├── variables/
│ │ ├── example1.cpp
│ │ ├── example2.cpp
│ ├── control_structures/
│ │ ├── if_else.cpp
│ │ ├── switch_case.cpp
│ ├── functions/
│ ├── function_declaration.cpp
│ ├── function_overloading.cpp
├── advanced_topics/
│ ├── templates/
│ │ ├── template_functions.cpp
│ │ ├── template_classes.cpp
│ ├── smart_pointers/
│ ├── unique_ptr.cpp
│ ├── shared_ptr.cpp
├── best_practices/
│ ├── code_organization/
│ │ ├── header_files.cpp
│ │ ├── source_files.cpp
│ ├── error_handling/
│ ├── try_catch.cpp
│ ├── assertions.cpp
├── additional_topics/
│ ├── multithreading/
│ │ ├── multithreading.cpp
│ ├── regular_expressions/
│ ├── regular_expressions.cpp
│ ├── file_input_output/
│ ├── file_input_output.cpp
│ ├── exception_handling/
│ ├── exception_handling.cpp
│ ├── operator_overloading/
│ ├── operator_overloading.cpp
│ ├── inheritance/
│ ├── inheritance.cpp
│ ├── lambda_functions/
│ ├── lambda_functions.cpp
│ ├── move_semantics/
│ ├── move_semantics.cpp
├── tools_and_resources/
│ ├── code_review.md
│ ├── testing.cpp
├── CMakeLists.txt


## Files and Folders

- **LICENSE**: This file contains the licensing information for this repository. You can use the examples and explanations for personal or commercial purposes.
- **README.md**: This is the file you're reading right now! It provides an overview of the repository, its structure, and the topics covered.

### Basics

- **variables/**: Examples of declaring and using variables, including data types, operators, and expressions.
- **control_structures/**: Examples of control structures, such as if-else statements, switch cases, loops, and conditional statements.
- **functions/**: Examples of function declarations, function overloading, and function templates.

### Advanced Topics

- **templates/**: Examples of using templates for generic programming, including function templates and class templates.
- **smart_pointers/**: Examples of using smart pointers, such as `unique_ptr` and `shared_ptr`, for memory management.

### Best Practices

- **code_organization/**: Examples of organizing code using header files, source files, and namespaces.
- **error_handling/**: Examples of handling errors using try-catch blocks, assertions, and error codes.

### Additional Topics

- **multithreading/**: Examples of multithreading in C++.
- **regular_expressions/**: Examples of using regular expressions.
- **file_input_output/**: Examples of file input and output.
- **exception_handling/**: Examples of exception handling.
- **operator_overloading/**: Examples of operator overloading.
- **inheritance/**: Examples of inheritance in C++.
- **lambda_functions/**: Examples of lambda functions.
- **move_semantics/**: Examples of move semantics.

### Tools and Resources

- **code_review.md**: Code review checklist.
- **testing.cpp**: Examples of testing using Google Test.

## Examples

### Variables
```cpp
// example1.cpp
#include <iostream>

int main() {
    int x = 5;  // declare and initialize an integer variable
    std::cout << "x = " << x << std::endl;
    return 0;
}

Control Structures
cpp
Copiar código
// if_else.cpp
#include <iostream>

int main() {
    int x = 5;
    if (x > 10) {
        std::cout << "x is greater than 10" << std::endl;
    } else {
        std::cout << "x is less than or equal to 10" << std::endl;
    }
    return 0;
}
Functions
cpp
Copiar código
// function_declaration.cpp
#include <iostream>
#include <string>

void greet(std::string name) {
    std::cout << "Hello, " << name << "!" << std::endl;
}

int main() {
    greet("John");
    return 0;
}
Templates
cpp
Copiar código
// template_functions.cpp
#include <iostream>

template <typename T>
T max(T a, T b) {
    return (a > b) ? a : b;
}

int main() {
    int x = 5;
    int y = 10;
    std::cout << "Max: " << max(x, y) << std::endl;
    return 0;
}
Advanced Topics
Templates
cpp
Copiar código
// template_classes.cpp
#include <iostream>
#include <string>

template <typename T>
class Container {
public:
    T value;
    Container(T val) : value(val) {}
    T getValue() { return value; }
};

int main() {
    Container<int> intContainer(5);
    std::cout << "Int value: " << intContainer.getValue() << std::endl;

    Container<std::string> stringContainer("Hello");
    std::cout << "String value: " << stringContainer.getValue() << std::endl;
    return 0;
}
Smart Pointers
cpp
Copiar código
// unique_ptr.cpp
#include <iostream>
#include <memory>

class MyClass {
public:
    MyClass() { std::cout << "MyClass constructor" << std::endl; }
    ~MyClass() { std::cout << "MyClass destructor" << std::endl; }
};

int main() {
    std::unique_ptr<MyClass> ptr(new MyClass);
    // ptr is the only owner of the MyClass object
    return 0;
}
Lambda Functions
cpp
Copiar código
// lambda_functions.cpp
#include <iostream>

int main() {
    auto lambda = [](int x, int y) { return x + y; };
    std::cout << "Result: " << lambda(5, 3) << std::endl;
    return 0;
}
Move Semantics
cpp
Copiar código
// move_semantics.cpp
#include <iostream>

class MyClass {
public:
    MyClass() { std::cout << "MyClass constructor" << std::endl; }
    MyClass(MyClass&& other) { std::cout << "MyClass move constructor" << std::endl; }
    ~MyClass() { std::cout << "MyClass destructor" << std::endl; }
};

int main() {
    MyClass obj1;
    MyClass obj2 = std::move(obj1);
    return 0;
}
Best Practices
Code Organization
cpp
Copiar código
// header_file.h
#ifndef HEADER_FILE_H
#define HEADER_FILE_H

void myFunction();

#endif  // HEADER_FILE_H
cpp
Copiar código
// source_file.cpp
#include <iostream>
#include "header_file.h"

void myFunction() {
    std::cout << "Hello, World!" << std::endl;
}
Error Handling
cpp
Copiar código
// error_handling.cpp
#include <iostream>
#include <stdexcept>

void myFunction() {
    try {
        // code that might throw an exception
        throw std::runtime_error("Error occurred");
    } catch (const std::exception& e) {
        std::cerr << "Error: " << e.what() << std::endl;
    }
}
Additional Topics
Multithreading
cpp
Copiar código
// multithreading.cpp
#include <iostream>
#include <thread>

void myFunction() {
    std::cout << "Hello from thread!" << std::endl;
}

int main() {
    std::thread t1(myFunction);
    t1.join();
    return 0;
}
Regular Expressions
cpp
Copiar código
// regular_expressions.cpp
#include <iostream>
#include <regex>
#include <string>

int main() {
    std::string input = "Hello, World!";
    std::regex pattern("Hello");
    if (std::regex_search(input, pattern)) {
        std::cout << "Match found!" << std::endl;
    }
    return 0;
}
File Input/Output
cpp
Copiar código
// file_input_output.cpp
#include <fstream>
#include <iostream>
#include <string>

int main() {
    std::ofstream file("example.txt");
    file << "Hello, World!" << std::endl;
    file.close();

    std::ifstream readFile("example.txt");
    std::string line;
    while (std::getline(readFile, line)) {
        std::cout << line << std::endl;
    }
    readFile.close();
    return 0;
}
Exception Handling
cpp
Copiar código
// exception_handling.cpp
#include <iostream>
#include <stdexcept>

void myFunction() {
    try {
        // code that might throw an exception
        throw std::runtime_error("Error occurred");
    } catch (const std::exception& e) {
        std::cerr << "Error: " << e.what() << std::endl;
    }
}
Operator Overloading
cpp
Copiar código
// operator_overloading.cpp
#include <iostream>

class MyClass {
public:
    int value;
    MyClass(int val) : value(val) {}

    MyClass operator+(const MyClass& other) {
        return MyClass(value + other.value);
    }
};

int main() {
    MyClass obj1(5);
    MyClass obj2(3);
    MyClass result = obj1 + obj2;
    std::cout << "Result: " << result.value << std::endl;
    return 0;
}
Inheritance
cpp
Copiar código
// inheritance.cpp
#include <iostream>

class Animal {
public:
    virtual void sound() = 0;
};

class Dog : public Animal {
public:
    void sound() override {
        std::cout << "Woof!" << std::endl;
    }
};

int main() {
    Dog myDog;
    myDog.sound();
    return 0;
}
Tools and Resources
Code Review
markdown
Copiar código
// code_review.md
### Code Review Checklist

* [ ] Does the code follow the coding standards?
* [ ] Are there any syntax errors or warnings?
* [ ] Are the variable names descriptive and consistent?
* [ ] Are the functions well-documented and easy to understand?
* [ ] Are there any performance or security issues?
Testing
cpp
Copiar código
// testing.cpp
#include <gtest/gtest.h>

TEST(MyTest, ExampleTest) {
    EXPECT_TRUE(true);
}

int main(int argc, char **argv) {
    ::testing::InitGoogleTest(&argc, argv);
    return RUN_ALL_TESTS();
}
Compilers, IDEs, and Debuggers
Compilers
GCC (GNU Compiler Collection)
Clang
MSVC (Microsoft Visual C++)
IDEs
Visual Studio
IntelliJ IDEA
Eclipse
Debuggers
GDB (GNU Debugger)
LLDB (Low-Level Debugger)
Visual Studio Debugger
css
Copiar código

This revised version should help organize the content more clearly and make it easier to understand and navigate.
LLDB (Low-Level Debugger)
Visual Studio Debugger
