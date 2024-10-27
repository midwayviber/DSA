# 1. MCQs on Objects and Classes :

###  Easy

1. **Which of the following best defines a class in object-oriented programming?**
   - A. A blueprint for creating objects
   - B. A specific instance of an object
   - C. A memory location for storing data
   - D. A function that returns data

   **Answer:** A

2. **What is an object in object-oriented programming?**
   - A. A blueprint used to create functions
   - B. An instance of a class
   - C. A data type that stores multiple values
   - D. An identifier for a function

   **Answer:** B

3. **What does the keyword `this` refer to within a class?**
   - A. The base class of the object
   - B. The parent of the object
   - C. The current instance of the class
   - D. The return type of the object

   **Answer:** C

---

### Medium

4. **Which access modifier allows a class member to be accessible only within its own class?**
   - A. `private`
   - B. `protected`
   - C. `public`
   - D. `static`

   **Answer:** A

5. **In C++, what does the following statement do? `MyClass obj = MyClass();`**
   - A. Creates a class called `obj`
   - B. Declares a pointer to an object of type `MyClass`
   - C. Creates an object `obj` of type `MyClass` and calls the default constructor
   - D. Creates a derived class named `obj`

   **Answer:** C

6. **Which of the following correctly describes an abstract class?**
   - A. A class that must be inherited and cannot be instantiated
   - B. A class that can be instantiated without any restrictions
   - C. A class with private data members only
   - D. A class that cannot have any member functions

   **Answer:** A

---

### Hard

7. **What is the primary purpose of a destructor in a class?**
   - A. To initialize class members when an object is created
   - B. To delete an object after its lifetime ends
   - C. To allocate memory for a new object
   - D. To provide a default value for class members

   **Answer:** B

8. **Which of the following best describes polymorphism in object-oriented programming?**
   - A. The ability of derived classes to access private members of base classes
   - B. A technique to hide data within a class
   - C. The ability of different objects to respond uniquely to the same function call
   - D. A function that can operate on different data types

   **Answer:** C

9. **Which of the following C++ concepts is used to resolve ambiguity in multiple inheritance?**
   - A. Method Overloading
   - B. Virtual Inheritance
   - C. Operator Overloading
   - D. Friend Function

   **Answer:** B

10. **In C++, when is a copy constructor called?**
    - A. When a new object is assigned to another object of the same class
    - B. When a function returns an object by value
    - C. When an object is passed by value as a parameter
    - D. All of the above

    **Answer:** D
---

# 2. MCQs on Constructors (Parameterized and Non-Parameterized) :

---

## Easy

1. **What is a constructor in C++?**
   - A. A special function that initializes an object
   - B. A regular function that returns the object’s data
   - C. A function that is used only for inheritance
   - D. A function that is used to delete an object

   **Answer:** A

2. **When is a constructor called in a class?**
   - A. When a function is invoked
   - B. When an object is created
   - C. When an object is deleted
   - D. When an object is assigned a new value

   **Answer:** B

3. **Which of the following correctly defines a default (non-parameterized) constructor?**
   - A. `MyClass(int x);`
   - B. `MyClass();`
   - C. `int MyClass();`
   - D. `MyClass(int x, int y);`

   **Answer:** B

4. **What is the purpose of a default (non-parameterized) constructor?**
   - A. To initialize all members to random values
   - B. To initialize object members with default values
   - C. To delete object members
   - D. To pass parameters to an object

   **Answer:** B

5. **Which of the following statements about constructors is true?**
   - A. A constructor has the same name as its class
   - B. Constructors must always return a value
   - C. Constructors cannot be overloaded
   - D. Constructors are called manually by the user

   **Answer:** A

6. **What does a parameterized constructor allow you to do?**
   - A. Create objects with default values
   - B. Initialize objects with specific values
   - C. Return values from an object
   - D. Delete an object’s data members

   **Answer:** B

---

## Medium

