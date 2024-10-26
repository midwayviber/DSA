
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


