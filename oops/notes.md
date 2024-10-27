# OOPs (Object-Oriented Programming)

Object-Oriented Programming (OOP) is a programming paradigm based on the concept of "objects," which can contain data and methods. OOP focuses on using these objects as the fundamental building blocks for building applications, enabling modularity, reuse, and scalability.

### Key Concepts of OOP:
1. **Encapsulation**: Bundling data and methods that operate on the data within one unit, such as a class.
2. **Abstraction**: Hiding complex implementation details and showing only the necessary features of an object.
3. **Inheritance**: Deriving new classes from existing ones, enabling code reuse.
4. **Polymorphism**: Allowing objects to be treated as instances of their parent class, especially when overriding methods.

![WhatsApp Image 2024-10-28 at 03 13 14_d6c0dd9e](https://github.com/user-attachments/assets/69322156-e2a9-43a0-bb27-b6b2ea10f5d3)

---

# Constructor

A constructor is a special method that is automatically called when an object of a class is created. It initializes the object and allocates memory for it.

### Example:
```cpp
class Example {
public:
    Example() {
        cout << "Constructor called!" << endl;
    }
};
```

![WhatsApp Image 2024-10-28 at 03 13 58_99519b04](https://github.com/user-attachments/assets/27788b8f-7814-485f-ac7e-83327477a3b2)

---

# Parameterized Constructor

A parameterized constructor allows passing parameters to initialize an object with specific values when it is created.

### Example:
```cpp
class Example {
public:
    int x;
    Example(int val) {
        x = val;
    }
};
```

![WhatsApp Image 2024-10-28 at 03 14 00_aa4d1982](https://github.com/user-attachments/assets/b69b88de-d6b7-4986-ac94-8bab37f8efbc)

---

# `this` Pointer

The `this` pointer is an implicit parameter to all member functions. It refers to the object invoking the member function, allowing access to its members.

### Example:
```cpp
class Example {
public:
    int x;
    Example(int x) {
        this->x = x;
    }
};
```

![WhatsApp Image 2024-10-28 at 03 14 06_b5fb3d30](https://github.com/user-attachments/assets/9ee0f8aa-ad4e-4054-8015-9e426d82cd78)

---

# Copy Constructor

A copy constructor creates a new object as a copy of an existing object. This is essential for defining how an object should be duplicated.

### Example:
```cpp
class Example {
public:
    int x;
    Example(const Example &obj) {
        x = obj.x;
    }
};
```

![WhatsApp Image 2024-10-28 at 03 14 12_d3f6ccfb](https://github.com/user-attachments/assets/9395daca-b4ca-4321-a6fa-cafc3c090e24)

---

# Destructor

A destructor is a method that is automatically called when an object goes out of scope or is deleted. It is used to release resources.

### Example:
```cpp
class Example {
public:
    ~Example() {
        cout << "Destructor called!" << endl;
    }
};
```

![WhatsApp Image 2024-10-28 at 03 14 18_49b97ab6](https://github.com/user-attachments/assets/4eaeb7c7-a61f-4aae-8084-f0a7eade6239)

---

# Polymorphism

Polymorphism allows one interface to be used for different underlying data types, enhancing flexibility and integration.

### Types of Polymorphism:
- **Compile-time Polymorphism**: Achieved through function overloading and operator overloading.
- **Runtime Polymorphism**: Achieved through inheritance and virtual functions.

![WhatsApp Image 2024-10-28 at 03 14 23_0f2e8a9a](https://github.com/user-attachments/assets/3b2b4cce-1bd1-47e2-a714-dda0ad51939d)

---

# Compile-Time and Run-Time Polymorphism

- **Compile-Time Polymorphism**: Function and operator overloading.
- **Run-Time Polymorphism**: Virtual functions and pointers to base classes.

![WhatsApp Image 2024-10-28 at 03 14 31_a12bfbe6](https://github.com/user-attachments/assets/cfeb2726-39ea-4a8c-928d-239be9228d9f)

---

# Function Overloading

Function overloading allows multiple functions with the same name but different parameters.

### Example:
```cpp
class Example {
public:
    void func(int x) { cout << "Integer: " << x << endl; }
    void func(double x) { cout << "Double: " << x << endl; }
};
```

![WhatsApp Image 2024-10-28 at 03 14 37_d75450a1](https://github.com/user-attachments/assets/b6601225-5389-4b50-bd1e-8e2aed50823f)

---

# Virtual Functions

A virtual function allows derived classes to override it, enabling polymorphic behavior.

### Example:
```cpp
class Base {
public:
    virtual void show() { cout << "Base class" << endl; }
};
class Derived : public Base {
public:
    void show() override { cout << "Derived class" << endl; }
};
```

![WhatsApp Image 2024-10-28 at 03 14 55_7f353902](https://github.com/user-attachments/assets/ce9d4ed0-035d-420c-9e2f-bed685a05fe0)

---

# Abstraction

Abstraction hides implementation details, exposing only essential features, which simplifies usage.

### Example:
```cpp
class AbstractShape {
public:
    virtual void draw() = 0;  // Pure virtual function
};
```

![WhatsApp Image 2024-10-28 at 03 15 09_9ccb83e2](https://github.com/user-attachments/assets/53ddf21e-ceb2-45f0-a579-f39309983b7a)

---

# Static Keyword

The `static` keyword makes a variable or function belong to the class instead of instances of the class. Static members are shared among all instances.

### Example:
```cpp
class Example {
public:
    static int count;
};
int Example::count = 0;
```

![WhatsApp Image 2024-10-28 at 03 15 19_d7d6b9c6](https://github.com/user-attachments/assets/e7604366-c3da-4c8b-8636-63756aff7481)
```

