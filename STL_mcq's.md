## STL: Vectors - Advanced-Level Questions

### 1. **MCQ**

**Q1**: Which of the following is true about the `std::vector` data structure?
- A) `std::vector` reserves exactly the required memory on initialization.
- B) `std::vector` has amortized `O(1)` complexity for push operations at the end.
- C) The `size()` and `capacity()` of a `std::vector` are always equal.
- D) `std::vector::shrink_to_fit()` is guaranteed to release all unused capacity.

**Answer**: **B** - The amortized complexity for appending elements at the end is `O(1)` due to capacity doubling.


### 2. **Code Debugging**

**Q2**: Find the bug in the following code that tries to erase all even numbers from a vector.

```cpp
std::vector<int> vec = {1, 2, 3, 4, 5, 6};
for (auto it = vec.begin(); it != vec.end(); ++it) {
    if (*it % 2 == 0) {
        vec.erase(it);
    }
}
```

**Answer**: The iterator becomes invalidated after an erase. Correct code:

```cpp
for (auto it = vec.begin(); it != vec.end(); ) {
    if (*it % 2 == 0) {
        it = vec.erase(it);
    } else {
        ++it;
    }
}
```


### 3. **True/False**

**Q3**: Resizing a `std::vector` using `resize()` increases the vector's `capacity` to match the `size` if the new size is larger than the current capacity.

**Answer**: **True**


### 4. **Code Debugging**

**Q4**: The following code intends to initialize a vector of size `10` with values `5`. What is the mistake?

```cpp
std::vector<int> vec(10, 5);
```

**Answer**: No mistake. This code is correct.


### 5. **MCQ**

**Q5**: What is the result of the following code?

```cpp
std::vector<int> vec = {1, 2, 3, 4, 5};
vec.insert(vec.begin() + 1, vec.begin(), vec.begin() + 3);
```

- A) `1, 2, 3, 4, 5`
- B) `1, 1, 2, 2, 3, 4, 5`
- C) `1, 1, 2, 3, 2, 3, 4, 5`
- D) `1, 1, 2, 1, 2, 3, 4, 5`

**Answer**: **B** - The vector becomes `1, 1, 2, 2, 3, 4, 5`.


### 6. **True/False**

**Q6**: The `clear()` function in `std::vector` sets the vector’s size to `0` but does not affect its capacity.

**Answer**: **True**


### 7. **MCQ**

**Q7**: Given the following code, what will be the output?

```cpp
std::vector<int> vec = {10, 20, 30};
vec.resize(5, 50);
for (auto v : vec) std::cout << v << " ";
```

- A) `10 20 30 50 50`
- B) `10 20 30 50 50 50`
- C) `10 20 30`
- D) Compilation Error

**Answer**: **A** - `10 20 30 50 50`.


### 8. **Code Debugging**

**Q8**: Spot the mistake if any in the code below:

```cpp
std::vector<int> vec(10);
vec.reserve(20);
```

**Answer**: The code is correct. `reserve()` only affects capacity, not size.


### 9. **True/False**

**Q9**: If `vec` is a `std::vector<int>`, calling `vec.data()` on an empty vector is undefined behavior.

**Answer**: **False** - `vec.data()` on an empty vector returns a `nullptr`, which is defined behavior.


### 10. **MCQ**

**Q10**: Which operation on a `std::vector` has the complexity of `O(n)` in the worst case?

- A) `push_back`
- B) `pop_back`
- C) `erase`
- D) `emplace_back`

**Answer**: **C** - `erase()` has a worst-case complexity of `O(n)` since it shifts elements.

---

Here’s the next set of questions on **Iterators** in STL, focusing on medium and hard levels.

---

## STL: Iterators - Advanced-Level Questions

### 1. **MCQ**

**Q1**: Given the following code, which output is correct?

```cpp
std::vector<int> vec = {1, 2, 3, 4, 5};
auto it = vec.begin();
std::advance(it, 3);
std::cout << *it;
```

- A) `2`
- B) `3`
- C) `4`
- D) Undefined behavior