7. **Which of the following correctly defines a parameterized constructor?**
   - A. `MyClass() {}`
   - B. `MyClass(int x) { this->x = x; }`
   - C. `MyClass return;`
   - D. `MyClass();`

   **Answer:** B

8. **What is the difference between a parameterized and a non-parameterized constructor?**
   - A. Parameterized constructors take arguments; non-parameterized do not
   - B. Non-parameterized constructors are public; parameterized are private
   - C. Parameterized constructors delete data; non-parameterized create data
   - D. Non-parameterized constructors return values; parameterized do not

   **Answer:** A

9. **How many times can a constructor be called for a single object?**
   - A. Once
   - B. Twice
   - C. Depends on the class size
   - D. As many times as needed

   **Answer:** A

10. **In C++, what will happen if no constructor is provided by the programmer?**
    - A. The program will generate an error
    - B. The compiler provides a default constructor
    - C. No object of the class can be created
    - D. The class cannot contain member variables

    **Answer:** B

11. **Which constructor is called when an object is copied?**
    - A. Default constructor
    - B. Copy constructor
    - C. Parameterized constructor
    - D. Destructor

    **Answer:** B

12. **How can you initialize class members using a parameterized constructor?**
    - A. By assigning values directly inside the constructor
    - B. By returning values from the constructor
    - C. By invoking a function inside the constructor
    - D. By calling the destructor

    **Answer:** A

13. **Which keyword is used to prevent a constructor from modifying member variables?**
    - A. `static`
    - B. `const`
    - C. `void`
    - D. `protected`

    **Answer:** B

14. **What does the following code do?**
    ```cpp
    MyClass obj1 = MyClass(5);
    MyClass obj2(obj1);
    ```
    - A. Creates two objects with different values
    - B. Calls the copy constructor for `obj2`
    - C. Calls a destructor
    - D. Calls the default constructor for `obj2`

    **Answer:** B

---

## Hard

15. **Which of the following statements is true about constructors?**
    - A. A class can have only one constructor
    - B. Constructors can be virtual
    - C. Constructors cannot be inherited
    - D. A constructor can return any type

    **Answer:** C

16. **What is the purpose of an initializer list in a constructor?**
    - A. To initialize members directly with provided values
    - B. To call the destructor
    - C. To reset member values to zero
    - D. To change access modifiers for member variables

    **Answer:** A

17. **Which of the following describes an explicit constructor?**
    - A. A constructor that can be called automatically
    - B. A constructor that can’t be called with a single argument
    - C. A constructor that prevents implicit type conversions
    - D. A constructor that has default arguments

    **Answer:** C

18. **When does the destructor for an object get called?**
    - A. Immediately after the constructor is called
    - B. When the object goes out of scope
    - C. Only at the end of the program
    - D. It must be manually called by the programmer

    **Answer:** B

19. **Which syntax is correct for using an initializer list in C++?**
    ```cpp
    class MyClass {
        int x;
    public:
        MyClass(int a) : x(a) {}
    };
    ```
    - A. `: x(a)` is correct syntax for the initializer list
    - B. `x(a)` inside the constructor body
    - C. No initializer list needed
    - D. `: a(x)`

    **Answer:** A

20. **What happens if a parameterized constructor is defined, but no default constructor is provided?**
    - A. An error occurs if an object is created without arguments
    - B. The compiler creates a default constructor automatically
    - C. The object will contain random data
    - D. All constructors will be deleted

    **Answer:** A
---
# 3. MCQs on the `this` Keyword :

---

## Easy

1. **What does the `this` keyword represent in C++?**
   - A. The class itself
   - B. A pointer to the current object
   - C. A function to initialize the class
   - D. A constant integer

   **Answer:** B

2. **In which type of methods can the `this` pointer be used?**
   - A. Static methods only
   - B. Non-static methods only
   - C. Constructors only
   - D. Global functions only

   **Answer:** B

3. **What type of value is `this` in C++?**
   - A. Integer
   - B. Object
   - C. Pointer
   - D. Float

   **Answer:** C

