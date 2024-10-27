
### 1. Which of the following is the correct way to concatenate two strings `s1` and `s2` in C++?

```markdown
- A) `s1.concat(s2);`
- B) `s1 + s2;`
- C) `s1.append(s2);`
- D) `Both B and C`
```
**Answer:** D

---

### 2. What will be the output of the following code snippet?
   ```cpp
   string s = "hello";
   s[0] = 'H';
   cout << s;
   ```
```markdown
- A) `Hello`
- B) `hello`
- C) `H`
- D) Compile-time error
```
**Answer:** A

---

### 3. What does the function `s.substr(3)` return if `s = "programming"`?

```markdown
- A) `gramming`
- B) `ogramming`
- C) `ming`
- D) `ramming`
```
**Answer:** A

---

### 4. Which header file is required to use C++ `string` class?

```markdown
- A) `string.h`
- B) `iostream`
- C) `cstring`
- D) `string`
```
**Answer:** D

---

### 5. What is the output of the following code?
   ```cpp
   string s = "example";
   cout << s.substr(2, 3);
   ```
```markdown
- A) `amp`
- B) `exa`
- C) `mpl`
- D) `sam`
```
**Answer:** A

---

### 6. Which function can be used to find the first occurrence of a character in a string?

```markdown
- A) `find_first()`
- B) `find()`
- C) `index()`
- D) `search()`
```
**Answer:** B

---

### 7. What will be the result of the following code snippet?
   ```cpp
   string s = "C++ Programming";
   s.erase(3, 11);
   cout << s;
   ```
```markdown
- A) `C++`
- B) `C++ ng`
- C) `C++ rogramming`
- D) `C++ Pro`
```
**Answer:** A

---

### 8. How do you check if a string is empty in C++?

```markdown
- A) `if (s.empty())`
- B) `if (s.length() == 0)`
- C) `if (s.size() == 0)`
- D) `All of the above`
```
**Answer:** D

---

### 9. What is the output of the following code?
   ```cpp
   string str = "apple";
   str[0] = 'A';
   cout << str;
   ```
```markdown
- A) `apple`
- B) `Apple`
- C) `Aple`
- D) `Error`
```
**Answer:** B

---

### 10. Which method is used to convert a string to an integer?

```markdown
- A) `to_integer()`
- B) `convert()`
- C) `stoi()`
- D) `int()`
```
**Answer:** C

---

### 11. Which of the following correctly creates a string with a repeated character?

```markdown
- A) `string s(5, 'a');`
- B) `string s('a', 5);`
- C) `string s = repeat('a', 5);`
- D) `string s = "aaaaa";`
```
**Answer:** A

---

### 12. How can you compare two strings for equality?

```markdown
- A) `s1 == s2`
- B) `s1.compare(s2) == 0`
- C) `s1.equals(s2)`
- D) Both A and B
```
**Answer:** D

---

### 13. Which function returns the last character of a string?

```markdown
- A) `last()`
- B) `back()`
- C) `end()`
- D) `tail()`
```
**Answer:** B

---

### 14. What does the `find()` method return if the character is not found?

```markdown
- A) `0`
- B) `-1`
- C) `string::npos`
- D) `nullptr`
```
**Answer:** C

---

### 15. Which of the following will correctly reverse a string in C++?

```markdown
- A) `reverse(s.begin(), s.end());`
- B) `s.reverse();`
- C) `s = reverse(s);`
- D) `s.reverse_string();`
```
**Answer:** A

---

### 16. Which method is used to remove leading and trailing whitespace from a string?

```markdown
- A) `trim()`
- B) `strip()`
- C) `clear()`
- D) `erase()`
```
**Answer:** A

---

### 17. What is the output of the following code?
   ```cpp
   string s = "OpenAI";
   s += " GPT";
   cout << s;
   ```
```markdown
- A) `OpenAI`
- B) `OpenAI GPT`
- C) `OpenAIGPT`
- D) `Error`
```
**Answer:** B

---

### 18. How can you convert a string to lowercase?

```markdown
- A) `transform(s.begin(), s.end(), s.begin(), ::tolower);`
- B) `s.lower();`
- C) `s.toLowerCase();`
- D) `s.make_lowercase();`
```
**Answer:** A

---

### 19. What will be the output of the following code?
   ```cpp
   string s1 = "hello";
   string s2 = "world";
   cout << s1 + s2;
   ```