**Answer**: **C** - `4`


### 2. **True/False**

**Q2**: Reverse iterators, when incremented, move backward through the container, effectively accessing the last element first.

**Answer**: **True**


### 3. **MCQ**

**Q3**: What will the following code output?

```cpp
std::vector<int> vec = {10, 20, 30, 40};
auto rit = vec.rbegin();
++rit;
std::cout << *rit;
```

- A) `10`
- B) `20`
- C) `30`
- D) `40`

**Answer**: **C** - `30`


### 4. **Code Debugging**

**Q4**: Identify the issue in the code below, which intends to print each element in reverse:

```cpp
std::vector<int> vec = {1, 2, 3, 4, 5};
for (auto it = vec.end(); it != vec.begin(); --it) {
    std::cout << *it << " ";
}
```

**Answer**: `vec.end()` points to one past the last element. Correct code:

```cpp
for (auto it = vec.end() - 1; it >= vec.begin(); --it) {
    std::cout << *it << " ";
}
```


### 5. **MCQ**

**Q5**: Which of the following iterators can be used only with containers supporting random access?

- A) Input iterator
- B) Bidirectional iterator
- C) Forward iterator
- D) Random access iterator

**Answer**: **D** - Random access iterators can only be used with containers that support direct element access.


### 6. **True/False**

**Q6**: `std::advance(it, n)` can be used with all iterator categories, but the complexity depends on the iterator type.

**Answer**: **True**


### 7. **Code Debugging**

**Q7**: What’s wrong with this code that intends to copy elements from one vector to another using iterators?

```cpp
std::vector<int> src = {1, 2, 3, 4};
std::vector<int> dest;
auto it = dest.begin();
std::copy(src.begin(), src.end(), it);
```

**Answer**: `dest` is empty, so `it` is invalid. Either `resize` or use `back_inserter`:

```cpp
std::copy(src.begin(), src.end(), std::back_inserter(dest));
```


### 8. **MCQ**

**Q8**: If `std::vector<int>::iterator it` is initialized to `vec.begin()`, which of the following is true?

- A) `std::advance(it, vec.size());` results in `it == vec.end()`
- B) `std::next(it, vec.size());` results in `*it == vec.back()`
- C) `std::advance(it, vec.size() - 1);` results in `it == vec.end()`
- D) `std::next(it, -vec.size());` is valid if `vec` is non-empty

**Answer**: **A** - Advancing by `vec.size()` leads to `vec.end()`.


### 9. **True/False**

**Q9**: `std::distance(it1, it2)` is `O(1)` if `it1` and `it2` are random access iterators.

**Answer**: **True**


### 10. **MCQ**

**Q10**: Which code snippet is correct for iterating over a `std::map<int, int>` using an iterator and printing key-value pairs?

- A)
  ```cpp
  for (auto it = map.begin(); it < map.end(); ++it)
      std::cout << it->first << " " << it->second;
  ```
- B)
  ```cpp
  for (auto it = map.begin(); it != map.end(); ++it)
      std::cout << it.first << " " << it.second;
  ```
- C)
  ```cpp
  for (auto it = map.begin(); it != map.end(); ++it)
      std::cout << it->first << " " << it->second;
  ```
- D)
  ```cpp
  for (auto it = map.begin(); it >= map.end(); --it)
      std::cout << it->first << " " << it->second;
  ```

**Answer**: **C**

---
Here’s the next set of questions on **Deque** in STL, focusing on advanced-level content.

---

## STL: Deque - Advanced-Level Questions

### 1. **MCQ**

**Q1**: Which of the following operations on a `std::deque` has the time complexity of `O(1)`?

- A) `push_front()`
- B) `push_back()`
- C) `pop_back()`
- D) All of the above

**Answer**: **D** - All of these operations are `O(1)`.


### 2. **True/False**

**Q2**: The `std::deque` container uses contiguous memory allocation, similar to `std::vector`.

**Answer**: **False** - `std::deque` does not use contiguous memory; it consists of multiple segments of memory.