4. **Which of the following is a valid use of the `this` pointer?**
   - A. To access static data members
   - B. To pass the current object as an argument
   - C. To create new objects
   - D. To assign a new value to the `this` pointer

   **Answer:** B

5. **What is the type of `this` pointer in a class named `MyClass`?**
   - A. `MyClass`
   - B. `MyClass*`
   - C. `int*`
   - D. `void*`

   **Answer:** B

---

## Medium

6. **Which statement best describes the `this` pointer in C++?**
   - A. A pointer to the base class of the object
   - B. A pointer to the current instance of the class
   - C. A reference to a static member of the class
   - D. A keyword to access private members of any class

   **Answer:** B

7. **How can the `this` pointer be used in a constructor?**
   - A. To prevent object creation
   - B. To differentiate between member variables and parameters
   - C. To delete an object
   - D. To call static functions within the class

   **Answer:** B

8. **What will `return *this;` do in a member function?**
   - A. Returns a copy of the object
   - B. Returns a pointer to the class
   - C. Returns the value of a specific variable
   - D. Returns the class name

   **Answer:** A

9. **Which of the following scenarios would require the use of `this`?**
   - A. Calling another function within the same class
   - B. Accessing a global variable with the same name as a class member variable
   - C. Accessing static members of the class
   - D. Returning the current class name

   **Answer:** B

10. **What does `this->x = x;` represent in a constructor?**
    - A. Assigns `this` to `x`
    - B. Assigns the parameter `x` to the member variable `x`
    - C. Calls a global variable `x`
    - D. Deletes the `x` variable in the class

    **Answer:** B
---

# 4. MCQs on Copy Constructors and Parameterized Copy Constructors

---

## Easy

1. **What is a copy constructor in C++?**
   - A. A constructor used to copy data members of one object to another
   - B. A constructor used to initialize static members
   - C. A constructor that takes no parameters
   - D. A constructor used to destroy an object

   **Answer:** A

2. **Which of the following is the correct syntax for a copy constructor?**
   - A. `ClassName(const ClassName obj);`
   - B. `ClassName(ClassName obj);`
   - C. `ClassName(const ClassName& obj);`
   - D. `ClassName(ClassName);`

   **Answer:** C

3. **When is a copy constructor called?**
   - A. When an object is deleted
   - B. When an object is copied
   - C. When an object is assigned a new value
   - D. When an object goes out of scope

   **Answer:** B

4. **What is the default behavior of the compiler if no copy constructor is defined?**
   - A. Generates an error
   - B. Automatically provides a default copy constructor
   - C. Skips object creation
   - D. Uses a parameterized constructor

   **Answer:** B

5. **A copy constructor typically accepts a parameter of which type?**
   - A. By value
   - B. By reference
   - C. By pointer
   - D. By array

   **Answer:** B

6. **Which of the following statements about copy constructors is correct?**
   - A. They must have the same name as the class
   - B. They must return a value
   - C. They cannot have parameters
   - D. They must be declared as `static`

   **Answer:** A

---

## Medium

7. **Which of the following is NOT a reason for a copy constructor to be called?**
   - A. Passing an object by value to a function
   - B. Returning an object by value from a function
   - C. Creating an object with an assignment operator
   - D. Assigning one object to another already-initialized object

   **Answer:** D

8. **What will happen if a copy constructor’s parameter is not passed by reference?**
   - A. The object will be copied recursively, causing a stack overflow
   - B. The object will be copied only once
   - C. An error will occur
   - D. The object will be passed by value, preventing recursion

   **Answer:** A

9. **Which of the following is true about the default copy constructor?**
   - A. It performs a shallow copy of the object
   - B. It performs a deep copy of the object
   - C. It throws an error if a copy is attempted
   - D. It only copies pointers, not values

   **Answer:** A

10. **What is the main difference between a copy constructor and a parameterized constructor?**
    - A. Copy constructors are always `const`
    - B. Copy constructors initialize an object with an existing object
    - C. Parameterized constructors require no arguments
    - D. Copy constructors can return values

    **Answer:** B

