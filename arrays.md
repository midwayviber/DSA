### 1. Given the array `int arr[10] = {0};`, what will be the output of the following code?
   ```cpp
   for(int i = 0; i < 10; ++i)
       arr[i] = arr[i] + i;
   std::cout << arr[5];
   ```
   - **a) 0**
   - **b) 5**
   - **c) 10**
   - **d) Compilation Error**

   **Answer:** **b) 5**

---

### 2. What will be the output of the following code?
   ```cpp
   int arr[] = {1, 2, 3, 4, 5};
   int *ptr = arr;
   std::cout << *(ptr + 3) << *(ptr++);
   ```
   - **a) 43**
   - **b) 42**
   - **c) Undefined behavior**
   - **d) Compilation error**

   **Answer:** **b) 42**

---

### 3. Which of the following correctly checks if an integer array `arr` of size `n` is sorted in non-decreasing order?
   ```cpp
   bool isSorted(int arr[], int n) {
       for (int i = 0; i < n - 1; i++) {
           if (arr[i] > arr[i + 1]) return false;
       }
       return true;
   }
   ```
   - **a) The function is correct.**
   - **b) The function should start from `i = 1` in the loop.**
   - **c) Change `i < n - 1` to `i < n`.**
   - **d) Change `if (arr[i] > arr[i + 1])` to `if (arr[i] >= arr[i + 1])`.**

   **Answer:** **a) The function is correct.**

---

### 4. What will be the output of the following code?
   ```cpp
   int arr[] = {5, 10, 15, 20};
   int *p = (arr + 1);
   std::cout << p[1] << " " << *(p - 1);
   ```
   - **a) 10 5**
   - **b) 15 5**
   - **c) 15 10**
   - **d) Compilation error**

   **Answer:** **b) 15 5**

---

### 5. How many bytes does the array `int arr[10];` occupy on a system with `sizeof(int) == 4`?
   - **a) 10**
   - **b) 20**
   - **c) 40**
   - **d) 80**

   **Answer:** **c) 40**

---

### 6. What does `int arr[] = {1, 2, 3}; int *ptr = arr + 3; std::cout << *(ptr - 1);` output?
   - **a) 3**
   - **b) 2**
   - **c) Undefined behavior**
   - **d) Compilation error**

   **Answer:** **a) 3**

---

### 7. Consider the following code:
   ```cpp
   int arr[5] = {1, 2, 3, 4, 5};
   int *ptr = arr + 1;
   std::cout << ptr[-1];
   ```
   What is printed?
   - **a) 1**
   - **b) 2**
   - **c) Undefined behavior**
   - **d) Compilation error**

   **Answer:** **a) 1**

---

### 8. Which statement best describes this code?
   ```cpp
   int arr[10];
   int *p = arr;
   std::cout << sizeof(arr) / sizeof(p);
   ```
   - **a) 1**
   - **b) 10**
   - **c) Undefined behavior**
   - **d) Depends on `sizeof(int)`**

   **Answer:** **a) 1**

---

### 9. What will be the output of `int arr[3] = {1, 2}; std::cout << arr[2];`?
   - **a) 1**
   - **b) 0**
   - **c) Garbage value**
   - **d) Compilation error**

   **Answer:** **b) 0**

---

### 10. Which of the following statements about arrays is correct?
   - **a) Array size can be changed at runtime.**
   - **b) Arrays are allocated in heap memory by default.**
   - **c) Array elements are contiguous in memory.**
   - **d) Arrays can store elements of different types.**

   **Answer:** **c) Array elements are contiguous in memory.**

### 11. What will the following code output?
   ```cpp
   int arr[] = {10, 20, 30, 40};
   int *ptr = arr;
   std::cout << *(ptr++) + *ptr;
   ```
   - **a) 30**
   - **b) 40**
   - **c) 50**
   - **d) Undefined behavior**

   **Answer:** **c) 50**

---

### 12. Which of the following correctly doubles the elements of an array `arr` of size `n`?
   ```cpp
   void doubleElements(int arr[], int n) {
       for (int i = 0; i < n; i++) {
           arr[i] *= 2;
       }
   }
   ```
   - **a) The function is correct.**
   - **b) Change `for (int i = 0; i < n; i++)` to `for (int i = 1; i <= n; i++)`.**
   - **c) Change `arr[i] *= 2` to `arr[i] = arr[i] + arr[i]`.**
   - **d) Replace `arr[i] *= 2` with `*(arr + i) *= 2`.**

   **Answer:** **a) The function is correct.**

---

### 13. Given `int arr[5] = {1, 2, 3, 4, 5};`, what will `std::cout << sizeof(arr) / sizeof(arr[0]);` print?
   - **a) 1**
   - **b) 5**
   - **c) 10**
   - **d) Undefined behavior**

   **Answer:** **b) 5**

---

### 14. Which statement about multidimensional arrays is correct in C++?
   - **a) Arrays can only be one-dimensional.**
   - **b) The total size of an `int arr[2][3];` is `3 * sizeof(int)`.**
   - **c) Each row of a 2D array can have a different number of columns.**
   - **d) `int arr[3][3] = {};` initializes all elements to 0.**

   **Answer:** **d) `int arr[3][3] = {};` initializes all elements to 0.**

