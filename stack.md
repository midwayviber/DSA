# Advanced Stack Questions

### True/False Questions

1. **True/False**: A stack implemented with a linked list does not require a fixed size.
   - **Answer**: True

2. **True/False**: In stack implementation using arrays, overflow can occur if the stack is full.
   - **Answer**: True

3. **True/False**: The `pop()` operation in a stack has a time complexity of O(n).
   - **Answer**: False (It’s O(1))

4. **True/False**: Stacks can be used to convert infix expressions to postfix expressions.
   - **Answer**: True

5. **True/False**: Stacks can only store homogeneous data types.
   - **Answer**: False (Stacks can store any data type depending on implementation)

6. **True/False**: Recursion can be simulated using a stack data structure.
   - **Answer**: True

7. **True/False**: The `isEmpty()` function in a stack implementation typically has a time complexity of O(1).
   - **Answer**: True

8. **True/False**: A stack’s primary operations are `push()`, `pop()`, `peek()`, and `clear()`.
   - **Answer**: True

9. **True/False**: The peek operation removes the top element from the stack.
   - **Answer**: False (It only retrieves it)

10. **True/False**: Stacks can be used to implement Depth-First Search (DFS) algorithms.
    - **Answer**: True

### Code Debugging Questions

11. **True/False**: The following code correctly initializes an empty stack in Python:
    ```python
    stack = []
    ```
    - **Answer**: True

12. **True/False**: In the code below, the stack will be empty after execution:
    ```python
    stack = [1, 2, 3]
    stack.pop()
    stack.pop()
    stack.pop()
    ```
    - **Answer**: True

13. **True/False**: This code will cause a stack overflow if `n` is too large:
    ```python
    def factorial(n):
        if n == 0:
            return 1
        return n * factorial(n - 1)
    ```
    - **Answer**: True

14. **True/False**: The following code will throw an error when trying to access `stack[-1]`:
    ```python
    stack = []
    top_element = stack[-1]
    ```
    - **Answer**: True

15. **True/False**: This code will correctly print all elements in the stack:
    ```python
    stack = [1, 2, 3]
    while stack:
        print(stack.pop())
    ```
    - **Answer**: True

16. **True/False**: The following code correctly checks if a stack is empty:
    ```python
    if len(stack) == 0:
        print("Stack is empty")
    ```
    - **Answer**: True

17. **True/False**: The following code performs a balanced parentheses check:
    ```python
    def is_balanced(expr):
        stack = []
        for char in expr:
            if char == '(':
                stack.append(char)
            elif char == ')':
                if not stack or stack.pop() != '(':
                    return False
        return not stack
    ```
    - **Answer**: True

18. **True/False**: This code correctly implements a stack class with a `push` and `pop` method:
    ```python
    class Stack:
        def __init__(self):
            self.stack = []

        def push(self, item):
            self.stack.append(item)

        def pop(self):
            return self.stack.pop() if self.stack else None
    ```
    - **Answer**: True

19. **True/False**: The following code incorrectly calculates the reverse of a string:
    ```python
    def reverse_string(s):
        stack = list(s)
        return ''.join(stack.pop() for _ in range(len(stack)))
    ```
    - **Answer**: False (It’s correct)

20. **True/False**: The `stack[-1]` expression gives the last element without removing it.
    - **Answer**: True

### Multiple Choice Questions (MCQs)

21. **What will be the output of the following code?**
    ```python
    stack = [1, 2, 3]
    stack.pop()
    stack.append(4)
    print(stack)
    ```
    - **Options**:
      - a) [1, 2]
      - b) [1, 2, 3]
      - c) [1, 2, 4]
      - d) Error
    - **Answer**: c) [1, 2, 4]

22. **What does the following code do?**
    ```python
    stack = []
    for i in range(5):
        stack.append(i)
    for i in range(5):
        print(stack.pop(), end=" ")
    ```
    - **Options**:
      - a) Prints numbers 0 to 4 in ascending order
      - b) Prints numbers 0 to 4 in descending order
      - c) Throws an error
      - d) None of the above
    - **Answer**: b) Prints numbers 0 to 4 in descending order

23. **In a stack, `pop` operation:**
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
      - c) `peek()` on a non-empty stack
      - d) None of the above
    - **Answer**: b) `pop()` on an empty stack

25. **What is the time complexity of `pop()` in a stack implemented with an array?**
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