### 3. **Code Debugging**

**Q3**: Identify the error in the following code snippet attempting to reverse a deque:

```cpp
std::deque<int> dq = {1, 2, 3, 4, 5};
std::reverse(dq.begin(), dq.end());
for (auto it = dq.begin(); it != dq.end(); ++it) {
    std::cout << *it << " ";
}
```

**Answer**: No error in the logic; the code is correct and will print `5 4 3 2 1`.


### 4. **MCQ**

**Q4**: Given the code below, what will be the output?

```cpp
std::deque<int> dq = {10, 20, 30};
dq.push_back(40);
dq.push_front(5);
std::cout << dq.at(1);
```

- A) `5`
- B) `10`
- C) `20`
- D) `30`

**Answer**: **B** - `10`


### 5. **True/False**

**Q5**: The `size()` method of a `std::deque` returns the number of elements currently stored in the container.

**Answer**: **True**


### 6. **Code Debugging**

**Q6**: Find the mistake in the following code, which attempts to remove all elements less than `3` from a deque:

```cpp
std::deque<int> dq = {1, 2, 3, 4, 5};
for (auto it = dq.begin(); it != dq.end(); ++it) {
    if (*it < 3) {
        dq.erase(it);
    }
}
```

**Answer**: The iterator is invalidated after an erase. Correct code:

```cpp
for (auto it = dq.begin(); it != dq.end(); ) {
    if (*it < 3) {
        it = dq.erase(it);
    } else {
        ++it;
    }
}
```


### 7. **MCQ**

**Q7**: What will the following code output?

```cpp
std::deque<int> dq = {1, 2, 3};
dq.emplace_front(0);
dq.emplace_back(4);
std::cout << dq.front() << " " << dq.back();
```

- A) `0 4`
- B) `1 3`
- C) `1 4`
- D) `0 3`

**Answer**: **A** - `0 4`


### 8. **True/False**

**Q8**: `std::deque` supports random access iterators, allowing for direct element access using the subscript operator.

**Answer**: **True**


### 9. **Code Debugging**

**Q9**: Identify the mistake in this code that attempts to access an out-of-bounds element:

```cpp
std::deque<int> dq = {1, 2, 3};
std::cout << dq[3];
```

**Answer**: This will result in undefined behavior as `dq[3]` is out of bounds. The correct index should be `dq[2]` for accessing the last element.


### 10. **MCQ**

**Q10**: Which of the following statements is false about `std::deque`?

- A) It allows fast insertions and deletions from both ends.
- B) It is more memory efficient than `std::vector`.
- C) It supports dynamic resizing.
- D) It can be used with the same algorithms as `std::vector`.

**Answer**: **B** - `std::deque` is generally less memory efficient than `std::vector` due to its non-contiguous storage structure.

---

Here’s the next set of questions on **Queue** in STL, focusing on advanced-level content.

---

## STL: Queue - Advanced-Level Questions

### 1. **MCQ**

**Q1**: Which of the following statements is true regarding `std::queue`?

- A) It allows random access to its elements.
- B) It allows insertion and deletion at both ends.
- C) It is implemented as a FIFO (First In First Out) data structure.
- D) It has a method `pop_front()`.

**Answer**: **C** - `std::queue` implements a FIFO data structure.


### 2. **True/False**

**Q2**: The `std::queue::size()` function has a time complexity of `O(1)`.

**Answer**: **True**


### 3. **Code Debugging**

**Q3**: Identify the error in the following code that attempts to access the front element of an empty queue:

```cpp
std::queue<int> q;
std::cout << q.front();
```

**Answer**: This code results in undefined behavior because `front()` cannot be called on an empty queue. You should check if the queue is empty before accessing the front:

```cpp
if (!q.empty()) {
    std::cout << q.front();
}
```


### 4. **MCQ**

**Q4**: What will be the output of the following code?

```cpp
std::queue<int> q;
q.push(10);
q.push(20);
q.pop();
q.push(30);
std::cout << q.front();
```