11. **Which of the following constructors is invoked when creating an object like this? `MyClass obj2 = obj1;`**
    - A. Default constructor
    - B. Parameterized constructor
    - C. Copy constructor
    - D. Destructor

    **Answer:** C

12. **What does a deep copy involve compared to a shallow copy?**
    - A. Copying only primitive data types
    - B. Copying all data members, including dynamically allocated memory
    - C. Copying only static members
    - D. Ignoring dynamically allocated memory

   **Answer:** B

13. **Which of the following correctly defines a parameterized copy constructor?**
    - A. `MyClass(MyClass obj, int val);`
    - B. `MyClass(const MyClass& obj, int val);`
    - C. `MyClass(MyClass& obj, int val);`
    - D. `MyClass(int val);`

   **Answer:** B

14. **How does a parameterized copy constructor differ from a standard copy constructor?**
    - A. It can accept additional parameters
    - B. It only copies primitive data types
    - C. It doesn’t initialize any member variables
    - D. It is called automatically

    **Answer:** A

15. **What will `return *this;` do in a copy constructor?**
    - A. Returns a reference to the copied object
    - B. Returns a new object
    - C. Returns an integer
    - D. Calls a destructor

    **Answer:** A

---

## Hard

16. **When creating a custom copy constructor, which type of copy (shallow or deep) is safer when dealing with dynamic memory allocation?**
    - A. Shallow copy
    - B. Deep copy
    - C. Either, depending on the compiler
    - D. Both are unsafe

    **Answer:** B

17. **If a class has pointer members, what should be ensured in its copy constructor?**
    - A. Shallow copy should be used
    - B. Only integer members are copied
    - C. Deep copy of pointer members should be performed
    - D. Avoid using a copy constructor

    **Answer:** C

18. **What is the result of using a shallow copy on a class with dynamically allocated memory?**
    - A. Both objects will point to the same memory
    - B. Each object will have its own copy of the memory
    - C. An error will occur during compilation
    - D. The object cannot be copied

    **Answer:** A

19. **What happens when a copy constructor and an assignment operator are both defined in a class?**
    - A. The copy constructor is called for object initialization
    - B. The assignment operator is called instead of the copy constructor
    - C. Both are called simultaneously
    - D. The assignment operator is ignored

    **Answer:** A

20. **What will happen if a class with a pointer data member does not define a copy constructor?**
    - A. A shallow copy is performed by default
    - B. A deep copy is performed by default
    - C. The program will fail to compile
    - D. The pointer will automatically be deleted

    **Answer:** A

---

# 5. MCQs on Destructors

---

## Easy

1. **What is a destructor in C++?**
   - A. A special function that is used to initialize an object
   - B. A special function that is used to destroy or clean up an object
   - C. A function to copy data from one object to another
   - D. A function that creates a deep copy of an object

   **Answer:** B

2. **Which symbol is used to define a destructor in C++?**
   - A. `#`
   - B. `@`
   - C. `~`
   - D. `$`

   **Answer:** C

3. **When is a destructor called?**
   - A. When an object is created
   - B. When an object goes out of scope or is explicitly deleted
   - C. When an object is assigned a new value
   - D. When the compiler initializes an object

   **Answer:** B

4. **What is the main purpose of a destructor?**
   - A. To initialize an object with default values
   - B. To free resources held by an object
   - C. To copy values from another object
   - D. To assign values to an object

   **Answer:** B

5. **Which of the following is the correct syntax for defining a destructor in a class named `MyClass`?**
   - A. `MyClass() {}`
   - B. `void ~MyClass() {}`
   - C. `~MyClass() {}`
   - D. `delete MyClass() {}`

   **Answer:** C

---

## Medium

6. **Can a destructor take arguments?**
   - A. Yes, it can take any number of arguments
   - B. Yes, but only one argument
   - C. No, destructors cannot take arguments
   - D. Only when the destructor is virtual

   **Answer:** C

