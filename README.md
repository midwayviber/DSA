# C++ Preparation Guide

## 1. Object-Oriented Programming (OOP)
Mastery is essential here. You should be comfortable with core OOP concepts as they are often tested in depth. Key topics include:

- **Inheritance**: Allows creating a new class from an existing class, inheriting its properties and behavior. Types include single, multiple, hierarchical, and hybrid inheritance.
- **Polymorphism**: Provides the ability to redefine methods in derived classes, allowing for both compile-time (function overloading, operator overloading) and runtime polymorphism (virtual functions).
- **Encapsulation**: Bundles data and methods operating on the data within one unit, typically a class, restricting direct access to some components.
- **Abstraction**: Hides complex implementation details and only exposes essential features to the user.

## 2. Templates
Templates are a key topic in C++. Understanding their basics is essential, though advanced usage may not always be required. Important concepts include:

- **Function Templates**: Enable writing generic functions that work with any data type, defined using `template <typename T>`.
- **Class Templates**: Allow creating classes that can operate with any data type. They are defined similarly to function templates and are particularly useful in data structures.
- **Advanced Topics (Optional)**: If time permits, explore advanced topics like specialization, variadic templates, and template metaprogramming for more complex scenarios.

## 3. Exception Handling
Exception handling is important for writing robust code. The basics are sufficient for most cases, covering concepts such as:

- **try, catch, throw**: Use `try` blocks to test code that may throw an exception, `catch` to handle exceptions, and `throw` to signal the occurrence of an exception.
- **Standard Exceptions**: Familiarize yourself with standard exceptions provided by C++ like `std::exception`, `std::runtime_error`, and `std::out_of_range`.
- **Custom Exceptions (Optional)**: Only explore custom exceptions if you have extra time, as they are less commonly required.

## 4. STL (Standard Template Library)
STL is a popular area for practical coding questions. It includes various containers, iterators, and algorithms. Key topics include:

- **Containers**: Understand how to use the main STL containers, such as:
  - **Vectors** (`std::vector`): Dynamic arrays that can change in size.
  - **Lists** (`std::list`): Doubly-linked lists allowing efficient insertion and deletion.
  - **Maps** (`std::map`, `std::unordered_map`): Associative containers that store key-value pairs.
  - **Sets** (`std::set`, `std::unordered_set`): Collections of unique elements.
- **Iterators**: Know how to navigate through containers using iterators, including `begin()`, `end()`, `rbegin()`, `rend()`.
- **Algorithms**: Practice common algorithms like `sort`, `find`, `binary_search`, and `reverse`.

## 5. Dynamic Memory Management & Smart Pointers
Understanding memory management is critical, especially with smart pointers in modern C++. Important areas include:

- **Raw Pointers**: Familiarize yourself with pointer basics, memory allocation (`new` and `delete`), and memory leaks.
- **Smart Pointers**: Use smart pointers to manage memory automatically and avoid leaks:
  - **std::shared_ptr**: Shared ownership of an object, allowing multiple pointers to point to the same resource.
  - **std::unique_ptr**: Unique ownership, ensuring that only one pointer points to the resource.
  - **std::weak_ptr**: A weak reference to an object managed by `std::shared_ptr`, used to prevent cyclic references.

## 6. Lambda Expressions
Lambda expressions provide a concise way to define anonymous functions, especially useful in combination with STL algorithms. Key points include:

- **Syntax**: Understand the basic syntax: `[capture](parameters) -> return_type { body; }`.
- **Capture List**: Allows capturing variables from the surrounding scope, with options like `[&]` for reference and `[=]` for value capture.
- **Usage in STL**: Lambdas are frequently used in algorithms such as `std::sort` and `std::for_each` for custom comparisons and actions.

## 7. Multi-threading & Concurrency
Moderate preparation should be enough unless you expect this topic to be heavily tested. Key concepts include:

- **Thread Creation**: Use the `<thread>` library to create and manage threads.
- **Synchronization**: Understand the use of synchronization mechanisms such as:
  - **Mutex** (`std::mutex`): Prevents data races by allowing only one thread to access a resource at a time.
  - **Lock** (`std::lock_guard`): A RAII-style mechanism for managing mutexes.
  - **Condition Variables** (`std::condition_variable`): Enables threads to communicate based on certain conditions.
  
## 8. File Handling
File handling is usually a smaller part of tests, so a moderate understanding should suffice. Key topics include:

- **Reading and Writing Files**: Understand how to open, read, and write to files using `std::ifstream` and `std::ofstream`.
- **Binary vs Text Files**: Know the difference between text and binary files and when to use each.
- **File Streams**: Familiarize yourself with file stream operations, including `seekg` and `seekp` for positioning within a file.

``
