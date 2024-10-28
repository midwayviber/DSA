# Advanced Stack Questions (C++)

### True/False Questions

1. **True/False**: A stack implemented using `std::vector` in C++ can dynamically resize.
   - **Answer**: True

2. **True/False**: In C++, a stack cannot be empty if it has been initialized.
   - **Answer**: False

3. **True/False**: The `pop()` operation in a C++ stack class has a time complexity of O(n).
   - **Answer**: False (It’s O(1))

4. **True/False**: A stack can be used to evaluate postfix expressions in C++.
   - **Answer**: True

5. **True/False**: The `top()` function in C++ returns and removes the top element of the stack.
   - **Answer**: False (It only retrieves the top element)

6. **True/False**: You can create a stack of any data type in C++ using templates.
   - **Answer**: True

7. **True/False**: In C++, you cannot use a stack to reverse a string.
   - **Answer**: False

8. **True/False**: The `size()` function of a C++ stack has a time complexity of O(1).
   - **Answer**: True

9. **True/False**: You can use a `std::stack` to implement a queue.
   - **Answer**: True

10. **True/False**: The STL stack in C++ does not allow direct access to its elements.
    - **Answer**: True

### Code Debugging Questions

11. **True/False**: The following code correctly initializes an empty stack in C++:
    ```cpp
    std::stack<int> s;
    ```
    - **Answer**: True

12. **True/False**: The following code will throw an exception when trying to access the top element of an empty stack:
    ```cpp
    std::stack<int> s;
    int top = s.top();
    ```
    - **Answer**: True

13. **True/False**: The following code correctly pops all elements from the stack:
    ```cpp
    std::stack<int> s;
    s.push(1);
    s.push(2);
    s.pop();
    s.pop();
    ```
    - **Answer**: True

14. **True/False**: This code correctly checks if the stack is empty:
    ```cpp
    std::stack<int> s;
    if (s.empty()) {
        std::cout << "Stack is empty";
    }
    ```
    - **Answer**: True

15. **True/False**: The following code correctly implements a stack using a linked list:
    ```cpp
    struct Node {
        int data;
        Node* next;
    };

    class Stack {
        Node* top;
    public:
        Stack() { top = nullptr; }
        void push(int value);
        int pop();
    };
    ```
    - **Answer**: True

16. **True/False**: This code correctly reverses a string using a stack:
    ```cpp
    std::string reverseString(std::string s) {
        std::stack<char> stack;
        for (char c : s) stack.push(c);
        for (int i = 0; i < s.length(); i++) {
            s[i] = stack.top();
            stack.pop();
        }
        return s;
    }
    ```
    - **Answer**: True

17. **True/False**: The following code will output the elements in the order they were added:
    ```cpp
    std::stack<int> s;
    s.push(1);
    s.push(2);
    s.push(3);
    while (!s.empty()) {
        std::cout << s.top() << " ";
        s.pop();
    }
    ```
    - **Answer**: False (It outputs in reverse order)

18. **True/False**: The following code checks for balanced parentheses correctly:
    ```cpp
    bool isBalanced(const std::string& expr) {
        std::stack<char> s;
        for (char c : expr) {
            if (c == '(') s.push(c);
            else if (c == ')') {
                if (s.empty()) return false;
                s.pop();
            }
        }
        return s.empty();
    }
    ```
    - **Answer**: True

19. **True/False**: The following code will lead to a stack overflow if called with a large value of `n`:
    ```cpp
    int factorial(int n) {
        if (n <= 1) return 1;
        return n * factorial(n - 1);
    }
    ```
    - **Answer**: True

20. **True/False**: The following code properly implements a custom stack class:
    ```cpp
    class MyStack {
        std::vector<int> stack;
    public:
        void push(int value) { stack.push_back(value); }
        int pop() { int top = stack.back(); stack.pop_back(); return top; }
    };
    ```
    - **Answer**: True

### Multiple Choice Questions (MCQs)

21. **What will be the output of the following code?**
    ```cpp
    std::stack<int> s;
    s.push(10);
    s.push(20);
    s.pop();
    s.push(30);
    std::cout << s.top();
    ```
    - **Options**:
      - a) 10
      - b) 20
      - c) 30
      - d) 40
    - **Answer**: c) 30

22. **What does the following code do?**
    ```cpp
    std::stack<int> s;
    for (int i = 0; i < 5; i++) s.push(i);
    while (!s.empty()) { std::cout << s.top() << " "; s.pop(); }
    ```
    - **Options**:
      - a) Prints numbers 0 to 4 in ascending order
      - b) Prints numbers 0 to 4 in descending order
      - c) Throws an error
      - d) None of the above
    - **Answer**: b) Prints numbers 0 to 4 in descending order

23. **In a stack, which operation:**
    - **Options**:
      - a) Adds an element
      - b) Removes the top element
      - c) Retrieves the top element without removing it
      - d) Removes an element from the bottom
    - **Answer**: b) Removes the top element

24. **Which of the following operations will cause an underflow in a stack?**
    - **Options**:
      - a) `push()` on an empty stack
      - b) `pop()` on an empty stack
      - c) `top()` on a non-empty stack
      - d) None of the above
    - **Answer**: b) `pop()` on an empty stack

25. **What is the time complexity of `pop()` in a stack implemented with a `std::vector`?**
    - **Options**:
      - a) O(n)
      - b) O(log n)
      - c) O(1)
      - d) None of the above
    - **Answer**: c) O(1)

26. **If you perform two `push()` operations followed by two `pop()` operations, the stack will:**
    - **Options**:
      - a) Be empty
      - b) Contain one element
      - c) Contain two elements
      - d) Cause an overflow
    - **Answer**: a) Be empty

27. **In a postfix expression evaluator using a stack, what happens when an operator is encountered?**
    - **Options**:
      - a) It is pushed onto the stack
      - b) Two elements are popped, operated on, and the result is pushed back
      - c) It is ignored
      - d) None of the above
    - **Answer**: b) Two elements are popped, operated on, and the result is pushed back

28. **Which of the following is a valid postfix expression?**
    - **Options**:
      - a) A + B *
      - b) AB+C*
      - c) (A + B) * C
      - d) None of the above
    - **Answer**: b) AB+C*

29. **In an infix to postfix conversion algorithm, an operator is pushed to the stack if:**
    - **Options**:
      - a) It has higher precedence than the operator on the stack
      - b) It has lower precedence than the operator on the stack
      - c) It is the same precedence as the operator on the stack
      - d) The stack is empty
    - **Answer**: a) It has higher precedence than the operator on the stack

30. **In a stack-based Depth-First Search (DFS) algorithm, what happens when a node has no unvisited adjacent nodes?**
    - **Options**:
      - a) The node is removed from the stack
      - b) The search is terminated
      - c) The node is marked as visited
      - d) None of the above
    - **Answer**: a) The node is removed from the stack

