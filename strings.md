
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