- A) `10`
- B) `20`
- C) `30`
- D) `Undefined behavior`

**Answer**: **B** - `20`


### 5. **True/False**

**Q5**: The `std::queue` container is implemented using a `std::deque` by default.

**Answer**: **True** - `std::queue` is typically implemented using `std::deque`, but it can also be implemented using other containers.


### 6. **Code Debugging**

**Q6**: What is wrong with the following code that attempts to create a queue from a vector?

```cpp
std::vector<int> vec = {1, 2, 3, 4};
std::queue<int> q(vec.begin(), vec.end());
```

**Answer**: This code is incorrect because `std::queue` does not have a constructor that accepts iterators. You can use a `std::deque` or a `std::list` to initialize the queue:

```cpp
std::queue<int> q(std::deque<int>(vec.begin(), vec.end()));
```


### 7. **MCQ**

**Q7**: Which of the following operations on `std::queue` has a time complexity of `O(n)`?

- A) `push()`
- B) `pop()`
- C) `front()`
- D) None of the above

**Answer**: **D** - All the mentioned operations have an average time complexity of `O(1)`.


### 8. **True/False**

**Q8**: You can use `std::queue` in a range-based for loop to iterate over its elements directly.

**Answer**: **False** - `std::queue` does not provide iterators for iteration.


### 9. **Code Debugging**

**Q9**: Identify the problem in this code attempting to clear a queue:

```cpp
std::queue<int> q;
q.push(1);
q.push(2);
q.push(3);
while (!q.empty()) {
    q.pop();
}
std::cout << q.front();
```

**Answer**: The code attempts to access `front()` after clearing the queue, resulting in undefined behavior. You should check if the queue is empty before accessing:

```cpp
if (!q.empty()) {
    std::cout << q.front();
}
```


### 10. **MCQ**

**Q10**: Which function can be used to check if a queue is empty?

- A) `is_empty()`
- B) `empty()`
- C) `size() == 0`
- D) Both B and C

**Answer**: **D** - Both `empty()` and checking `size() == 0` can be used to check if a queue is empty.

---

Here’s the next set of questions on **Priority Queue** in STL, focusing on advanced-level content.

---

## STL: Priority Queue - Advanced-Level Questions

### 1. **MCQ**

**Q1**: What is the underlying data structure used for implementing `std::priority_queue`?

- A) Binary Tree
- B) AVL Tree
- C) Heap
- D) Hash Table

**Answer**: **C** - `std::priority_queue` is implemented using a heap (specifically a binary heap).


### 2. **True/False**

**Q2**: The default behavior of `std::priority_queue` is to provide a max-heap.

**Answer**: **True** - By default, `std::priority_queue` behaves as a max-heap.


### 3. **Code Debugging**

**Q3**: Identify the error in the following code that tries to access the top element of an empty priority queue:

```cpp
std::priority_queue<int> pq;
std::cout << pq.top();
```

**Answer**: This will result in undefined behavior because `top()` cannot be called on an empty priority queue. You should check if the queue is empty before accessing:

```cpp
if (!pq.empty()) {
    std::cout << pq.top();
}
```


### 4. **MCQ**

**Q4**: What will be the output of the following code?

```cpp
std::priority_queue<int> pq;
pq.push(10);
pq.push(20);
pq.push(15);
pq.pop();
std::cout << pq.top();
```

- A) `10`
- B) `15`
- C) `20`
- D) `Undefined behavior`

**Answer**: **C** - `20`


### 5. **True/False**

**Q5**: You can change the order of elements in `std::priority_queue` by providing a custom comparator.

**Answer**: **True** - You can provide a custom comparator to change the ordering of elements.


### 6. **Code Debugging**

**Q6**: Find the mistake in the following code that attempts to create a priority queue from a vector:

```cpp
std::vector<int> vec = {10, 20, 15};
std::priority_queue<int> pq(vec.begin(), vec.end());
```

**Answer**: The code will not compile because `std::priority_queue` does not accept a range of iterators directly in the constructor. You need to use a different approach, such as copying elements into the queue:

```cpp
std::priority_queue<int> pq(vec.begin(), vec.end(), std::less<int>());
```


### 7. **MCQ**

**Q7**: Which of the following statements is false regarding `std::priority_queue`?

- A) It can store duplicate values.
- B) It allows direct access to any element in the container.
- C) The `top()` method gives you the largest element.
- D) It supports operations like `push()`, `pop()`, and `top()`.

**Answer**: **B** - `std::priority_queue` does not allow direct access to elements other than the top element.


### 8. **True/False**

**Q8**: `std::priority_queue` has a `size()` method that returns the number of elements currently in the priority queue.

**Answer**: **True**


### 9. **Code Debugging**

**Q9**: Identify the problem in this code snippet that tries to sort elements using a priority queue:

```cpp
std::priority_queue<int> pq;
pq.push(4);
pq.push(1);
pq.push(3);
while (!pq.empty()) {
    std::cout << pq.pop() << " ";
}
```

**Answer**: The method `pop()` should be `top()` when trying to access the top element before popping. The correct code is:

```cpp
while (!pq.empty()) {
    std::cout << pq.top() << " ";  // Use top() to access the largest element
    pq.pop();                        // Then pop to remove it
}
```


### 10. **MCQ**

**Q10**: What happens if you attempt to push an element into a full priority queue?

- A) It throws an exception.
- B) It discards the new element.
- C) It expands the queue's capacity.
- D) It results in undefined behavior.

**Answer**: **C** - `std::priority_queue` can dynamically grow to accommodate new elements.

---

Here’s the next set of questions on **Dictionaries** (i.e., `std::unordered_map` and `std::map`) in STL, focusing on advanced-level content.

---

## STL: Dictionaries - Advanced-Level Questions

### 1. **MCQ**

**Q1**: Which of the following is true about `std::unordered_map`?

- A) It maintains the order of elements based on the keys.
- B) It is implemented as a binary search tree.
- C) It provides average-case constant time complexity for lookups.
- D) It cannot store duplicate keys.

**Answer**: **C** - `std::unordered_map` provides average-case `O(1)` time complexity for lookups.


### 2. **True/False**

**Q2**: The `std::map` container allows duplicate keys.

**Answer**: **False** - `std::map` does not allow duplicate keys; each key must be unique.


### 3. **Code Debugging**

**Q3**: Identify the error in the following code that tries to access a value using a key not present in the `std::unordered_map`:

```cpp
std::unordered_map<std::string, int> umap;
umap["one"] = 1;
std::cout << umap.at("two");
```

**Answer**: This code will throw an `out_of_range` exception because the key "two" does not exist in the map. Use `find()` to check for existence before accessing:

```cpp
if (umap.find("two") != umap.end()) {
    std::cout << umap.at("two");
}
```


### 4. **MCQ**

**Q4**: What will be the output of the following code?

```cpp
std::map<int, std::string> m;
m[2] = "two";
m[1] = "one";
m[3] = "three";
std::cout << m[1] << " " << m[3];
```

- A) `one three`
- B) `three one`
- C) `two one`
- D) `one two`

**Answer**: **A** - `one three`


### 5. **True/False**

**Q5**: The `std::unordered_map` can be used with any data type as keys.

**Answer**: **False** - The keys must be hashable types, meaning they need to have a corresponding hash function.


### 6. **Code Debugging**

**Q6**: Find the mistake in this code attempting to iterate through an `std::map`:

```cpp
std::map<int, std::string> m = {{1, "one"}, {2, "two"}, {3, "three"}};
for (auto it = m.begin(); it != m.end(); it++) {
    std::cout << it.first << " " << it.second << std::endl;
}
```

**Answer**: The code is incorrect due to how the iterator is accessed. It should be `it->first` and `it->second`, not `it.first` and `it.second`. The correct code is:

```cpp
for (auto it = m.begin(); it != m.end(); it++) {
    std::cout << it->first << " " << it->second << std::endl;
}
```


### 7. **MCQ**

