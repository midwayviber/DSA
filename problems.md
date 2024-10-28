### 1. **Two Sum (Brute-force)**

**Problem**: Given an array of integers, find two numbers that add up to a specific target.

**Brute-force Code**:
```cpp
#include <iostream>
#include <vector>

std::vector<int> twoSum(std::vector<int>& nums, int target) {
    for (int i = 0; i < nums.size(); ++i) {
        for (int j = i + 1; j < nums.size(); ++j) {
            if (nums[i] + nums[j] == target) return {i, j};
        }
    }
    return {}; // No solution found
}

int main() {
    std::vector<int> nums = {2, 7, 11, 15};
    int target = 9;
    std::vector<int> result = twoSum(nums, target);
    if (!result.empty()) {
        std::cout << "Indices: " << result[0] << ", " << result[1] << std::endl;
    } else {
        std::cout << "No solution found." << std::endl;
    }
    return 0;
}
```

---

### 2. **Maximum Sum Subarray (Brute-force)**

**Problem**: Find the contiguous subarray within an array with the largest sum.

**Brute-force Code**:
```cpp
#include <iostream>
#include <vector>
#include <climits>

int maxSubArray(std::vector<int>& nums) {
    int maxSum = INT_MIN;
    for (int i = 0; i < nums.size(); ++i) {
        int currentSum = 0;
        for (int j = i; j < nums.size(); ++j) {
            currentSum += nums[j];
            maxSum = std::max(maxSum, currentSum);
        }
    }
    return maxSum;
}

int main() {
    std::vector<int> nums = {-2, 1, -3, 4, -1, 2, 1, -5, 4};
    std::cout << "Maximum Sum Subarray: " << maxSubArray(nums) << std::endl;
    return 0;
}
```

---

### 3. **Frequency of Characters in a String (Brute-force)**

**Problem**: Count the occurrences of each character in a string.

**Brute-force Code**:
```cpp
#include <iostream>
#include <string>

void charFrequency(std::string s) {
    for (char c = 'a'; c <= 'z'; ++c) {
        int count = 0;
        for (char ch : s) {
            if (ch == c) count++;
        }
        if (count > 0) std::cout << c << ": " << count << std::endl;
    }
}

int main() {
    std::string str = "hello";
    charFrequency(str);
    return 0;
}
```

---

### 4. **Longest Substring Without Repeating Characters (Brute-force)**

**Problem**: Find the length of the longest substring without repeating characters.

**Brute-force Code**:
```cpp
#include <iostream>
#include <string>
#include <unordered_set>

int lengthOfLongestSubstring(std::string s) {
    int maxLength = 0;
    for (int i = 0; i < s.size(); ++i) {
        std::unordered_set<char> uniqueChars;
        for (int j = i; j < s.size(); ++j) {
            if (uniqueChars.count(s[j])) break;
            uniqueChars.insert(s[j]);
            maxLength = std::max(maxLength, j - i + 1);
        }
    }
    return maxLength;
}

int main() {
    std::string str = "abcabcbb";
    std::cout << "Length of Longest Substring Without Repeating Characters: " 
              << lengthOfLongestSubstring(str) << std::endl;
    return 0;
}
```

---

### 5. **Longest Palindromic Substring (Brute-force)**

**Problem**: Find the longest substring that is a palindrome.

**Brute-force Code**:
```cpp
#include <iostream>
#include <string>

bool isPalindrome(const std::string& s, int start, int end) {
    while (start < end) {
        if (s[start++] != s[end--]) return false;
    }
    return true;
}

std::string longestPalindrome(std::string s) {
    std::string longest;
    for (int i = 0; i < s.size(); ++i) {
        for (int j = i; j < s.size(); ++j) {
            if (isPalindrome(s, i, j) && (j - i + 1) > longest.size()) {
                longest = s.substr(i, j - i + 1);
            }
        }
    }
    return longest;
}

int main() {
    std::string str = "babad";
    std::cout << "Longest Palindromic Substring: " << longestPalindrome(str) << std::endl;
    return 0;
}
```

---

### 6. **Subarray with Given Sum (Brute-force)**

**Problem**: Find if there’s a subarray with a given sum.

**Brute-force Code**:
```cpp
#include <iostream>
#include <vector>

bool subarraySum(std::vector<int>& nums, int target) {
    for (int i = 0; i < nums.size(); ++i) {
        int currentSum = 0;
        for (int j = i; j < nums.size(); ++j) {
            currentSum += nums[j];
            if (currentSum == target) return true;
        }
    }
    return false;
}

int main() {
    std::vector<int> nums = {1, 2, 3, 7, 5};
    int target = 12;
    std::cout << (subarraySum(nums, target) ? "Found" : "Not found") << std::endl;
    return 0;
}
```

