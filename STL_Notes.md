# STL (Standard Template Library)

The Standard Template Library (STL) in C++ is a powerful set of template classes designed to manage and manipulate collections of data. The STL includes four primary components:

1. **Containers**: Structures that store data.
2. **Iterators**: Objects that point to elements within containers.
3. **Algorithms**: Functions that perform operations on containers.
4. **Functions**: Functional components like function pointers and functors.

---

## 1. Vector

A `vector` is a dynamic array that can change in size, allowing for efficient random access to elements.

### Example:
```cpp
#include <vector>
std::vector<int> vec = {1, 2, 3, 4};
vec.push_back(5);  // Adds an element at the end
```

![WhatsApp Image 2024-10-28 at 03 15 32_064dd012](https://github.com/user-attachments/assets/714d32ac-6d40-4610-9b16-67a26459373d)

---

## 2. Iterators

Iterators are objects that act as pointers, used to traverse through containers such as vectors, lists, and maps.

### Example:
```cpp
std::vector<int>::iterator it;
for (it = vec.begin(); it != vec.end(); ++it) {
    std::cout << *it << " ";
}
```

![WhatsApp Image 2024-10-28 at 03 15 44_a71456d0](https://github.com/user-attachments/assets/84bfc4bc-caae-42a7-8e03-c3a5b0cf00e3)

---

## 3. Deque

A `deque` (double-ended queue) allows insertion and deletion at both the front and the back.

### Example:
```cpp
#include <deque>
std::deque<int> deq = {1, 2, 3};
deq.push_front(0);  // Inserts at the front
deq.push_back(4);   // Inserts at the back
```

![WhatsApp Image 2024-10-28 at 03 15 53_42d26457](https://github.com/user-attachments/assets/3a982139-0155-4e89-abf1-834b5546bd24)

---

## 4. Queue

A `queue` is a first-in-first-out (FIFO) data structure, where elements are added at the back and removed from the front.

### Example:
```cpp
#include <queue>
std::queue<int> q;
q.push(1);
q.pop();  // Removes the front element
```

![WhatsApp Image 2024-10-28 at 03 16 07_747567c4](https://github.com/user-attachments/assets/a4d96816-8d6d-4833-b8b0-23a1c97dae76)

---

## 5. Priority Queue

A `priority_queue` is a special type of queue in which elements are ordered based on their priority, with the largest element at the front by default.

### Example:
```cpp
#include <queue>
std::priority_queue<int> pq;
pq.push(10);
pq.push(5);
pq.push(20);  // 20 will be at the front as it has the highest priority
```

![WhatsApp Image 2024-10-28 at 03 16 23_36d22e2a](https://github.com/user-attachments/assets/ff643639-312f-42fa-be05-bedeb6269a51)

---

## 6. Dictionaries

Dictionaries in C++ can be implemented using maps, which store key-value pairs.

---

## 7. Maps

`Map` is an associative container that stores elements in a key-value pair format, with unique keys and ordered entries.

### Example:
```cpp
#include <map>
std::map<int, std::string> mp;
mp[1] = "One";
mp[2] = "Two";
```

![WhatsApp Image 2024-10-28 at 03 16 35_76ae9bf9](https://github.com/user-attachments/assets/0859f161-e906-45ae-b86d-a485559e2061)

---

## 8. Multi Maps

A `multimap` allows multiple values for a single key.

### Example:
```cpp
#include <map>
std::multimap<int, std::string> mmp;
mmp.insert({1, "One"});
mmp.insert({1, "Another One"});
```

![WhatsApp Image 2024-10-28 at 03 16 48_28834254](https://github.com/user-attachments/assets/b2d89b6f-c18a-4b90-bd2e-df860312046b)

---

## 9. Set

A `set` is a collection of unique elements, where elements are automatically ordered.

### Example:
```cpp
#include <set>
std::set<int> s;
s.insert(1);
s.insert(2);
```

![WhatsApp Image 2024-10-28 at 03 17 01_026eac37](https://github.com/user-attachments/assets/81c0e2d7-e23f-46a7-9e90-7602a70205a6)

---

## 10. Algorithms

The STL provides various algorithms to perform operations like sorting, searching, and manipulating containers.

### Example:
```cpp
#include <algorithm>
std::vector<int> vec = {4, 2, 3, 1};
std::sort(vec.begin(), vec.end());  // Sorts the vector
```

![WhatsApp Image 2024-10-28 at 03 17 17_6dd71a85](https://github.com/user-attachments/assets/8f4e298f-1a37-445a-ad35-adaacb45e3fc)
```