**Q7**: Which of the following functions can be used to remove an element from an `std::map`?

- A) `remove()`
- B) `erase()`
- C) `delete()`
- D) `clear()`

**Answer**: **B** - `erase()` is the function used to remove elements from an `std::map`.


### 8. **True/False**

**Q8**: The `find()` method of `std::unordered_map` returns an iterator to the element if found; otherwise, it returns the end iterator.

**Answer**: **True**


### 9. **Code Debugging**

**Q9**: Identify the problem in this code that attempts to insert elements into an `std::map`:

```cpp
std::map<std::string, int> wordCount;
wordCount["hello"]++;
std::cout << wordCount["hello"];
```

**Answer**: The code does not initialize the value for "hello" before incrementing. This will create an entry with a default value of `0` for "hello". The correct code should first initialize the key if needed:

```cpp
wordCount["hello"] = 0; // Optional, but good practice for clarity
wordCount["hello"]++;
std::cout << wordCount["hello"];
```


### 10. **MCQ**

**Q10**: What will be the result of the following code snippet?

```cpp
std::unordered_map<int, int> umap = {{1, 10}, {2, 20}, {3, 30}};
umap.erase(2);
std::cout << umap.size();
```

- A) `2`
- B) `3`
- C) `1`
- D) `Undefined behavior`

**Answer**: **A** - `2` (after erasing the element with key `2`).

---

Here’s the next set of questions on **Maps** (i.e., `std::multimap`) in STL, focusing on advanced-level content.

---

## STL: Maps (Multimap) - Advanced-Level Questions

### 1. **MCQ**

**Q1**: Which of the following statements is true about `std::multimap`?

- A) It allows duplicate keys.
- B) It maintains the order of elements based on the values.
- C) It provides constant time complexity for lookups.
- D) It cannot store more than one value for a single key.

**Answer**: **A** - `std::multimap` allows duplicate keys.


### 2. **True/False**

**Q2**: The elements in a `std::multimap` are stored in a sorted order based on the keys.

**Answer**: **True** - `std::multimap` maintains its elements in sorted order by key.


### 3. **Code Debugging**

**Q3**: Identify the error in the following code that tries to insert duplicate keys into a `std::multimap`:

```cpp
std::multimap<int, std::string> mmap;
mmap.insert({1, "one"});
mmap.insert({1, "uno"});
std::cout << mmap.size();
```

**Answer**: There is no error in the code; it correctly inserts duplicate keys into the multimap. The output will be `2` because it counts both entries.

### 4. **MCQ**

**Q4**: What will be the output of the following code?

```cpp
std::multimap<int, std::string> mmap;
mmap.insert({1, "one"});
mmap.insert({2, "two"});
mmap.insert({1, "uno"});
auto it = mmap.find(1);
std::cout << it->second << " ";
it++;
std::cout << it->second;
```

- A) `one uno`
- B) `uno one`
- C) `one one`
- D) `uno two`

**Answer**: **A** - `one uno`


### 5. **True/False**

**Q5**: The `std::multimap` provides an `erase()` function that can remove all entries with a specific key.

**Answer**: **True** - The `erase()` function can remove all entries associated with a specific key.


### 6. **Code Debugging**

**Q6**: Identify the mistake in this code that attempts to retrieve values associated with a specific key from a `std::multimap`:

```cpp
std::multimap<int, std::string> mmap = {{1, "one"}, {1, "uno"}, {2, "two"}};
auto it = mmap.equal_range(1);
while (it.first != it.second) {
    std::cout << it.first->second << " ";
    it.first++;
}
```

**Answer**: The code is correct; it retrieves all values for the key `1`. The output will be `one uno`. No changes are needed.


### 7. **MCQ**

**Q7**: Which of the following operations has a time complexity of `O(log n)` in a `std::multimap`?

- A) `insert()`
- B) `find()`
- C) `erase()`
- D) All of the above

**Answer**: **D** - All of the above operations have a time complexity of `O(log n)`.


### 8. **True/False**