---

### 15. Consider the code:
   ```cpp
   int arr[5] = {1, 2, 3, 4, 5};
   int *p = arr + 2;
   std::cout << *p + *(p + 2);
   ```
   What will it print?
   - **a) 3**
   - **b) 7**
   - **c) 8**
   - **d) Undefined behavior**

   **Answer:** **c) 8**

---

### 16. Given `int arr[10];`, which of the following statements is incorrect?
   - **a) `sizeof(arr) / sizeof(int)` gives the number of elements in `arr`.**
   - **b) `&arr[0] == arr` is true.**
   - **c) `*(arr + 10)` accesses the last element.**
   - **d) `arr[9]` accesses the last element.**

   **Answer:** **c) `*(arr + 10)` accesses the last element.**

---

### 17. What does `int arr[] = {1, 2, 3, 4}; std::cout << *(&arr[2] - 1);` output?
   - **a) 1**
   - **b) 2**
   - **c) 3**
   - **d) Undefined behavior**

   **Answer:** **b) 2**

---

### 18. What will be the output of the following code?
   ```cpp
   int arr[] = {1, 2, 3, 4, 5};
   int *p = arr;
   p += 2;
   std::cout << *p;
   ```
   - **a) 1**
   - **b) 2**
   - **c) 3**
   - **d) Undefined behavior**

   **Answer:** **c) 3**

---

### 19. Given the array `int arr[] = {10, 20, 30};`, what does `std::cout << *(arr + 1) + arr[0];` output?
   - **a) 10**
   - **b) 20**
   - **c) 30**
   - **d) 40**

   **Answer:** **d) 40**

---

### 20. Which of the following expressions will not cause an out-of-bounds access?
   ```cpp
   int arr[3] = {1, 2, 3};
   ```
   - **a) arr[3]**
   - **b) *(arr + 3)**
   - **c) arr[-1]**
   - **d) *(arr + 2)**

   **Answer:** **d) *(arr + 2)**

---

### 21. Which of the following will print the last element of an integer array `arr` with `n` elements?
   - **a) `std::cout << arr[n - 1];`**
   - **b) `std::cout << arr[n];`**
   - **c) `std::cout << arr[-1];`**
   - **d) `std::cout << *(arr + n);`**

   **Answer:** **a) `std::cout << arr[n - 1];`**

---

### 22. What does the following code print?
   ```cpp
   int arr[5] = {5, 10, 15, 20, 25};
   std::cout << arr[1] << *(arr + 1);
   ```
   - **a) 10 10**
   - **b) 5 5**
   - **c) 15 15**
   - **d) 10 5**

   **Answer:** **a) 10 10**

---

### 23. What does the following code print?
   ```cpp
   int arr[2][3] = {{1, 2, 3}, {4, 5, 6}};
   std::cout << arr[1][1];
   ```
   - **a) 3**
   - **b) 4**
   - **c) 5**
   - **d) Compilation error**

   **Answer:** **c) 5**

---

### 24. Given the array `int arr[] = {3, 6, 9, 12, 15};`, what does `std::cout << *(arr + 4);` print?
   - **a) 12**
   - **b) 15**
   - **c) 6**
   - **d) Undefined behavior**

   **Answer:** **b) 15**

---

### 25. What is the output of the following code?
   ```cpp
   int arr[5] = {1, 2, 3, 4, 5};
   int *p = arr;
   std::cout << *(p + 2) + *(p + 4);
   ```
   - **a) 6**
   - **b) 9**
   - **c) 7**
   - **d) 10**

   **Answer:** **d) 10**

---

### 26. Given `int arr[] = {2, 4, 6, 8};`, what is the result of `std::cout << arr[1] + arr[3];`?
   - **a) 2**
   - **b) 6**
   - **c) 12**
   - **d) 20**

   **Answer:** **c) 12**

---

### 27. What will be the output of this code snippet?
   ```cpp
   int arr[5] = {10, 20, 30, 40, 50};
   std::cout << arr[3 - 1];
   ```
   - **a) 10**
   - **b) 20**
   - **c) 30**
   - **d) 40**

   **Answer:** **c) 30**

---

### 28. Which of the following correctly swaps the first and last element of an integer array `arr` of size `n`?
   ```cpp
   void swapFirstLast(int arr[], int n) {
       int temp = arr[0];
       arr[0] = arr[n - 1];
       arr[n - 1] = temp;
   }
   ```
   - **a) The function is correct.**
   - **b) Change `arr[0]` to `*(arr + 0)`.**
   - **c) Replace `temp = arr[0];` with `temp = arr[n - 1];`.**
   - **d) Add `n > 1` condition check.**

   **Answer:** **a) The function is correct.**

---

### 29. What does `int arr[] = {4, 8, 12}; std::cout << arr[1];` output?
   - **a) 4**
   - **b) 8**
   - **c) 12**


   - **d) Compilation error**

   **Answer:** **b) 8**

---

### 30. What will `std::cout << sizeof(int[3][3]);` output on a system where `sizeof(int) == 4`?
   - **a) 12**
   - **b) 36**
   - **c) 24**
   - **d) Compilation error**

   **Answer:** **b) 36**

