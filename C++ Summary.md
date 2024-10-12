# C++ Programming Summary/Overview

## Object-Oriented Programming

> ### This section was written in conjunction with ChatGPT.

Object-Oriented Programming (**OOP**) is a programming paradigm that organizes code around objects, which are instances of classes. It focuses on the concept of objects, their properties (attributes), and behaviors (methods), allowing for modular, reusable, and structured code design.

## Encapsulation
Encapsulation is the practice of bundling data and the methods that operate on that data within a single unit, which is typically a class. It promotes data hiding and information hiding, ensuring that the internal state and implementation details of an object are not directly accessible from outside the object. Encapsulation helps achieve data integrity, security, and abstraction by controlling access through well-defined interfaces.

## Data Hiding
Data hiding is a principle closely related to encapsulation. It involves concealing the internal implementation details of an object and exposing only the necessary information through well-defined interfaces. By hiding implementation details, the object's data is protected and can only be accessed or modified through controlled methods. This enhances data security, code maintainability, and reduces the risk of unintended modifications or access to critical data.

## Inheritance

Inheritance is a mechanism in OOP that allows new classes (derived classes or subclasses) to inherit properties and behaviors from existing classes (base classes or superclasses). Inheritance promotes code reuse, as derived classes can inherit and extend the functionality of their base classes. The derived classes can add new attributes and behaviors or override existing ones to customize the behavior of inherited members. Inheritance facilitates code organization, modularity, and the creation of hierarchical relationships between classes.

## Polymorphism

Polymorphism is a fundamental concept in object-oriented programming (OOP) that allows objects of different classes to be treated as objects of a common base class. It enables you to write code that can work with objects of multiple types in a uniform manner.

Polymorphism is often illustrated through inheritance, where you have a base class and multiple derived classes that inherit from it. The derived classes can override or extend the behavior of the base class's methods, while still adhering to the common interface.

> ### This section was written in conjunction with Leo, Brave`s build-in AI.

Object-Oriented Programming (**OOP**) is a programming paradigm that revolves around the concept of “objects” and their interactions. In C++, OOP is achieved through the use of classes, objects, inheritance, polymorphism, and encapsulation.

### Key Concepts:

1. **Classes**: A class is a blueprint or a template that defines the properties and behavior of an object. It’s a user-defined data type that encapsulates data and functions that operate on that data.
2. **Objects**: An object is an instance of a class, with its own set of attributes (data) and methods (functions). Objects have their own memory space and can be manipulated independently.
3. **Inheritance**: Inheritance allows a derived class to inherit the properties and behavior of a base class. This enables code reuse and facilitates a hierarchical organization of classes.
4. **Polymorphism**: Polymorphism is the ability of an object to take on multiple forms. In C++, this is achieved through function overloading (multiple functions with the same name but different parameters) and function overriding (a derived class provides a different implementation of a function already defined in its base class).
5. **Encapsulation**: Encapsulation is the concept of hiding an object’s internal state and behavior from the outside world, while exposing only a controlled interface through which other objects can interact with it.

### C++ OOP Features:

1. **Constructors**: Special member functions that initialize objects when they’re created.
2. **Destructors**: Special member functions that clean up resources when objects are destroyed.
3. **Access Specifiers**: public, private, and protected keywords control access to class members.
4. **Virtual Functions**: Allow for dynamic method dispatching and polymorphism.
5. **Operator Overloading**: Enables the use of operators (e.g., +, -, ==) with user-defined classes.

## C++ OOP Examples:

**Simple Class**: Define a `Car` class with attributes brand, model, and mileage, and methods `startEngine()` and `accelerate()`.
```c++
class Car {
public:
    string brand;
    string model;
    int mileage;

    void startEngine() { cout << "Vroom!" << endl; }
    void accelerate() { mileage++; }
};
```
**Inheritance**: Create a `ElectricCar` class that inherits from Car and adds a `batteryLevel` attribute and a `charge()` method.
```c++
class ElectricCar : public Car {
public:
    int batteryLevel;

    void charge() { batteryLevel += 10; }
};
```
**Polymorphism**: Define a Vehicle class with a virtual `drive()` method, and have Car and `ElectricCar` classes override this method.
```c++
class Vehicle {
public:
    virtual void drive() { cout << "Driving..." << endl; }
};

class Car : public Vehicle {
public:
    void drive() { cout << "Driving with gasoline..." << endl; }
};

class ElectricCar : public Vehicle {
public:
    void drive() { cout << "Driving with electricity..." << endl; }
};
```
### Best Practices:

