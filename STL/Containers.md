![image](https://github.com/user-attachments/assets/ff7760bf-f0ea-44ac-960a-0d06ca0efbf5)
# Pairs in C++

## Definition
A **pair** is a simple container in the C++ Standard Template Library (STL) that stores two heterogeneous values as a single unit. It is defined in the `<utility>` header and can be used to group two related values.

![image](https://github.com/user-attachments/assets/6dad98e0-fe31-423e-abcb-8cb37ba0f1fb)


## Syntax
```cpp
#include <utility>

std::pair<Type1, Type2> pairName;
```

## Characteristics
- Pairs can hold values of different types.
- The types of the values can be specified as template parameters.
- Pairs support comparison operators such as `==`, `!=`, `<`, `>`, etc.

## Example Usage

### 1. Creating a Pair
```cpp
#include <iostream>
#include <utility>

int main() {
    std::pair<int, std::string> myPair(1, "Apple");
    std::cout << "First: " << myPair.first << ", Second: " << myPair.second << std::endl;
    return 0;
}
```

### 2. Returning Multiple Values from a Function
```cpp
#include <iostream>
#include <utility>

std::pair<int, int> getCoordinates() {
    return std::make_pair(10, 20);
}

int main() {
    std::pair<int, int> coords = getCoordinates();
    std::cout << "X: " << coords.first << ", Y: " << coords.second << std::endl;
    return 0;
}
```

### 3. Using Pairs with STL Containers
```cpp
#include <iostream>
#include <vector>
#include <utility>

int main() {
    std::vector<std::pair<int, std::string>> fruitList;
    fruitList.push_back(std::make_pair(1, "Apple"));
    fruitList.push_back(std::make_pair(2, "Banana"));

    for (const auto& fruit : fruitList) {
        std::cout << "ID: " << fruit.first << ", Name: " << fruit.second << std::endl;
    }
    return 0;
}
```

### 4. Comparing Pairs
```cpp
#include <iostream>
#include <utility>

int main() {
    std::pair<int, int> pair1(1, 2);
    std::pair<int, int> pair2(1, 3);

    if (pair1 < pair2) {
        std::cout << "pair1 is less than pair2" << std::endl;
    } else {
        std::cout << "pair1 is not less than pair2" << std::endl;
    }
    return 0;
}
```

# 2. Vectors : 

# Vectors in C++

## Definition
A **vector** is a sequence container in the C++ Standard Template Library (STL) that represents a dynamic array. It can grow and shrink in size, allowing for flexible management of data.

## Characteristics
- Vectors store elements in a contiguous memory location.
- They provide random access to elements using an index.
- Vectors automatically manage memory allocation and deallocation.

## Syntax
```cpp
#include <vector>

std::vector<Type> vectorName;
```

## Commonly Used Vector Functions

### 1. Element Access
- `at(index)`: Accesses the element at the specified index with bounds checking.
- `operator[]`: Accesses the element at the specified index without bounds checking.
- `front()`: Returns a reference to the first element.
- `back()`: Returns a reference to the last element.
- `data()`: Returns a pointer to the underlying array.

### 2. Capacity
- `size()`: Returns the number of elements in the vector.
- `capacity()`: Returns the number of elements that the vector can hold before needing to allocate more memory.
- `empty()`: Checks if the vector is empty.
- `reserve(size)`: Requests to reserve at least the specified number of elements.
- `shrink_to_fit()`: Reduces the capacity to fit the current size.

### 3. Modifiers
- `push_back(value)`: Adds an element to the end of the vector.
- `pop_back()`: Removes the last element.
- `insert(position, value)`: Inserts an element at the specified position.
- `erase(position)`: Removes the element at the specified position.
- `clear()`: Removes all elements from the vector.
- `assign(count, value)`: Assigns values to the vector.

### 4. Algorithms
- `sort()`: Sorts the elements of the vector.
- `reverse()`: Reverses the order of the elements.

## Example Usage

### 1. Creating and Using a Vector
```cpp
#include <iostream>
#include <vector>

int main() {
    std::vector<int> myVector;

    // Adding elements
    myVector.push_back(10);
    myVector.push_back(20);
    myVector.push_back(30);

    // Accessing elements
    for (size_t i = 0; i < myVector.size(); ++i) {
        std::cout << "Element at index " << i << ": " << myVector[i] << std::endl;
    }
    return 0;
}
```

### 2. Using `sort()` Function
```cpp
#include <iostream>
#include <vector>
#include <algorithm> // for sort

int main() {
    std::vector<int> myVector = {3, 1, 4, 1, 5, 9};

    // Sorting the vector
    std::sort(myVector.begin(), myVector.end());

    // Displaying sorted elements
    for (const auto& elem : myVector) {
        std::cout << elem << " ";
    }
    std::cout << std::endl;

    return 0;
}
```

### 3. Inserting and Erasing Elements
```cpp
#include <iostream>
#include <vector>

int main() {
    std::vector<int> myVector = {10, 20, 30};

    // Inserting an element
    myVector.insert(myVector.begin() + 1, 15); // Insert 15 at index 1

    // Erasing an element
    myVector.erase(myVector.begin()); // Remove the first element

    // Displaying elements
    for (const auto& elem : myVector) {
        std::cout << elem << " ";
    }
    std::cout << std::endl;

    return 0;
}
```

### 4. Using `clear()` and `empty()`
```cpp
#include <iostream>
#include <vector>

int main() {
    std::vector<int> myVector = {1, 2, 3};

    // Clear the vector
    myVector.clear();

    // Check if the vector is empty
    if (myVector.empty()) {
        std::cout << "The vector is empty." << std::endl;
    }

    return 0;
}
```