7. **What is the sequence of destructor calls in a class hierarchy (e.g., derived class object)?**
   - A. Derived class first, then base class
   - B. Base class first, then derived class
   - C. In random order
   - D. Only base class destructor is called

   **Answer:** A

8. **Which of the following statements about destructors is correct?**
   - A. Destructors can be overloaded
   - B. Destructors must return an integer
   - C. A class can have only one destructor
   - D. Destructors are automatically called in any order

   **Answer:** C

9. **What happens if a class with a pointer data member doesn’t define a destructor?**
   - A. The pointer memory is automatically deallocated
   - B. The object’s pointer may cause a memory leak
   - C. The pointer is copied to the stack
   - D. The program will throw an error at compile-time

   **Answer:** B

10. **Which of the following describes a situation where you might need a virtual destructor?**
    - A. When the class has only integer members
    - B. When you use inheritance and need to delete a derived class object via a base class pointer
    - C. When the class has no dynamic memory allocation
    - D. When the class does not use inheritance

   **Answer:** B

---

# 6. MCQs on Polymorphism, Compile-Time and Runtime Polymorphism, Function Overloading, Constructor Overloading, and Function Overriding :

---

## Easy

1. **What is polymorphism in C++?**
   - A. The ability to inherit properties from a base class
   - B. The ability to have multiple functions with the same name but different implementations
   - C. The ability to have multiple inheritance
   - D. The ability to write code without classes

   **Answer:** B

2. **Which of the following best describes compile-time polymorphism?**
   - A. Determining the function to be executed at runtime
   - B. Overloading functions or operators
   - C. Using virtual functions
   - D. Using pure virtual functions

   **Answer:** B

3. **What is function overloading?**
   - A. Using the same function name with different parameters
   - B. Using the same function name and parameters
   - C. Using virtual functions
   - D. Reusing code from a base class

   **Answer:** A

4. **What is runtime polymorphism?**
   - A. Deciding which function to call at compile-time
   - B. Deciding which function to call at runtime
   - C. Deciding which class to inherit
   - D. Determining the type of a variable at compile-time

   **Answer:** B

5. **Which keyword is used to implement runtime polymorphism in C++?**
   - A. `virtual`
   - B. `static`
   - C. `final`
   - D. `override`

   **Answer:** A

---

## Medium

6. **What is constructor overloading?**
   - A. Using a single constructor in multiple classes
   - B. Having multiple constructors with different parameters in the same class
   - C. Creating constructors with the same parameter type
   - D. Using the `virtual` keyword with constructors

   **Answer:** B

7. **Which of the following is required to implement function overriding?**
   - A. The `static` keyword
   - B. The same function name with different parameter lists
   - C. A derived class and a virtual function in the base class
   - D. Constructors with the same name in different classes

   **Answer:** C

8. **In function overloading, which of the following differs between the overloaded functions?**
   - A. The function name
   - B. The return type
   - C. The parameter list
   - D. The function name and return type

   **Answer:** C

9. **What is the output if a virtual function is called on a base class pointer pointing to a derived class object?**
   - A. The base class version of the function
   - B. The derived class version of the function
   - C. A compile-time error
   - D. A runtime error

   **Answer:** B

10. **Which of the following supports dynamic (runtime) polymorphism in C++?**
    - A. Function overloading
    - B. Constructor overloading
    - C. Virtual functions
    - D. Template functions

    **Answer:** C

---

## Hard

11. **What will happen if a derived class function is defined without the `override` keyword?**
    - A. It will not override the base class function
    - B. It will throw a compilation error
    - C. It will override the base class function if it has the same signature
    - D. The program will throw a runtime error

    **Answer:** C

12. **In C++, what does the `final` keyword do when used with a function?**
    - A. Prevents the function from being called
    - B. Prevents the function from being overridden in derived classes
    - C. Forces the function to be overridden
    - D. Makes the function a pure virtual function

    **Answer:** B

13. **Which of the following allows an object to take many forms in polymorphism?**
    - A. Type inference
    - B. Inheritance and virtual functions
    - C. Templates
    - D. Overloading operators

    **Answer:** B