```markdown
- A) `helloworld`
- B) `hello world`
- C) `hello`
- D) `world`
```
**Answer:** A

---

### 20. Which of the following functions is used to convert a string to uppercase?

```markdown
- A) `toupper()`
- B) `make_uppercase()`
- C) `transform()`
- D) `upper()`
```
**Answer:** C

---

### 21. What will be the output of this code snippet?
   ```cpp
   string str = "Hello, World!";
   cout << str.find('W');
   ```
```markdown
- A) `7`
- B) `6`
- C) `5`
- D) `Error`
```
**Answer:** B

---

### 22. Which of the following is not a valid string constructor?

```markdown
- A) `string s1 = "hello";`
- B) `string s2(5, 'x');`
- C) `string s3 = string();`
- D) `string s4 = "hello" + "world";`
```
**Answer:** D

---

### 23. How can you replace a substring in a string?

```markdown
- A) `s.replace("old", "new");`
- B) `s.replace(s.find("old"), "old".length(), "new");`
- C) `s.change("old", "new");`
- D) `s.modify("old", "new");`
```
**Answer:** B

---

### 24. Which of the following is the correct syntax to declare a string?

```markdown
- A) `string s;`
- B) `String s;`
- C) `std::string s;`
- D) Both A and C
```
**Answer:** D

---

### 25. What is the purpose of `std::getline()`?

```markdown
- A) To read a single character from input
- B) To read a string until a newline character
- C) To read input into a character array
- D) To convert a string to an integer
```
**Answer:** B

---

### 26. Which method is used to split a string into substrings based on a delimiter?

```markdown
- A) `split()`
- B) `tokenize()`
- C) `s.substr()`
- D) No direct method in STL
```
**Answer:** D

---

### 27. What is the output of the following code?
   ```cpp
   string s = "123";
   int num = stoi(s);
   cout << num + 1;
   ```
```markdown
- A) `123`
- B) `124`
- C) `Error`
- D) `1`
```
**Answer:** B

---

### 28. How do you check if a string contains a specific substring?

```markdown
- A) `s.contains("substring")`
- B) `s.find("substring") != string::npos`
- C) `s.has("substring")`
- D) `s.indexOf("substring")`
```
**Answer:** B

---

### 29. Which of the following statements about `std::string` is true?

```markdown
- A) `std::string` is immutable.
- B) `std::string` automatically handles memory.
- C) `std::string` cannot store characters outside ASCII.
- D) `std::string` is

 only for UTF-8 encoded strings.
```
**Answer:** B

---

### 30. How do you convert a number to a string?

```markdown
- A) `string s = convert(num);`
- B) `string s = to_string(num);`
- C) `string s = int_to_string(num);`
- D) `string s = num.toString();`
```
**Answer:** B

---

Here are 10 advanced-level multiple-choice questions (MCQs) related to strings in C++, formatted in Markdown, focusing on challenging concepts that may come up in coding interviews:

### 1. Which algorithm can be used to efficiently search for a substring in a string?

```markdown
- A) Linear Search
- B) KMP (Knuth-Morris-Pratt)
- C) Binary Search
- D) Brute Force
```
**Answer:** B

---

### 2. What is the time complexity of the `std::string::find()` method in the worst case?

```markdown
- A) O(n)
- B) O(n^2)
- C) O(log n)
- D) O(1)
```
**Answer:** A

---

### 3. How can you check if two strings are rotations of each other?

```markdown
- A) By sorting both strings and comparing them
- B) By concatenating one string with itself and checking for the other
- C) By checking if their lengths are equal
- D) Both A and B
```
**Answer:** B

---

### 4. Which of the following is a method to split a string into substrings based on a delimiter in C++?

```markdown
- A) `s.split(delimiter);`
- B) `std::istringstream`
- C) `s.tokenize(delimiter);`
- D) `s.substr(delimiter);`
```
**Answer:** B

---

### 5. What is the output of the following code snippet?
   ```cpp
   string str = "abc";
   str[1] = 'x';
   cout << str;
   ```
```markdown
- A) `abc`
- B) `axc`
- C) `Error`
- D) `x`
```
**Answer:** B

---

### 6. Which STL function can be used to remove duplicate characters from a string?

```markdown
- A) `unique()`
- B) `distinct()`
- C) `remove_duplicates()`
- D) `erase_duplicates()`
```
**Answer:** A

---