1. Follow the Single Responsibility Principle (SRP): Each class should have a single, well-defined responsibility.
2. Use encapsulation to hide internal implementation details.
3. Favor composition over inheritance: Instead of inheriting from a base class, consider composing objects from smaller, independent components.
4. Use polymorphism to write flexible and reusable code.

Resources:

“Object-Oriented Programming in C++” by Robert Lafore (book)
GeeksforGeeks - Object-Oriented Programming in C++
C++ documentation - Classes and Objects
Remember to practice and experiment with different OOP concepts in C++ to solidify your understanding.

## Syntax and Structure

> ### This section was written in conjunction with ChatGPT.

Syntax refers to the set of rules that define the structure, format and grammar of a programming language. It dictates how statements and expressions should be written to form valid code.

C++ follows a structured syntax that includes elements such as keywords1, identifiers, operators and control structures. The syntax is designed to provide precise instructions to the compiler on how to interpret and execute the code.

### Weak vs Strong typing
Weak and strong typing refer to different approaches in how programming languages handle data types and type safety.

In C++, the language is considered strongly typed, as it requires explicit type conversions and does not perform implicit type coercion without the programmer's explicit instruction (except number data types). C++ enforces strong typing to ensure type safety and minimize potential errors.

Weak Typing (Python2 code):
```c++
a = 5 # Compiled! Because Python is a weak typing language.
```
Strong Typing (C++ code):
```c++
a = 5; // Error!
int a = 5; // Compiled!
```
### Semicolons in C++
In C++, a semicolon (;) is used to mark the end of a statement. It serves as a delimiter, indicating to the compiler that one statement has finished and another begins. The presence of semicolons allows the compiler to separate statements and interpret code correctly.

The requirement for semicolons in C++ is a design choice that provides explicit statement termination. This approach allows for more fine-grained control over program execution and eliminates ambiguity.

In contrast, languages like Python2 use indentation to define blocks of code, eliminating the need for explicit statement termination with semicolons.
```c++
int a = 5; // Compiled!
int b = 5 // Error! Semicolon missing.
```

### Curly Braces in C++
C++ uses curly braces ({}) as block delimiters to enclose multiple statements or define the body of control structures, functions, and classes. The use of curly braces provides a clear and explicit way to define the boundaries of code blocks (also know as a scope).

Curly braces help define the scope of variables and maintain code readability. They ensure that statements within the braces are treated as a single unit, making it easier to understand the flow and logic of the program.
```c++
class Car
{

};
namespace MyNamespace
{

}
void MyFunction()
{
    {
        // Scope inside a function
    }
}
```
### Comments in C++
Both single-line and multi-line comments are helpful for adding explanatory notes, documenting code, or temporarily disabling sections of code during debugging or development. They enhance code readability, facilitate collaboration, and provide valuable information to developers maintaining the codebase.

#### Single-line comments
Single-line comments start with two forward slashes // and continue until the end of the line.

They are typically used for brief comments or explanations on a single line.
```
// This is a single-line comment in C++
```

#### Multi-line comments
Multi-line comments, also known as block comments, start with a forward slash (/) followed by an asterisk (*) and end with an asterisk (*) followed by a forward slash (/).

Multi-line comments can span multiple lines and are used for more extensive comments or documentation.
```
/*
    This is a multi-line comment
    It can span multiple lines
*/
```

### Headers vs source files
In C++, header files and source files are two types of files used to organize and manage code in a C++ program.

#### Header Files (.h)
- Header files contain declarations of classes, functions, variables, and other elements that are used in the program.
- They provide interfaces to the functionality implemented in the corresponding source files.
- Header files are included in source files using #include directives to make the declarations visible to the compiler during the compilation process.

#### Source Files (.cpp)
- Source files contain the actual implementations of the functions and classes declared in the header files.
- They define how the functions and classes behave and provide the logic for the program's functionality.
- Source files are compiled to object files and then linked together to create the final executable.