14. **Which of the following is true about function overloading and function overriding?**
    - A. Function overloading occurs only in base classes
    - B. Function overriding can be done with non-virtual functions
    - C. Function overloading is compile-time polymorphism, and function overriding is runtime polymorphism
    - D. Both are types of runtime polymorphism

    **Answer:** C

15. **Which of the following statements is correct about constructors and polymorphism?**
    - A. Constructors can be virtual
    - B. Constructors support runtime polymorphism
    - C. Constructors cannot be virtual
    - D. Constructors can be overridden like virtual functions

    **Answer:** C

16. **What would happen if two overloaded functions have the same name and parameter types but different return types?**
    - A. The compiler will choose the function with the appropriate return type
    - B. The function with the highest return type is selected
    - C. A compilation error will occur
    - D. Both functions will execute

    **Answer:** C

17. **Which feature is used to call a base class method in the derived class if it has been overridden?**
    - A. The `this` pointer
    - B. The base class name and scope resolution operator
    - C. The `virtual` keyword
    - D. The `override` keyword

    **Answer:** B

18. **Which of the following statements about pure virtual functions is correct?**
    - A. They provide an implementation in the base class
    - B. They cannot be overridden in derived classes
    - C. They must be implemented in derived classes
    - D. They must be called directly

    **Answer:** C

19. **Which of the following scenarios best describes when constructor overloading is useful?**
    - A. When a class has multiple inheritance
    - B. When a class needs multiple ways to initialize its objects
    - C. When a class contains pure virtual functions
    - D. When a class contains only static members

    **Answer:** B

20. **Which of the following is true regarding virtual destructors?**
    - A. They are used to prevent memory leaks in polymorphic classes
    - B. They cannot be used in derived classes
    - C. They override the base class constructor
    - D. They cause memory leaks in non-polymorphic classes

    **Answer:** A

---

# 7. MCQs on Virtual Functions

---

## Easy

1. **What is a virtual function in C++?**
   - A. A function that doesn’t have a return type
   - B. A function that can be overridden in derived classes
   - C. A function that is always called at compile-time
   - D. A function that can only be used in base classes

   **Answer:** B

2. **What keyword is used to declare a virtual function in C++?**
   - A. `override`
   - B. `virtual`
   - C. `abstract`
   - D. `protected`

   **Answer:** B

3. **Which of the following describes a pure virtual function?**
   - A. A function with no parameters
   - B. A function defined in the base class with an implementation
   - C. A virtual function with no definition in the base class
   - D. A function that must be implemented in the base class

   **Answer:** C

4. **What is the purpose of a virtual function?**
   - A. To allow function calls to be determined at compile-time
   - B. To allow derived classes to override the base class function
   - C. To allow only one implementation in the class hierarchy
   - D. To prevent inheritance

   **Answer:** B

5. **If a virtual function in a base class is overridden in the derived class, which function is called when accessed through a base class pointer to the derived object?**
   - A. The base class version
   - B. The derived class version
   - C. Both versions
   - D. None of the above

   **Answer:** B

---

## Medium

6. **What is the output if a non-virtual function is called on a base class pointer pointing to a derived class object?**
   - A. Base class function is called
   - B. Derived class function is called
   - C. It depends on the compiler
   - D. An error occurs

   **Answer:** A

7. **What is the primary benefit of using virtual functions in a base class?**
   - A. To ensure derived classes cannot override functions
   - B. To allow derived classes to have their own implementations
   - C. To make the class final
   - D. To make the function accessible to all classes

   **Answer:** B

8. **Which of the following statements about virtual destructors is true?**
   - A. They prevent derived class destructors from being called
   - B. They are only useful in non-polymorphic classes
   - C. They ensure the proper destructor calls in polymorphic classes
   - D. They cause memory leaks in derived classes

   **Answer:** C

---

## Hard

9. **Which of the following correctly defines a pure virtual function?**
   - A. `virtual void display() {}`
   - B. `void display() = 0;`
   - C. `virtual void display() = 0;`
   - D. `void display();`

   **Answer:** C