### 7. How do you reverse a string in place?

```markdown
- A) `reverse(s.begin(), s.end());`
- B) `s.reverse();`
- C) `s = reverse(s);`
- D) `for(int i = 0; i < s.length()/2; i++) swap(s[i], s[s.length()-1-i]);`
```
**Answer:** D

---

### 8. Which of the following can be used to convert a string to a float in C++?

```markdown
- A) `to_float()`
- B) `stof()`
- C) `convert_to_float()`
- D) `float(st);`
```
**Answer:** B

---

### 9. What is the purpose of the `std::string::replace()` method?

```markdown
- A) To replace a substring with another string
- B) To replace all occurrences of a character
- C) To replace characters at specific positions
- D) All of the above
```
**Answer:** D

---

### 10. Which of the following statements about `std::string` and memory is true?

```markdown
- A) `std::string` is always allocated on the stack.
- B) `std::string` handles its own memory allocation and deallocation.
- C) `std::string` cannot be resized after initialization.
- D) `std::string` always uses a fixed size buffer.
```
**Answer:** B

---

### 1. What is the result of the following code?
```cpp
std::string s = "hello";
s.insert(2, "XY");
std::cout << s;
```
```markdown
- A) `heXYllo`
- B) `heXYllo`
- C) `helloXY`
- D) `hellXYo`
```
**Answer:** A

---

### 2. Which of the following correctly splits a string by a delimiter using `std::stringstream`?

```cpp
- A) `std::stringstream ss(s);`
- B) `while (getline(ss, token, delimiter))`
- C) `std::string token;`
- D) All of the above
```
**Answer:** D

---

### 3. What does the following code print?
```cpp
std::string str = "abcde";
std::cout << str.substr(1, 3);
```
```markdown
- A) `abc`
- B) `bcd`
- C) `cde`
- D) `de`
```
**Answer:** B

---

### 4. In which of the following cases does using `std::string::reserve()` not change the size of the string?

```markdown
- A) When the reserved size is less than the current size
- B) When the reserved size is equal to the current size
- C) When the reserved size is greater than the current size
- D) Both A and B
```
**Answer:** D

---

### 5. What will be the output of the following code?
```cpp
std::string str1 = "hello";
std::string str2 = str1;
str1[0] = 'H';
std::cout << str2;
```
```markdown
- A) `hello`
- B) `Hello`
- C) `h`
- D) `Error`
```
**Answer:** A

---

### 6. Which of the following correctly checks if a string is a palindrome in C++?

```markdown
- A) `s == reverse(s)`
- B) `s == std::string(s.rbegin(), s.rend())`
- C) `std::equal(s.begin(), s.end(), s.rbegin())`
- D) Both B and C
```
**Answer:** D

---

### 7. What will be the output of the following code snippet?
```cpp
std::string str = "hello";
str.replace(1, 3, "abc");
std::cout << str;
```
```markdown
- A) `habclo`
- B) `habc`
- C) `haabc`
- D) `heabc`
```
**Answer:** D

---

### 8. What is the time complexity of `std::string::find()` in the worst case?

```markdown
- A) O(n)
- B) O(n log n)
- C) O(n^2)
- D) O(1)
```
**Answer:** A

---

### 9. Which function is used to convert a string to a double in C++?

```markdown
- A) `to_double()`
- B) `stod()`
- C) `strtod()`
- D) `convert_to_double()`
```
**Answer:** B

---

### 10. Which of the following will successfully reverse a string in C++?

```markdown
- A) `std::reverse(s.begin(), s.end());`
- B) `s.reverse();`
- C) `s = std::reverse(s);`
- D) `s = reverse(s.begin(), s.end());`
```
**Answer:** A

---

### 11. What will be the output of the following code?
```cpp
std::string s1 = "abc";
std::string s2 = "ABC";
std::cout << (s1 < s2);
```
```markdown
- A) `1`
- B) `0`
- C) `true`
- D) `false`
```
**Answer:** A

---

### 12. Which method would you use to convert a `std::string` to an integer?

```markdown
- A) `string_to_int()`
- B) `stoi()`
- C) `convert()`
- D) `to_integer()`
```
**Answer:** B

---

### 13. What will the following code output?
```cpp
std::string s = "hello";
std::cout << s.find_first_of("aeiou");
```
```markdown
- A) `0`
- B) `1`
- C) `4`
- D) `-1`
```
**Answer:** B

