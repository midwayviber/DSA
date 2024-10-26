Here's a detailed and structured markdown guide on **Object-Oriented Programming (OOP)** in C++ with definitions, explanations, and code examples for each topic in **Easy**, **Medium**, and **Hard** categories.

```markdown
# Object-Oriented Programming (OOP) in C++

## Easy

### 1. Classes and Objects
- **Definition**: A class is a blueprint for creating objects, containing properties (data) and methods (functions). An object is an instance of a class.
  
#### Example:
```cpp
#include <iostream>
using namespace std;

class Car {
public:
    string brand;
    int year;

    void display() {
        cout << "Brand: " << brand << ", Year: " << year << endl;
    }
};

int main() {
    Car car1;
    car1.brand = "Toyota";
    car1.year = 2020;
    car1.display();
    return 0;
}
```

---

### 2. Encapsulation
- **Definition**: Encapsulation is the concept of bundling data and methods that operate on the data within a single unit (class). It is achieved using access specifiers (`private`, `protected`, `public`) to control access to the members.

#### Example:
```cpp
#include <iostream>
using namespace std;

class BankAccount {
private:
    double balance;

public:
    BankAccount(double initialBalance) : balance(initialBalance) {}

    void deposit(double amount) {
        balance += amount;
    }

    void withdraw(double amount) {
        if (amount <= balance) {
            balance -= amount;
        } else {
            cout << "Insufficient balance!" << endl;
        }
    }

    double getBalance() const {
        return balance;
    }
};

int main() {
    BankAccount account(1000);
    account.deposit(500);
    account.withdraw(200);
    cout << "Balance: $" << account.getBalance() << endl;
    return 0;
}
```

---

### 3. Inheritance (Basic)
- **Definition**: Inheritance allows a class (derived class) to inherit properties and methods from another class (base class), enabling code reuse.

#### Example:
```cpp
#include <iostream>
using namespace std;

class Animal {
public:
    void sound() {
        cout << "Some generic animal sound" << endl;
    }
};

class Dog : public Animal {
public:
    void bark() {
        cout << "Woof!" << endl;
    }
};

int main() {
    Dog dog;
    dog.sound(); // Inherited method from Animal class
    dog.bark();  // Method from Dog class
    return 0;
}
```

---

## Medium

### 4. Polymorphism (Compile-time)
- **Definition**: Polymorphism allows entities to take on multiple forms. Compile-time polymorphism is achieved through function overloading and operator overloading.

#### Function Overloading Example:
```cpp
#include <iostream>
using namespace std;

class MathOperations {
public:
    int add(int a, int b) {
        return a + b;
    }

    double add(double a, double b) {
        return a + b;
    }
};

int main() {
    MathOperations math;
    cout << "Int add: " << math.add(5, 3) << endl;
    cout << "Double add: " << math.add(5.5, 3.2) << endl;
    return 0;
}
```

#### Operator Overloading Example:
```cpp
#include <iostream>
using namespace std;

class Complex {
private:
    double real, imag;

public:
    Complex(double r = 0, double i = 0) : real(r), imag(i) {}

    Complex operator + (const Complex& other) {
        return Complex(real + other.real, imag + other.imag);
    }

    void display() const {
        cout << real << " + " << imag << "i" << endl;
    }
};

int main() {
    Complex c1(3.5, 2.5), c2(1.5, 1.5);
    Complex c3 = c1 + c2;
    c3.display();
    return 0;
}
```

---

### 5. Inheritance (Multiple Inheritance)
- **Definition**: Multiple inheritance allows a class to inherit from more than one base class. This can lead to ambiguity if two base classes have members with the same name.

#### Example:
```cpp
#include <iostream>
using namespace std;

class Base1 {
public:
    void show() {
        cout << "Base1 show()" << endl;
    }
};

class Base2 {
public:
    void show() {
        cout << "Base2 show()" << endl;
    }
};

class Derived : public Base1, public Base2 {
public:
    void display() {
        Base1::show(); // Resolving ambiguity
        Base2::show();
    }
};

int main() {
    Derived obj;
    obj.display();
    return 0;
}
```

---

### 6. Virtual Functions
- **Definition**: Virtual functions allow derived classes to override methods in the base class, providing dynamic (run-time) polymorphism.

#### Example:
```cpp
#include <iostream>
using namespace std;

class Animal {
public:
    virtual void sound() {
        cout << "Some generic animal sound" << endl;
    }
};

class Dog : public Animal {
public:
    void sound() override {
        cout << "Woof!" << endl;
    }
};

int main() {
    Animal* animal = new Dog();
    animal->sound(); // Calls Dog's sound() due to dynamic binding
    delete animal;
    return 0;
}
```

---

### 7. Abstract Classes
- **Definition**: An abstract class is a class with at least one pure virtual function, making it uninstantiable. It's used to define interfaces for derived classes.

#### Example:
```cpp
#include <iostream>
using namespace std;

class Shape {
public:
    virtual void draw() = 0; // Pure virtual function
};

class Circle : public Shape {
public:
    void draw() override {
        cout << "Drawing a circle" << endl;
    }
};

int main() {
    Shape* shape = new Circle();
    shape->draw();
    delete shape;
    return 0;
}
```

---

## Hard

### 8. Run-time Polymorphism
- **Definition**: Run-time polymorphism is achieved through virtual functions, allowing derived classes to override base class methods with their own implementations. The compiler uses virtual tables (vTables) to manage dynamic binding.

#### Example:
```cpp
#include <iostream>
using namespace std;

class Animal {
public:
    virtual void sound() {
        cout << "Some generic animal sound" << endl;
    }
};

class Cat : public Animal {
public:
    void sound() override {
        cout << "Meow!" << endl;
    }
};

int main() {
    Animal* animal = new Cat();
    animal->sound(); // Calls Cat's sound() due to vTable
    delete animal;
    return 0;
}
```

---

### 9. Diamond Problem and Virtual Inheritance
- **Definition**: The diamond problem occurs when a derived class inherits from two classes that both inherit from the same base class. Virtual inheritance solves this by sharing a single instance of the base class.

#### Example:
```cpp
#include <iostream>
using namespace std;

class Animal {
public:
    void sound() {
        cout << "Some generic animal sound" << endl;
    }
};

class Mammal : virtual public Animal {};
class Bird : virtual public Animal {};

class Bat : public Mammal, public Bird {};

int main() {
    Bat bat;
    bat.sound(); // No ambiguity due to virtual inheritance
    return 0;
}
```

---

### 10. Virtual Destructors
- **Definition**: Virtual destructors ensure that the destructor of a derived class is called when an object is deleted through a pointer to the base class.

#### Example:
```cpp
#include <iostream>
using namespace std;

class Base {
public:
    virtual ~Base() {
        cout << "Base destructor called" << endl;
    }
};

class Derived : public Base {
public:
    ~Derived() {
        cout << "Derived destructor called" << endl;
    }
};

int main() {
    Base* obj = new Derived();
    delete obj; // Calls Derived destructor, then Base destructor
    return 0;
}
```

