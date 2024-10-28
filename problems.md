# Advanced C++ Coding Test Preparation

## 1. Two Sum
**Problem**: Given an array of integers, find two numbers that add up to a specific target.

**Code**:
```cpp
vector<int> twoSum(vector<int>& nums, int target) {
    for (int i = 0; i < nums.size(); ++i) {
        for (int j = i + 1; j < nums.size(); ++j) {
            if (nums[i] + nums[j] == target) return {i, j};
        }
    }
    return {};
}
```

## 2. Maximum Sum Subarray (Kadane's Algorithm)
**Problem**: Find the contiguous subarray with the largest sum.

**Code**:
```cpp
int maxSubArray(vector<int>& nums) {
    int maxSum = nums[0], currentSum = nums[0];
    for (int i = 1; i < nums.size(); ++i) {
        currentSum = max(nums[i], currentSum + nums[i]);
        maxSum = max(maxSum, currentSum);
    }
    return maxSum;
}
```

## 3. Frequency of Characters in a String
**Problem**: Count the occurrences of each character in a string.

**Code**:
```cpp
vector<int> charFrequency(string s) {
    vector<int> freq(256, 0);
    for (char c : s) freq[c]++;
    return freq;
}
```

## 4. Longest Substring Without Repeating Characters
**Problem**: Find the length of the longest substring without repeating characters.

**Code**:
```cpp
int lengthOfLongestSubstring(string s) {
    int maxLength = 0;
    unordered_map<char, int> seen;
    for (int start = 0, end = 0; end < s.size(); ++end) {
        if (seen.count(s[end])) start = max(seen[s[end]] + 1, start);
        seen[s[end]] = end;
        maxLength = max(maxLength, end - start + 1);
    }
    return maxLength;
}
```

## 5. Longest Palindromic Substring
**Problem**: Find the longest substring that is a palindrome.

**Code**:
```cpp
string longestPalindrome(string s) {
    int start = 0, maxLength = 1;
    for (int i = 0; i < s.size(); ++i) {
        int l = i, r = i;
        while (l >= 0 && r < s.size() && s[l] == s[r]) {
            if (r - l + 1 > maxLength) start = l, maxLength = r - l + 1;
            --l, ++r;
        }
        l = i, r = i + 1;
        while (l >= 0 && r < s.size() && s[l] == s[r]) {
            if (r - l + 1 > maxLength) start = l, maxLength = r - l + 1;
            --l, ++r;
        }
    }
    return s.substr(start, maxLength);
}
```

## 6. Subarray with Given Sum
**Problem**: Find if there’s a subarray with a given sum.

**Code**:
```cpp
bool subarraySum(vector<int>& nums, int target) {
    int sum = 0, start = 0;
    for (int end = 0; end < nums.size(); ++end) {
        sum += nums[end];
        while (sum > target && start < end) sum -= nums[start++];
        if (sum == target) return true;
    }
    return false;
}
```

## 7. Reverse Words in a String
**Problem**: Reverse the order of words in a given string.

**Code**:
```cpp
string reverseWords(string s) {
    reverse(s.begin(), s.end());
    int start = 0;
    for (int end = 0; end <= s.size(); ++end) {
        if (end == s.size() || s[end] == ' ') {
            reverse(s.begin() + start, s.begin() + end);
            start = end + 1;
        }
    }
    return s;
}
```

## 8. Longest Common Prefix
**Problem**: Find the longest common prefix in an array of strings.

**Code**:
```cpp
string longestCommonPrefix(vector<string>& strs) {
    if (strs.empty()) return "";
    string prefix = strs[0];
    for (int i = 1; i < strs.size(); ++i) {
        while (strs[i].find(prefix) != 0) prefix = prefix.substr(0, prefix.size() - 1);
    }
    return prefix;
}
```

## 9. Count Subarrays with Sum Equals K
**Problem**: Count the number of subarrays that sum to `K`.

**Code**:
```cpp
int subarraySumEqualsK(vector<int>& nums, int k) {
    int count = 0, sum = 0;
    unordered_map<int, int> sumFreq;
    sumFreq[0] = 1;
    for (int num : nums) {
        sum += num;
        count += sumFreq[sum - k];
        sumFreq[sum]++;
    }
    return count;
}
```

## 10. Majority Element
**Problem**: Find the majority element in an array.

**Code**:
```cpp
int majorityElement(vector<int>& nums) {
    int candidate = nums[0], count = 1;
    for (int i = 1; i < nums.size(); ++i) {
        if (nums[i] == candidate) count++;
        else if (--count == 0) candidate = nums[i], count = 1;
    }
    return candidate;
}
```

## 11. String Rotation Check
**Problem**: Check if one string is a rotation of another.

**Code**:
```cpp
bool isRotation(string s1, string s2) {
    return s1.size() == s2.size() && (s1 + s1).find(s2) != string::npos;
}
```

## 12. Subarray Product Less Than K
**Problem**: Count the number of subarrays where the product is less than K.

**Code**:
```cpp
int numSubarrayProductLessThanK(vector<int>& nums, int k) {
    int product = 1, count = 0, left = 0;
    for (int right = 0; right < nums.size(); ++right) {
        product *= nums[right];
        while (left <= right && product >= k) product /= nums[left++];
        count += right - left + 1;
    }
    return count;
}
```

## 13. Count Distinct Elements in Every Subarray of Size K
**Problem**: Count distinct elements in each subarray of size `K`.

**Code**:
```cpp
vector<int> distinctElementsInWindow(vector<int>& nums, int k) {
    vector<int> result;
    unordered_map<int, int> freq;
    for (int i = 0; i < nums.size(); ++i) {
        freq[nums[i]]++;
        if (i >= k) {
            if (--freq[nums[i - k]] == 0) freq.erase(nums[i - k]);
        }
        if (i >= k - 1) result.push_back(freq.size());
    }
    return result;
}
```

## 14. Minimum Window Substring
**Problem**: Find the smallest substring that contains all characters of another string.

**Code**:
```cpp
string minWindow(string s, string t) {
    unordered_map<char, int> tFreq, windowFreq;
    for (char c : t) tFreq[c]++;
    int left = 0, minLen = INT_MAX, minStart = 0, matchCount = 0;
    for (int right = 0; right < s.size(); ++right) {
        char rChar = s[right];
        if (++windowFreq[rChar] == tFreq[rChar]) matchCount++;
        while (matchCount == tFreq.size()) {
            if (right - left + 1 < minLen) minLen = right - left + 1, minStart = left;
            if (--windowFreq[s[left]] < tFreq[s[left]]) matchCount--;
            left++;
        }
    }
    return minLen == INT_MAX ? "" : s.substr(minStart, minLen);
}
```

## 15. Valid Anagram Check
**Problem**: Check if two strings are anagrams.

**Code**:
```cpp
bool isAnagram(string s, string t) {
    if (s.size() != t.size()) return false;
    vector<int> freq(26, 0);
    for (char c : s) freq[c - 'a']++;
    for (char c : t) if (--freq[c - 'a'] < 0) return false;
    return true;
}
```