10. **If a derived class does not override a pure virtual function from the base class, what is the result?**
    - A. The derived class becomes abstract
    - B. The derived class can still be instantiated
    - C. The compiler will add a default implementation
    - D. The function is ignored

   **Answer:** A
---

# 8. MCQs on Abstraction and Abstract Classes

---

## Easy

1. **What is abstraction in C++?**
   - A. The process of inheriting multiple classes
   - B. The process of hiding implementation details and showing only functionality
   - C. The use of constructors and destructors
   - D. The ability to have multiple classes with the same name

   **Answer:** B

2. **What is an abstract class in C++?**
   - A. A class with at least one pure virtual function
   - B. A class with only private members
   - C. A class that cannot be inherited
   - D. A class with only static members

   **Answer:** A

3. **Which of the following can be used to define an abstract class in C++?**
   - A. A class with only private methods
   - B. A class with a `final` keyword
   - C. A class with at least one pure virtual function
   - D. A class with no constructors

   **Answer:** C

4. **How is a pure virtual function declared in C++?**
   - A. `void function() = 1;`
   - B. `virtual void function() = 0;`
   - C. `void function();`
   - D. `virtual void function();`

   **Answer:** B

5. **What happens if a derived class does not override a pure virtual function?**
   - A. It will cause a runtime error
   - B. The derived class becomes an abstract class
   - C. The pure virtual function is ignored
   - D. The derived class cannot access the function

   **Answer:** B

---

## Medium

6. **Can an abstract class in C++ be instantiated?**
   - A. Yes, always
   - B. No, an abstract class cannot be instantiated
   - C. Only if it has no pure virtual functions
   - D. Only in derived classes

   **Answer:** B

7. **What is the primary purpose of abstraction in object-oriented programming?**
   - A. To manage memory efficiently
   - B. To simplify complex systems by focusing on high-level operations
   - C. To allow multiple inheritance
   - D. To enable polymorphism

   **Answer:** B

8. **Which of the following statements is true about abstract classes?**
   - A. Abstract classes cannot contain non-virtual functions
   - B. Abstract classes can have both implemented and pure virtual functions
   - C. Abstract classes cannot have member variables
   - D. Abstract classes must be inherited to access their members

   **Answer:** B

9. **If a base class is abstract, then what is true of any derived class?**
   - A. It must also be abstract
   - B. It must implement all pure virtual functions to be non-abstract
   - C. It can ignore the pure virtual functions
   - D. It must override all member functions

   **Answer:** B

10. **What is the syntax to declare a class `Base` as an abstract class with a pure virtual function `display`?**
    - A. `class Base { void display() {}; };`
    - B. `class Base { virtual void display(); };`
    - C. `class Base { virtual void display() = 0; };`
    - D. `class Base { display() = 0; };`

    **Answer:** C

---

## Hard

11. **Why are pure virtual functions often declared in base classes?**
    - A. To ensure derived classes implement the function
    - B. To prevent derived classes from being instantiated
    - C. To provide an implementation in the base class
    - D. To enable function overloading

    **Answer:** A

12. **What will happen if a class has no pure virtual functions but inherits from an abstract class?**
    - A. It automatically becomes abstract
    - B. It remains a concrete class if it implements all inherited pure virtual functions
    - C. It cannot inherit from an abstract class
    - D. It will become abstract only if a virtual function is redefined

    **Answer:** B

13. **Which of the following best describes when to use an abstract class?**
    - A. When the base class needs to provide a complete implementation
    - B. When the base class is meant to define a common interface but not be instantiated
    - C. When the class should not be inherited
    - D. When only static methods are required

    **Answer:** B

14. **Can an abstract class contain a constructor in C++?**
    - A. No, abstract classes cannot have constructors
    - B. Yes, but it cannot be called
    - C. Yes, constructors in abstract classes are used to initialize data members
    - D. Only if it contains no pure virtual functions

    **Answer:** C