---

### 7. **Reverse Words in a String (Brute-force)**

**Problem**: Reverse the order of words in a given string.

**Brute-force Code**:
```cpp
#include <iostream>
#include <string>
#include <vector>
#include <sstream>

std::string reverseWords(std::string s) {
    std::vector<std::string> words;
    std::stringstream ss(s);
    std::string word;
    while (ss >> word) {
        words.push_back(word);
    }
    
    std::string reversed;
    for (int i = words.size() - 1; i >= 0; --i) {
        reversed += words[i] + (i > 0 ? " " : "");
    }
    return reversed;
}

int main() {
    std::string str = "hello world";
    std::cout << "Reversed Words: " << reverseWords(str) << std::endl;
    return 0;
}
```

---

### 8. **Longest Common Prefix (Brute-force)**

**Problem**: Find the longest common prefix in an array of strings.

**Brute-force Code**:
```cpp
#include <iostream>
#include <vector>
#include <string>

std::string longestCommonPrefix(std::vector<std::string>& strs) {
    if (strs.empty()) return "";
    std::string prefix = strs[0];
    for (int i = 1; i < strs.size(); ++i) {
        while (strs[i].find(prefix) != 0) {
            prefix = prefix.substr(0, prefix.size() - 1);
            if (prefix.empty()) return "";
        }
    }
    return prefix;
}

int main() {
    std::vector<std::string> strs = {"flower", "flow", "flight"};
    std::cout << "Longest Common Prefix: " << longestCommonPrefix(strs) << std::endl;
    return 0;
}
```

### 1. **Find All Unique Pairs with Given Sum**

```cpp
#include <vector>
#include <set>
#include <algorithm>

std::vector<std::pair<int, int>> findPairsWithSum(const std::vector<int>& nums, int target) {
    std::vector<std::pair<int, int>> pairs;
    std::set<std::pair<int, int>> uniquePairs;

    for (int i = 0; i < nums.size(); ++i) {
        for (int j = i + 1; j < nums.size(); ++j) {
            if (nums[i] + nums[j] == target) {
                int a = std::min(nums[i], nums[j]);
                int b = std::max(nums[i], nums[j]);
                uniquePairs.insert({a, b});
            }
        }
    }

    for (auto& p : uniquePairs) {
        pairs.push_back(p);
    }

    return pairs;
}
```

---

### 2. **All Subarrays of an Array**

```cpp
#include <vector>

std::vector<std::vector<int>> getAllSubarrays(const std::vector<int>& nums) {
    std::vector<std::vector<int>> subarrays;
    for (int i = 0; i < nums.size(); ++i) {
        std::vector<int> subarray;
        for (int j = i; j < nums.size(); ++j) {
            subarray.push_back(nums[j]);
            subarrays.push_back(subarray);
        }
    }
    return subarrays;
}
```

---

### 3. **Count Distinct Elements in Every Subarray of Size `k`**

```cpp
#include <vector>
#include <unordered_set>

std::vector<int> countDistinctInSubarrays(const std::vector<int>& nums, int k) {
    std::vector<int> distinctCounts;
    for (int i = 0; i <= nums.size() - k; ++i) {
        std::unordered_set<int> uniqueElements(nums.begin() + i, nums.begin() + i + k);
        distinctCounts.push_back(uniqueElements.size());
    }
    return distinctCounts;
}
```

---

### 4. **Generate All Permutations of a String**

```cpp
#include <string>
#include <vector>
#include <algorithm>

std::vector<std::string> getAllPermutations(std::string s) {
    std::vector<std::string> permutations;
    std::sort(s.begin(), s.end());
    do {
        permutations.push_back(s);
    } while (std::next_permutation(s.begin(), s.end()));
    return permutations;
}
```

---

### 5. **Find Longest Subarray with Given Sum**

```cpp
#include <vector>

int longestSubarrayWithSum(const std::vector<int>& nums, int target) {
    int maxLength = 0;
    for (int i = 0; i < nums.size(); ++i) {
        int currentSum = 0;
        for (int j = i; j < nums.size(); ++j) {
            currentSum += nums[j];
            if (currentSum == target) {
                maxLength = std::max(maxLength, j - i + 1);
            }
        }
    }
    return maxLength;
}
```

---

### 6. **Count Inversions in an Array**

**Inversion**: A pair `(i, j)` is an inversion if `i < j` and `nums[i] > nums[j]`.

```cpp
#include <vector>

int countInversions(const std::vector<int>& nums) {
    int inversionCount = 0;
    for (int i = 0; i < nums.size(); ++i) {
        for (int j = i + 1; j < nums.size(); ++j) {
            if (nums[i] > nums[j]) {
                inversionCount++;
            }
        }
    }
    return inversionCount;
}
```

