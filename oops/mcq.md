# Object-Oriented Programming (OOP) in C++ MCQs

---

## Easy Questions

1. **What is a class in C++?**
   - A) A function
   - B) A blueprint for creating objects
   - C) A variable type
   - D) A compiler option
   - **Answer:** B

2. **What is an object in C++?**
   - A) A piece of code
   - B) A blueprint for creating classes
   - C) An instance of a class
   - D) A type of function
   - **Answer:** C

3. **Which access specifier is used to allow access only within the same class?**
   - A) public
   - B) private
   - C) protected
   - D) external
   - **Answer:** B

4. **What keyword is used to create an object in C++?**
   - A) new
   - B) struct
   - C) object
   - D) class
   - **Answer:** D

5. **Which of the following allows access to derived class members but not outside classes?**
   - A) private
   - B) public
   - C) protected
   - D) internal
   - **Answer:** C

6. **Encapsulation in C++ is implemented using:**
   - A) Inheritance
   - B) Functions
   - C) Classes and objects
   - D) Pointers
   - **Answer:** C

7. **Which of the following is not a feature of OOP?**
   - A) Polymorphism
   - B) Inheritance
   - C) Encapsulation
   - D) Global variables
   - **Answer:** D

8. **What is the default access specifier for class members in C++?**
   - A) private
   - B) public
   - C) protected
   - D) external
   - **Answer:** A

9. **Which function runs automatically when an object is created?**
   - A) Destructor
   - B) Constructor
   - C) Accessor
   - D) Mutator
   - **Answer:** B

10. **Inheritance enables:**
    - A) Code reusability
    - B) Multiple objects
    - C) Memory optimization
    - D) Data security
    - **Answer:** A

11. **Which of the following is a type of polymorphism in C++?**
    - A) Function overloading
    - B) Data hiding
    - C) Access specifier
    - D) Virtual functions
    - **Answer:** A

12. **An abstract class in C++ is created using:**
    - A) Constructor
    - B) Virtual function
    - C) Pure virtual function
    - D) Destructor
    - **Answer:** C

13. **What is the purpose of a destructor in C++?**
    - A) To create objects
    - B) To initialize variables
    - C) To clean up resources when an object is deleted
    - D) To overload functions
    - **Answer:** C

14. **What does `this` pointer represent?**
    - A) A pointer to the object itself
    - B) A pointer to the class
    - C) A pointer to the main function
    - D) A pointer to the parent class
    - **Answer:** A

15. **Which of the following is not a type of inheritance?**
    - A) Single
    - B) Multiple
    - C) Composite
    - D) Multilevel
    - **Answer:** C

16. **Static members of a class are shared among:**
    - A) All instances of the class
    - B) Only one object
    - C) Private members
    - D) Protected members
    - **Answer:** A

17. **Which of the following keywords is used for inheritance?**
    - A) implement
    - B) inherit
    - C) extends
    - D) : (colon)
    - **Answer:** D

18. **Which feature allows the same function to behave differently in different classes?**
    - A) Encapsulation
    - B) Inheritance
    - C) Polymorphism
    - D) Abstraction
    - **Answer:** C

19. **How is data hiding achieved in C++?**
    - A) Using private members
    - B) Using inheritance
    - C) Using functions
    - D) Using public members
    - **Answer:** A

20. **What is another name for function overloading?**
    - A) Compile-time polymorphism
    - B) Runtime polymorphism
    - C) Abstraction
    - D) Data hiding
    - **Answer:** A

---

## Medium Questions

21. **Which operator is used to define a pointer to a member of a class?**
    - A) *
    - B) ::
    - C) ->
    - D) &
    - **Answer:** C

22. **Which of the following does not support dynamic polymorphism?**
    - A) Virtual functions
    - B) Operator overloading
    - C) Abstract classes
    - D) Interfaces
    - **Answer:** B

23. **In multiple inheritance, ambiguity is resolved using:**
    - A) Access specifiers
    - B) Virtual functions
    - C) Scope resolution operator
    - D) Static functions
    - **Answer:** C

24. **Which of the following is not a valid access specifier?**
    - A) public
    - B) internal
    - C) protected
    - D) private
    - **Answer:** B

25. **What does an abstract class contain at least one of?**
    - A) Pure virtual function
    - B) Static member
    - C) Private member
    - D) Inline function
    - **Answer:** A

26. **What is the function of the `new` keyword in C++?**
    - A) Deletes an object
    - B) Creates a class
    - C) Allocates memory
    - D) Copies an object
    - **Answer:** C

27. **The `delete` keyword in C++ is used to:**
    - A) Deallocate memory
    - B) Copy an object
    - C) Overload a function
    - D) Declare a variable
    - **Answer:** A

28. **Which of the following is true about virtual destructors?**
    - A) They do not exist in C++
    - B) They are called when an object is destroyed
    - C) They prevent memory leaks
    - D) Both B and C
    - **Answer:** D

29. **What happens when a base class destructor is non-virtual and an object of a derived class is deleted?**
    - A) Only base class destructor is called
    - B) Only derived class destructor is called
    - C) Both destructors are called
    - D) None are called
    - **Answer:** A

30. **Which of the following enables runtime polymorphism?**
    - A) Function overloading
    - B) Virtual functions
    - C) Operator overloading
    - D) Templates
    - **Answer:** B

31. **Which keyword is used to prevent a function from being overridden?**
    - A) static
    - B) const
    - C) final
    - D) override
    - **Answer:** C