15. **Which of the following statements is correct about member variables in abstract classes?**
    - A. Abstract classes cannot have member variables
    - B. Abstract classes can have member variables, which can be initialized in constructors
    - C. Member variables must be static in abstract classes
    - D. Member variables in abstract classes cannot be accessed in derived classes

    **Answer:** B

---

# 9. MCQs on Static Keyword, Static Variables, and Static Objects

---

## Easy

1. **What does the `static` keyword indicate when used with a variable in C++?**
   - A. The variable can be accessed from any function
   - B. The variable retains its value between function calls
   - C. The variable is only available in the current block
   - D. The variable is a constant

   **Answer:** B

2. **Which of the following is true about static variables in a function?**
   - A. They are re-initialized each time the function is called
   - B. They are initialized only once and retain their value between function calls
   - C. They cannot be used in recursive functions
   - D. They are only accessible within the function where they are declared

   **Answer:** B

3. **How is a static member variable defined in a class?**
   - A. `static int x;`
   - B. `int static x;`
   - C. `static int x();`
   - D. `int x = static;`

   **Answer:** A

4. **What is the lifetime of a static variable in C++?**
   - A. Until the end of the block in which it is defined
   - B. Until the end of the program
   - C. Until the end of the function in which it is defined
   - D. Until it is explicitly deleted

   **Answer:** B

5. **What will happen if you declare a static variable in a loop?**
   - A. It will be initialized every time the loop iterates
   - B. It will retain its value between iterations of the loop
   - C. It will not compile
   - D. It will be treated as a global variable

   **Answer:** B

---

## Medium

6. **Which of the following statements about static member functions is correct?**
   - A. They can access non-static member variables directly
   - B. They cannot be called without an object
   - C. They can be called using the class name
   - D. They can only be declared in derived classes

   **Answer:** C

7. **When a static member variable is declared in a class, where is it stored?**
   - A. In the stack memory
   - B. In the heap memory
   - C. In the data segment of the memory
   - D. In the code segment of the memory

   **Answer:** C

8. **How do you initialize a static member variable of a class?**
   - A. It can only be initialized inside the constructor
   - B. It must be initialized outside the class definition
   - C. It cannot be initialized
   - D. It can be initialized within any member function

   **Answer:** B

9. **Which of the following is a valid declaration of a static object?**
   - A. `static Object obj;`
   - B. `Object static obj;`
   - C. `static Object obj();`
   - D. `Object obj = static;`

   **Answer:** A

10. **What is the purpose of static objects?**
    - A. To allow multiple instances of a class
    - B. To ensure that an object has a single instance throughout the program
    - C. To limit the scope of an object to a function
    - D. To create a temporary object that can be reused

    **Answer:** B

---

## Hard

11. **What will happen if you attempt to declare a static variable in a header file without using `extern`?**
    - A. It will lead to linker errors due to multiple definitions
    - B. It will work without issues
    - C. It will cause a compilation error
    - D. It will be treated as a global variable

    **Answer:** A

12. **Which of the following statements about static variables in classes is true?**
    - A. Each object of the class has its own copy of the static variable
    - B. Static variables are shared among all objects of the class
    - C. Static variables cannot be accessed outside the class
    - D. Static variables can be modified only within member functions

    **Answer:** B

13. **Can a static member function be declared as `const` in C++?**
    - A. Yes, it can
    - B. No, it cannot
    - C. Only if it has no parameters
    - D. Only if it is defined outside the class

    **Answer:** B

14. **What is the output of the following code snippet?**
    ```cpp
    void function() {
        static int x = 0;
        x++;
        std::cout << x << std::endl;
    }

    int main() {
        function();
        function();
        function();
        return 0;
    }
    ```
    - A. 1 2 3
    - B. 0 0 0
    - C. 1 1 1
    - D. 1 2 2

    **Answer:** A

15. **Which of the following is NOT a characteristic of static member variables?**
    - A. They are shared among all instances of a class
    - B. They are initialized only once
    - C. They can be initialized in the constructor
    - D. They can be accessed using the class name

    **Answer:** C