---

### 7. **Count Subarrays with Product Less Than `k`**

```cpp
#include <vector>

int countSubarraysWithProductLessThanK(const std::vector<int>& nums, int k) {
    int count = 0;
    for (int i = 0; i < nums.size(); ++i) {
        int product = 1;
        for (int j = i; j < nums.size(); ++j) {
            product *= nums[j];
            if (product < k) {
                count++;
            } else {
                break;
            }
        }
    }
    return count;
}
```

### 8. **Find First Non-Repeating Character in a String**

```cpp
#include <string>
#include <unordered_map>

char firstNonRepeatingCharacter(const std::string& str) {
    for (int i = 0; i < str.size(); ++i) {
        bool isUnique = true;
        for (int j = 0; j < str.size(); ++j) {
            if (i != j && str[i] == str[j]) {
                isUnique = false;
                break;
            }
        }
        if (isUnique) return str[i];
    }
    return '\0';  // Returns null character if no non-repeating character is found
}
```

---

### 9. **Count Palindromic Substrings in a String**

```cpp
#include <string>

bool isPalindrome(const std::string& str, int start, int end) {
    while (start < end) {
        if (str[start++] != str[end--]) return false;
    }
    return true;
}

int countPalindromicSubstrings(const std::string& str) {
    int count = 0;
    for (int i = 0; i < str.size(); ++i) {
        for (int j = i; j < str.size(); ++j) {
            if (isPalindrome(str, i, j)) {
                count++;
            }
        }
    }
    return count;
}
```

---

### 10. **Find Longest Common Prefix among an Array of Strings**

```cpp
#include <vector>
#include <string>

std::string longestCommonPrefix(const std::vector<std::string>& strs) {
    if (strs.empty()) return "";
    std::string prefix = strs[0];
    for (int i = 1; i < strs.size(); ++i) {
        int j = 0;
        while (j < prefix.size() && j < strs[i].size() && prefix[j] == strs[i][j]) {
            j++;
        }
        prefix = prefix.substr(0, j);
        if (prefix.empty()) break;
    }
    return prefix;
}
```

---

### 11. **Find Maximum Product Subarray**

```cpp
#include <vector>

int maxProductSubarray(const std::vector<int>& nums) {
    int maxProduct = nums[0];
    for (int i = 0; i < nums.size(); ++i) {
        int currentProduct = 1;
        for (int j = i; j < nums.size(); ++j) {
            currentProduct *= nums[j];
            maxProduct = std::max(maxProduct, currentProduct);
        }
    }
    return maxProduct;
}
```

---

### 12. **Generate All Subsequences of a String**

```cpp
#include <string>
#include <vector>

void generateSubsequences(const std::string& str, int index, std::string current, std::vector<std::string>& subsequences) {
    if (index == str.size()) {
        if (!current.empty()) subsequences.push_back(current);
        return;
    }
    generateSubsequences(str, index + 1, current + str[index], subsequences);
    generateSubsequences(str, index + 1, current, subsequences);
}

std::vector<std::string> getAllSubsequences(const std::string& str) {
    std::vector<std::string> subsequences;
    generateSubsequences(str, 0, "", subsequences);
    return subsequences;
}
```

---

### 13. **Rotate an Array by `k` Positions (Left Rotation)**

```cpp
#include <vector>

std::vector<int> rotateArrayLeft(const std::vector<int>& nums, int k) {
    int n = nums.size();
    std::vector<int> rotatedArray(n);
    for (int i = 0; i < n; ++i) {
        rotatedArray[(i + n - k) % n] = nums[i];
    }
    return rotatedArray;
}
```

---

### 14. **Find All Pairs in an Array with a Given Difference**

```cpp
#include <vector>
#include <utility>
#include <cmath>

std::vector<std::pair<int, int>> findPairsWithDifference(const std::vector<int>& nums, int diff) {
    std::vector<std::pair<int, int>> pairs;
    for (int i = 0; i < nums.size(); ++i) {
        for (int j = i + 1; j < nums.size(); ++j) {
            if (std::abs(nums[i] - nums[j]) == diff) {
                pairs.emplace_back(nums[i], nums[j]);
            }
        }
    }
    return pairs;
}
```

---

### 15. **Find the Largest Sum Contiguous Subarray**

```cpp
#include <vector>
#include <algorithm>

int maxSumSubarray(const std::vector<int>& nums) {
    int maxSum = nums[0];
    for (int i = 0; i < nums.size(); ++i) {
        int currentSum = 0;
        for (int j = i; j < nums.size(); ++j) {
            currentSum += nums[j];
            maxSum = std::max(maxSum, currentSum);
        }
    }
    return maxSum;
}
```