32. **What is the purpose of the `override` keyword in C++?**
    - A) To create a base class
    - B) To create an abstract class
    - C) To explicitly declare that a function is intended to override a base class function
    - D) To prevent a function from being overridden
    - **Answer:** C

33. **What is `vTable` in C++?**
    - A) A table for virtual function pointers
    - B) A type of loop
    - C) A storage for class data members
    - D) An access specifier
    - **Answer:** A

34. **Which access specifier allows access to derived class but not to any other classes?**
    - A) public
    - B) private
    - C) protected
    - D) internal
    - **Answer:** C

35. **Which of the following is a feature of virtual inheritance?**
    - A) Reduces memory
    - B) Prevents multiple copies of base class in derived class
    - C) Increases security
    - D) Allows private inheritance
    - **Answer:** B

36. **How many constructors can a class have?**
    - A) Only one
    - B) Two
    - C) As many as needed
    - D) None
    - **Answer:** C

37. **Which type of inheritance is used to avoid the diamond problem?**
    - A) Multiple inheritance
    - B) Multilevel inheritance
    - C) Virtual inheritance
    - D) Hybrid inheritance
    - **Answer:** C

38. **Which of the following can only be used with pointers or references?**
    - A) Static functions
    - B) Virtual functions
    - C) Inline functions
    - D) Static members
    - **Answer:** B

39. **What is `dynamic_cast` used for?**
    - A) Type casting of primitive types
    - B) Type casting of pointers and references in inheritance hierarchies
    - C) To cast integers to floats
    - D) To cast floats to strings
    - **Answer:** B

40. **Which of the following is not true for polymorphism?**
    - A) It is a concept of OOP
    - B) It allows functions to behave differently
    - C) It is not possible in C++
    - D) It helps in code reusability
    - **Answer:** C

---

## Hard Questions

41. **What does `explicit` keyword do in C++?**
    - A) Marks a constructor as inline
    - B) Marks a function as inline
    - C) Prevents implicit conversion of constructors
    - D) Marks a function as protected
    - **Answer:** C

42. **Which of the following allows copying of objects with user-defined data types?**
    - A) Copy constructor
    - B) Destructor
    - C) Static function
    - D) Friend function
    - **Answer:** A

43. **What is the default return type of `main()` function?**
    - A) void
    - B) int
    - C) double
    - D) None
    - **Answer:** B

44. **What is the purpose of `typeid` operator in C++?**
    - A) Returns the type of a class
    - B) Returns the size of a class
    - C) Returns runtime type information of an object
    - D) Converts int to double
    - **Answer:** C

45. **Which keyword is used to handle memory leaks caused by destructors?**
    - A) virtual
    - B) explicit
    - C) inline
    - D) static
    - **Answer:** A

46. **What is the return type of a destructor?**
    - A) void
    - B) int
    - C) char
    - D) Destructors do not have a return type
    - **Answer:** D

47. **Which of the following can access private members of a class?**
    - A) Friend function
    - B) Public function
    - C) Protected function
    - D) Static function
    - **Answer:** A

48. **What is RAII in C++?**
    - A) Resource Allocation Is Initialization
    - B) Rapid Allocation Is Important
    - C) Reference Allocation Interface Initialization
    - D) Resource Allocation Important Interface
    - **Answer:** A

49. **Which of the following is true about `nullptr`?**
    - A) It is equivalent to 0
    - B) It has a dedicated type
    - C) It can be used as a boolean
    - D) None of the above
    - **Answer:** B

50. **What does `noexcept` keyword specify in a function?**
    - A) That a function throws an exception
    - B) That a function does not throw any exceptions
    - C) That a function returns nothing
    - D) That a function is private
    - **Answer:** B

51. **In which case would you use `std::move()`?**
    - A) When copying data
    - B) When moving data without copying
    - C) When initializing data
    - D) When destructing data
    - **Answer:** B

52. **Which of the following types can be overridden by derived classes?**
    - A) Pure virtual functions
    - B) Static functions
    - C) Constructor
    - D) Destructor
    - **Answer:** A

53. **What type of inheritance is prevented by C++?**
    - A) Single inheritance
    - B) Hybrid inheritance
    - C) Private inheritance
    - D) Circular inheritance
    - **Answer:** D

54. **What does `decltype` do in C++?**
    - A) Declares a class
    - B) Determines the type of a variable
    - C) Defines a pointer
    - D) Initializes an array
    - **Answer:** B

55. **Which of the following can be overloaded?**
    - A) Scope resolution operator
    - B) Assignment operator
    - C) Member selection operator
    - D) All of the above
    - **Answer:** B

56. **What is meant by shallow copy?**
    - A) Copy of primitive data only
    - B) Copy of objects and pointers only
    - C) Bitwise copy of an object
    - D) Recursive copy of data
    - **Answer:** C

57. **How is dynamic polymorphism achieved in C++?**
    - A) Using operator overloading
    - B) Using virtual functions
    - C) Using inline functions
    - D) Using static functions
    - **Answer:** B

58. **Which keyword is used to declare a function in a derived class to prevent hiding of the base class function?**
    - A) override
    - B) final
    - C) virtual
    - D) inline
    - **Answer:** A

59. **What does `static_assert` do in C++?**
    - A) Allows compile-time assertions
    - B) Allows runtime assertions
    - C) Checks memory usage
    - D) Validates pointers
    - **Answer:** A

60. **What is the purpose of `lambda` expressions in C++?**
    - A) Defines anonymous functions
    - B) Defines static variables
    - C) Enables polymorphism
    - D) Defines global variables
    - **Answer:** A