**Q8**: You can use a `std::multimap` to store pairs of values where both keys and values are of different types.

**Answer**: **True** - A `std::multimap` can store pairs with different key and value types.


### 9. **Code Debugging**

**Q9**: Identify the problem in this code snippet trying to initialize a `std::multimap` with an array:

```cpp
std::multimap<int, std::string> mmap;
int arr[][2] = {{1, "one"}, {2, "two"}, {1, "uno"}};
for (auto &pair : arr) {
    mmap.insert({pair[0], pair[1]});
}
```

**Answer**: The code will not compile because `pair[1]` is of type `int`, but the second element in the multimap is `std::string`. You should change the array to store strings:

```cpp
std::pair<int, std::string> arr[] = {{1, "one"}, {2, "two"}, {1, "uno"}};
for (auto &pair : arr) {
    mmap.insert(pair);
}
```


### 10. **MCQ**

**Q10**: If you have the following multimap, what will be the output of `mmap.count(1)`?

```cpp
std::multimap<int, std::string> mmap = {{1, "one"}, {1, "uno"}, {2, "two"}};
```

- A) `1`
- B) `2`
- C) `3`
- D) `0`

**Answer**: **B** - `2`, because there are two entries with the key `1`.

---

Here’s the next set of questions on **Set** (i.e., `std::set` and `std::multiset`) in STL, focusing on advanced-level content.

---

## STL: Set - Advanced-Level Questions

### 1. **MCQ**

**Q1**: Which of the following is true about `std::set`?

- A) It allows duplicate elements.
- B) It maintains the order of elements based on a comparator.
- C) It provides average-case constant time complexity for insertions.
- D) It allows access to elements by index.

**Answer**: **B** - `std::set` maintains the order of elements based on a comparator.


### 2. **True/False**

**Q2**: The elements in a `std::set` are stored in a sorted order based on the keys.

**Answer**: **True** - `std::set` keeps its elements sorted.


### 3. **Code Debugging**

**Q3**: Identify the error in the following code that tries to insert duplicate elements into a `std::set`:

```cpp
std::set<int> s;
s.insert(1);
s.insert(1);
std::cout << s.size();
```

**Answer**: There is no error in the code; however, the size of the set will be `1` since duplicates are not allowed. The output will be `1`.


### 4. **MCQ**

**Q4**: What will be the output of the following code?

```cpp
std::set<int> s = {2, 1, 3};
s.insert(2);
s.erase(1);
std::cout << *s.begin();
```

- A) `1`
- B) `2`
- C) `3`
- D) `Undefined behavior`

**Answer**: **B** - `2`, because `1` is erased, and `2` is the smallest remaining element.


### 5. **True/False**

**Q5**: The `std::multiset` allows duplicate elements.

**Answer**: **True** - `std::multiset` can store multiple instances of the same element.


### 6. **Code Debugging**

**Q6**: Identify the mistake in this code that attempts to find an element in a `std::set`:

```cpp
std::set<int> s = {1, 2, 3};
auto it = s.find(4);
std::cout << *it;
```

**Answer**: The code will result in undefined behavior since `find()` will return `s.end()` when the element is not found. You should check if the iterator is equal to `s.end()` before dereferencing:

```cpp
if (it != s.end()) {
    std::cout << *it;
} else {
    std::cout << "Element not found";
}
```


### 7. **MCQ**

**Q7**: Which of the following functions can be used to remove an element from a `std::set`?

- A) `remove()`
- B) `delete()`
- C) `erase()`
- D) `clear()`

**Answer**: **C** - `erase()` is the function used to remove elements from a `std::set`.


### 8. **True/False**

**Q8**: You can use a `std::set` to store pairs of values where both keys and values are of different types.

**Answer**: **False** - A `std::set` requires that all elements be of the same type.


### 9. **Code Debugging**

**Q9**: Identify the problem in this code snippet trying to initialize a `std::multiset` with an array:

```cpp
std::multiset<int> ms;
int arr[] = {1, 2, 1};
for (auto &el : arr) {
    ms.insert(el);
}
```