#### Reason for Separate Header and Source Files
The separation of header and source files is a design choice that promotes modularity and improves build efficiency in C++. By keeping declarations in header files and implementations in source files, the compiler can easily check for correctness and compile only the necessary code, reducing build times and preventing redundant compilation.

#### History of Single File Extensions

In the early days of computing, languages like Fortran and COBOL used single file extensions because of the limitations of the operating systems and compilers at the time. Each file had to adhere to a specific format defined by the language and its compiler, and the extension represented that format.

Other languages, like C#3, Java4, and Python2, continued to use single file extensions because they adopted a more integrated approach to handling both declarations and implementations within a single file.

In modern programming, the choice of using single file extensions or separate header and source files depends on the language's design philosophy and the needs of the development community. Both approaches have their strengths and weaknesses, and different languages adopt the one that best aligns with their goals and use cases.

#### Includes
In C++, the include directive is used to bring external code (headers or libraries) into your source code. It allows you to access the declarations and definitions present in those files.

The include directive is typically written as:

#include "filename.h"   // Using double quotes for user-defined headers
#include <filename.h>   // Using angular brackets for standard library headers
Here's the difference between using double quotes and angular brackets:

1. **Double Quotes (`filename.h`**): When you use double quotes, the preprocessor searches for the header file in the current directory first. If it doesn't find the file there, it will look in the additional include directories specified in the project settings.

Example: `#include "MyHeader.h"`

2. **Angular Brackets (`<filename.h>`)**: When you use angular brackets, the preprocessor only searches for the header file in the standard library directories specified for the compiler.

Example: `#include <iostream>`

In general, you use double quotes for your own header files (which may be part of your project) and angular brackets for standard library headers (like iostream, vector, etc.) or headers from external libraries.

> ### This section was written in conjunction with Leo, Brave`s build-in AI.
C++ syntax refers to the rules that govern the structure of C++ programs, including:

1. **Indentation**: C++ uses indentation to denote block-level structure, such as if-else statements, loops, and functions.
2. **Keywords**: C++ has a set of reserved keywords, such as if, else, for, while, switch, case, etc., which have specific meanings.
3. **Identifiers**: C++ uses identifiers (names) for variables, functions, and labels, which must start with a letter or underscore and can be followed by letters, digits, and underscores.
4. **Operators**: C++ has various operators for arithmetic, comparison, logical, assignment, and other operations.
5. **Brackets**: C++ uses parentheses () for function calls, and square brackets [] for array indexing.
6. **Semicolons**: C++ uses semicolons ; to terminate statements.

## Structure in C++

C++ structure refers to the organization of code into logical units, including:

1. **Functions**: C++ functions are self-contained blocks of code that perform specific tasks, returning values or modifying external state.
2. **Classes**: C++ classes define user-defined data types, combining data members (variables) and member functions (methods).
3. **Structures**: C++ structures (typedef’d as struct) are similar to classes, but without inheritance and with default public access.
4. **Enums**: C++ enumerations (typedef’d as enum) define a set of named constants.
5. **Unions**: C++ unions define a type that can hold values of different data types, occupying the same memory space.
6. **Arrays**: C++ arrays store multiple values of the same data type, indexed by integers.
7. **Pointers**: C++ pointers store memory addresses, allowing indirect access to variables.

## Best Practices

1. **Consistent indentation**: Use a consistent number of spaces for indentation throughout the code.
2. **Proper naming**: Use meaningful and descriptive names for variables, functions, and classes.
3. **Code organization**: Structure code into logical modules, functions, and classes.
4. **Commenting**: Use comments to explain code intent, assumptions, and limitations.
5. **Error handling**: Implement robust error handling mechanisms to detect and recover from errors.

## Example Code

Here’s a simple C++ program demonstrating syntax and structure:
```c++
#include <iostream>

// Structure to represent a person
struct Person {
    std::string name;
    int age;
};

// Function to print person information
void printPerson(const Person& p) {
    std::cout << "Name: " << p.name << ", Age: " << p.age << std::endl;
}

int main() {
    // Create a Person structure instance
    Person john = {"John", 30};

    // Call the printPerson function
    printPerson(john);

    return 0;
}
```
This code demonstrates:

- Structure declaration (struct Person)
- Function definition (void printPerson)
- Variable declaration and initialization (Person john)
- Function call (printPerson(john))