---

### 14. Which of the following will correctly check if a string contains only digits?

```markdown
- A) `std::all_of(s.begin(), s.end(), ::isdigit);`
- B) `s.isdigit();`
- C) `std::isdigit(s);`
- D) `s.is_numeric();`
```
**Answer:** A

---

### 15. What will the following code output?
```cpp
std::string s = "   trim me   ";
s.erase(0, s.find_first_not_of(" "));
s.erase(s.find_last_not_of(" ") + 1);
std::cout << "'" << s << "'";
```
```markdown
- A) `'trim me'`
- B) `'   trim me   '`
- C) `'trim me   '`
- D) `'   trim me'`
```
**Answer:** A

---

### 16. Which of the following methods is used to compare two strings lexicographically?

```markdown
- A) `s1.equals(s2);`
- B) `s1.compare(s2);`
- C) `s1 == s2;`
- D) Both B and C
```
**Answer:** D

---

### 17. What does the function `std::string::clear()` do?

```markdown
- A) Deletes the string
- B) Resets the string to its initial state
- C) Removes all whitespace from the string
- D) Both A and B
```
**Answer:** B

---

### 18. How can you remove duplicate characters from a string in C++?

```markdown
- A) Using `std::unique()` and `std::erase()`
- B) Using a loop and `std::find()`
- C) Using `std::remove_duplicates()`
- D) Both A and B
```
**Answer:** D

---

### 19. What will be the output of the following code?
```cpp
std::string str = "hello";
std::cout << str.substr(2, 1);
```
```markdown
- A) `h`
- B) `e`
- C) `l`
- D) `lo`
```
**Answer:** C

---

### 20. Which of the following statements about `std::string` is false?

```markdown
- A) It can store Unicode characters.
- B) It can be resized dynamically.
- C) It is immutable once created.
- D) It can be initialized from a character array.
```
**Answer:** C

---

### 21. How do you replace all occurrences of a character in a string?

```markdown
- A) Using `std::replace()`
- B) Using `std::replace_if()`
- C) By iterating and replacing manually
- D) All of the above
```
**Answer:** D

---

### 22. What will be the output of the following code?
```cpp
std::string s = "abcabc";
s.erase(std::remove(s.begin(), s.end(), 'a'), s.end());
std::cout << s;
```
```markdown
- A) `bcabc`
- B) `abc`
- C) `bc`
- D) `Error`
```
**Answer:** A

---

### 23. Which of the following correctly appends a character to a string?

```markdown
- A) `s.push_back('c');`
- B) `s += 'c';`
- C) `s.append('c');`
- D) All of the above
```
**Answer:** D

---

### 24. What will be the result of the following code snippet?
```cpp
std::string str = "Hello, World!";
std::cout << str.find(", ");
```
```markdown
- A) `5`
- B) `6`
- C) `7`
- D) `-1`
```
**Answer:** A

---

### 25. Which of the following is true about `std::string::data()`?

```markdown
- A) Returns a const char*
- B) Returns a mutable char*
- C) Returns a copy of the string data
- D) Both A and B
```
**Answer:** A

---

### 26. What will the following code output?
```cpp
std::string s1 = "hello";
std::string s2 = "HELLO";
std::cout << (s1.compare(s2) == 0);
```
```markdown
- A) `1`
- B) `0`
- C) `true`
- D) `false`
```
**Answer:** D

### 27. How do you concatenate two strings efficiently?

```markdown
- A) `s1 + s2;`
- B) `s1.append(s2);`
- C) `s1 += s2;`
- D) All of the above
```
**Answer:** D

---

### 28. Which of the following functions is used to find the last occurrence of a character in a string?

```markdown
- A) `s.find_last_of()`
- B) `s.rfind()`
- C) `s.find()`
- D) Both A and B
```
**Answer:** D

---

### 29. What does the following code output?
```cpp
std::string s = "abcdefg";
s.erase(s.begin() + 2, s.end() - 2);
std::cout << s;
```
```markdown
- A) `abc`
- B) `de`
- C) `fg`
- D) `a`
```
**Answer:** A

---

### 30. Which of the following methods allows you to convert a string into lowercase in C++?

```markdown
- A) `std::transform(s.begin(), s.end(), s.begin(), ::tolower);`
- B) `s.toLower();`
- C) `std::tolower(s);`
- D) `s.lowercase();`
```
**Answer:** A

---