**Answer**: The code is correct; it initializes a multiset with duplicate elements. The output size will be `3` because `1` appears twice.


### 10. **MCQ**

**Q10**: If you have the following multiset, what will be the output of `ms.count(1)`?

```cpp
std::multiset<int> ms = {1, 2, 1, 3};
```

- A) `1`
- B) `2`
- C) `3`
- D) `0`

**Answer**: **B** - `2`, because there are two instances of the element `1`.

---

Here’s the next set of questions on **Algorithms** in STL, focusing on advanced-level content.

---

## STL: Algorithms - Advanced-Level Questions

### 1. **MCQ**

**Q1**: Which of the following algorithms can be used to sort a range in a `std::vector`?

- A) `std::find()`
- B) `std::sort()`
- C) `std::reverse()`
- D) `std::accumulate()`

**Answer**: **B** - `std::sort()` can be used to sort a range in a `std::vector`.


### 2. **True/False**

**Q2**: The `std::binary_search()` algorithm requires a sorted range to function correctly.

**Answer**: **True** - `std::binary_search()` only works on sorted ranges.


### 3. **Code Debugging**

**Q3**: Identify the error in the following code that attempts to find the minimum element in a vector:

```cpp
std::vector<int> v = {5, 2, 3, 1, 4};
auto min = std::min_element(v);
std::cout << *min;
```

**Answer**: The code is incorrect because `std::min_element()` requires two parameters: the beginning and the end of the range. The correct usage is:

```cpp
auto min = std::min_element(v.begin(), v.end());
std::cout << *min;
```


### 4. **MCQ**

**Q4**: What is the time complexity of the `std::lower_bound()` function?

- A) `O(n)`
- B) `O(log n)`
- C) `O(n log n)`
- D) `O(1)`

**Answer**: **B** - `std::lower_bound()` has a time complexity of `O(log n)`.


### 5. **True/False**

**Q5**: The `std::shuffle()` algorithm randomizes the order of elements in a range.

**Answer**: **True** - `std::shuffle()` randomly rearranges the elements in a specified range.


### 6. **Code Debugging**

**Q6**: Identify the problem in this code snippet that attempts to use `std::accumulate()`:

```cpp
std::vector<int> v = {1, 2, 3, 4};
int sum = std::accumulate(v.begin(), v.end());
std::cout << sum;
```

**Answer**: The code is incorrect because `std::accumulate()` requires a second parameter for the initial value. The correct code should be:

```cpp
int sum = std::accumulate(v.begin(), v.end(), 0);
std::cout << sum;
```


### 7. **MCQ**

**Q7**: Which algorithm is used to count the number of elements in a range that satisfy a specific condition?

- A) `std::count_if()`
- B) `std::find_if()`
- C) `std::for_each()`
- D) `std::transform()`

**Answer**: **A** - `std::count_if()` counts the elements satisfying a given condition.


### 8. **True/False**

**Q8**: The `std::unique()` algorithm can remove duplicate elements from a sorted range.

**Answer**: **False** - `std::unique()` removes duplicates only if they are consecutive; it requires the range to be sorted before usage.


### 9. **Code Debugging**

**Q9**: Identify the mistake in this code that tries to reverse a vector:

```cpp
std::vector<int> v = {1, 2, 3, 4};
std::reverse(v.begin());
std::cout << v[0];
```

**Answer**: The code is incorrect because `std::reverse()` requires two iterators to define the range to reverse. The correct usage is:

```cpp
std::reverse(v.begin(), v.end());
std::cout << v[0]; // Now it will correctly print the first element after reversing.
```


### 10. **MCQ**

**Q10**: What will be the result of the following code snippet?

```cpp
std::vector<int> v = {3, 1, 4, 1, 5};
std::sort(v.begin(), v.end());
std::cout << v[1];
```

- A) `1`
- B) `3`
- C) `4`
- D) `5`

**Answer**: **A** - `1`, as the vector will be sorted to `{1, 1, 3, 4, 5}`.

---