Note that this is a simplified example, and real-world C++ programs typically involve more complex structures, functions, and error handling mechanisms.

## Standard Library
This section was written in conjunction with ChatGPT.
The standard library in C++ is a collection of pre-defined classes and functions that provide a wide range of functionality for common tasks. It is a part of the C++ Standard Template Library (STL) and is officially known as the C++ Standard Library. The library is designed to be platform-independent and provides a standardized set of features that are supported across different C++ compilers and environments.

The C++ Standard Library is organized into several header files, each of which contains declarations for specific classes and functions. Some of the key components of the standard library include containers (like vectors, lists, maps, etc.), algorithms (sorting, searching, etc.), iterators, input/output operations, strings, and more.

To use the standard library in C++, you include the appropriate header files in your code, and then you can directly use the classes and functions provided by the library. For example, to use the std::vector class, you include the <vector> header file and then create instances of the vector and use its methods.

The name "std" comes from the fact that all the classes, functions, and other elements of the standard library are part of the std namespace. The namespace std is used to avoid naming conflicts with other libraries and user-defined code. By using the std:: prefix before any element from the standard library, you explicitly specify that you are referring to the elements in the std namespace.

Here's a simple example of how to use the standard library in C++:
```c+++
#include <iostream>
#include <vector>
#include <algorithm>

std::vector<int> numbers = {5, 2, 9, 1, 7};

// Use standard library algorithm to sort the vector
std::sort(numbers.begin(), numbers.end());

// Use standard library to print the sorted vector
for (int num : numbers)
{
    std::cout << num << " ";
}
```

> ### This section was written in conjunction with Leo, Brave`s build-in AI.

The **C++ Standard Library**, also known as the STL (Standard Template Library), is **a comprehensive collection of reusable components and algorithms for performing common tasks in C++ programming**. It provides a wide range of features, including:

1. **Containers**: Such as vectors, lists, sets, maps, and arrays, for storing and manipulating data.
2. **Algorithms**: For performing operations on containers, such as sorting, searching, and manipulating elements.
3. **Iterators**: For traversing and accessing elements in containers.
4. **Streams**: For input/output operations, including file I/O, console I/O, and string manipulation.
5. **Strings**: For working with strings, including concatenation, searching, and manipulation.
6. **Numerics**: For mathematical operations, such as arithmetic, trigonometry, and statistical functions.
7. **Utility**: For miscellaneous tasks, such as memory management, exception handling, and type traits.

### Implementations

The C++ Standard Library has several implementations, including:

1. **GNU C++ Standard Library** (libstdc++): Part of the GNU Compiler Collection (GCC), licensed under the GPL v3 with the GCC Runtime Library Exception.
2. **LLVM C++ Standard Library** (libc++): Part of the LLVM Compiler Infrastructure, licensed under the Apache License 2.0 with LLVM Exceptions.
3. **Microsoft C++ Standard Library** (MSVC STL): Part of the Microsoft Visual C++ compiler, licensed under the Apache License 2.0 with LLVM Exceptions.
4. **NVIDIA C++ Standard Library** (libcudacxx): Part of the NVIDIA CUDA Toolkit, licensed under the Apache License 2.0 with LLVM Exceptions.
5. **HPX C++ Standard Library for Parallelism and Concurrency** (HPX): Developed by the STELLAR Group, licensed under the Boost Software License 1.0.
6. **Electronic Arts Standard Template Library** (EASTL): Developed by Electronic Arts, licensed under the BSD 3-Clause License.

### Key Features and Evolution

The C++ Standard Library has undergone significant changes and improvements over the years. Some notable features and milestones include:

1. **C++98**: Introduced the STL, with a focus on generic programming and containers.
2. **C++11**: Added features like move semantics, rvalue references, and lambda expressions.
3. **C++14**: Introduced generic lambdas, return type deduction, and variable templates.
4. **C++17**: Added features like structured bindings, if-constexpr, and fold expressions.
5. **C++20**: Introduced concepts, modules, and coroutines.
6. **C++23**: Improved interoperability with C, deprecated some legacy headers, and added named modules.

### Conclusion

The C++ Standard Library is a fundamental part of the C++ programming language, providing a wide range of reusable components and algorithms for common tasks. Its implementations vary, but the core features and evolution have been shaped by the C++ standards committee and the contributions of the developer community.