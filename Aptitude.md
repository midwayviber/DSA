# Aptitude Notes

## 1. **Number System**

The number system deals with different types of numbers and their properties.

### Types of Numbers:
1. **Natural Numbers**: Counting numbers starting from 1 (1, 2, 3, ...).
2. **Whole Numbers**: Natural numbers including 0 (0, 1, 2, 3, ...).
3. **Integers**: All positive and negative whole numbers including 0 (-2, -1, 0, 1, 2, ...).
4. **Rational Numbers**: Numbers that can be expressed in the form of \( \frac{p}{q} \), where \( p \) and \( q \) are integers and \( q \neq 0 \).
5. **Irrational Numbers**: Numbers that cannot be expressed as a fraction (e.g., \( \sqrt{2}, \pi \)).
6. **Real Numbers**: All rational and irrational numbers.
7. **Prime Numbers**: Numbers greater than 1 with no divisors other than 1 and themselves (e.g., 2, 3, 5, 7, 11, ...).
8. **Composite Numbers**: Numbers that have more than two divisors (e.g., 4, 6, 8, 9, ...).

### Key Concepts:
- **Even Numbers**: Numbers divisible by 2.
- **Odd Numbers**: Numbers not divisible by 2.
- **Divisibility Rules**:
  - **By 2**: Number ends in 0, 2, 4, 6, or 8.
  - **By 3**: Sum of digits is divisible by 3.
  - **By 5**: Number ends in 0 or 5.
  - **By 11**: Difference between the sum of alternate digits is divisible by 11.

### Properties of Numbers:
- **Addition**: \( a + b = b + a \) (Commutative), \( (a + b) + c = a + (b + c) \) (Associative).
- **Multiplication**: \( a \times b = b \times a \) (Commutative), \( (a \times b) \times c = a \times (b \times c) \) (Associative).
- **Distributive Property**: \( a(b + c) = ab + ac \).

### Factorization:
- Breaking a number down into its prime factors.
  - Example: 36 = \( 2^2 \times 3^2 \).

### Remainder Theorem:
- If a number \( N \) is divided by a divisor \( D \), then the remainder \( R \) is found using:
  \[
  N = D \times Q + R
  \]
  where \( Q \) is the quotient and \( R \) is the remainder.

---

## 2. **LCM & HCF**

### **Least Common Multiple (LCM)**:
The smallest number that is a multiple of two or more numbers.

#### Steps to Find LCM:
1. Find the prime factorization of each number.
2. Take the highest powers of all prime factors.
3. Multiply them together to get the LCM.

- **Example**:
  - Find LCM of 12 and 15.
    - 12 = \( 2^2 \times 3 \)
    - 15 = \( 3 \times 5 \)
    - LCM = \( 2^2 \times 3 \times 5 = 60 \).

#### Shortcut Formula:
If \( a \) and \( b \) are two numbers, then:
\[
LCM(a, b) = \frac{a \times b}{HCF(a, b)}
\]

### **Highest Common Factor (HCF)**:
The largest number that divides two or more numbers.

#### Steps to Find HCF:
1. Find the prime factorization of each number.
2. Take the lowest powers of all common prime factors.
3. Multiply them together to get the HCF.

- **Example**:
  - Find HCF of 12 and 15.
    - 12 = \( 2^2 \times 3 \)
    - 15 = \( 3 \times 5 \)
    - HCF = 3.

#### HCF Using Euclidean Algorithm:
For two numbers \( a \) and \( b \):
1. Divide \( a \) by \( b \) and get the remainder \( r \).
2. Replace \( a \) with \( b \) and \( b \) with \( r \).
3. Repeat until the remainder is 0. The divisor at this step is the HCF.

---

## 3. **Ratio & Proportion**

### **Ratio**:
A ratio compares two quantities of the same kind and is written as \( a : b \), where \( a \) and \( b \) are quantities.

- **Example**: If a bag contains 3 red balls and 5 blue balls, the ratio of red balls to blue balls is \( 3 : 5 \).

#### Properties of Ratios:
- \( a : b = \frac{a}{b} \).
- Invert the ratio: \( b : a \).
- Multiply or divide both terms of the ratio by the same number.

#### Types of Ratios:
1. **Duplicate Ratio**: \( a^2 : b^2 \).
2. **Triplicate Ratio**: \( a^3 : b^3 \).
3. **Sub-duplicate Ratio**: \( \sqrt{a} : \sqrt{b} \).

### **Proportion**:
When two ratios are equal, they are said to be in proportion.
- \( a : b = c : d \) is written as \( a : b :: c : d \), where \( a \) and \( d \) are called "extremes," and \( b \) and \( c \) are called "means."
  
- **Example**: If 2 : 3 = 6 : 9, then \( 2 \times 9 = 3 \times 6 \).

#### Properties of Proportions:
- **Cross Multiplication**: In a proportion \( \frac{a}{b} = \frac{c}{d} \), cross-multiply to get \( a \times d = b \times c \).

#### Direct & Inverse Proportion:
1. **Direct Proportion**: If \( x \) and \( y \) are directly proportional, then \( x \propto y \), meaning \( x = k \times y \) (for some constant \( k \)).
2. **Inverse Proportion**: If \( x \) and \( y \) are inversely proportional, then \( x \propto \frac{1}{y} \), meaning \( x \times y = k \) (for some constant \( k \)).

---

## 4. **Averages**

The average (or mean) of a set of numbers is the sum of all the numbers divided by the count of numbers.

#### Formula:
\[
\text{Average} = \frac{\text{Sum of all terms}}{\text{Number of terms}}
\]

### Key Concepts:
1. **Finding the Total**: Given the average and the number of terms, the sum can be found as:
   \[
   \text{Sum of terms} = \text{Average} \times \text{Number of terms}
   \]

2. **Weighted Average**: When different items contribute differently to the total, the weighted average is calculated as:
   \[
   \text{Weighted Average} = \frac{w_1x_1 + w_2x_2 + \dots + w_nx_n}{w_1 + w_2 + \dots + w_n}
   \]
   where \( w_1, w_2, \dots \) are weights and \( x_1, x_2, \dots \) are the values.

3. **Effect on Average**:
   - **Inclusion of New Data**: If new data is added, recalculate the average with the updated sum and count.
   - **Removal of Data**: Recalculate by adjusting the sum and count appropriately.

#### Example Problem:
- **Find the average of 4, 8, 6, and 10**:
  - Sum of terms = \( 4 + 8 + 6 + 10 = 28 \)
  - Number of terms = 4
  - Average = \( \frac{28}{4} = 7 \)

---

# Number System MCQ Questions with Explanations

### Q1. The number which when divided by 7, 11, and 13 leaves a remainder of 5 in each case is:
- A) 998
- B) 959
- C) 960
- D) 945  
**Answer**: B) 959  
**Explanation**: The least common multiple (LCM) of 7, 11, and 13 is 1001. The number should be of the form 1001n + 5. For n = 0, the number is 5. For n = 1, the number is 1001 + 5 = 1006. So, for n = -1, the number is 1001 - 5 = 959.

### Q2. What is the least number which when divided by 4, 6, 8, 12, and 16 leaves a remainder of 2 in each case?
- A) 48
- B) 50
- C) 46
- D) 58  
**Answer**: B) 50  
**Explanation**: The LCM of 4, 6, 8, 12, and 16 is 48. The least number that leaves a remainder of 2 must be of the form 48n + 2. For n = 1, the number is 50.

### Q3. Find the largest number which divides 62, 132, and 237 leaving remainders 2, 3, and 4 respectively.
- A) 10
- B) 15
- C) 25
- D) 35  
**Answer**: A) 10  
**Explanation**: The numbers are 62 - 2 = 60, 132 - 3 = 129, and 237 - 4 = 233. We need to find the GCD (Greatest Common Divisor) of 60, 129, and 233, which is 10.

### Q4. A two-digit number is such that the product of its digits is 18. If 63 is added to the number, the digits interchange their places. What is the number?
- A) 26
- B) 36
- C) 63
- D) 72  
**Answer**: B) 36  
**Explanation**: Let the digits be x and y. Then the number is 10x + y. The product of digits is xy = 18. When 63 is added, the digits interchange, so the new number is 10y + x. Therefore, 10y + x = 10x + y + 63. Solving these equations, we get x = 3 and y = 6. So, the number is 36.

### Q5. The number 7254*98 is divisible by 11. Find the missing digit.
- A) 3
- B) 4
- C) 7
- D) 6  
**Answer**: D) 6  
**Explanation**: For a number to be divisible by 11, the alternating sum of its digits should be divisible by 11. For 7254*98, we calculate (7 - 2 + 5 - 4 + * - 9 + 8). Setting this equal to a multiple of 11, we find the missing digit * = 6.

### Q6. The smallest number which when increased by 5 is completely divisible by 8, 12, and 15 is:
- A) 115
- B) 120
- C) 235
- D) 240  
**Answer**: A) 115  
**Explanation**: The LCM of 8, 12, and 15 is 120. The number should be of the form 120n - 5. For n = 1, the number is 115.

### Q7. A number when divided by 12 leaves a remainder of 5. If the same number is divided by 8, the remainder is 1. What is the number?
- A) 17
- B) 25
- C) 29
- D) 37  
**Answer**: C) 29  
**Explanation**: The number can be written as 12k + 5. It should also be in the form 8m + 1. Testing values, we find that 29 satisfies both conditions.

### Q8. A number consists of two digits such that the digit at the tens place is twice the digit in the unit's place. If the sum of the digits is 12, find the number.
- A) 63
- B) 72
- C) 93
- D) 84  
**Answer**: D) 84  
**Explanation**: Let the digits be x and y. The number is 10x + y. Given that x = 2y and x + y = 12, solving these equations gives x = 8 and y = 4. Hence, the number is 84.

### Q9. The sum of two numbers is 256 and their HCF is 32. How many such pairs of numbers are possible?
- A) 1
- B) 2
- C) 3
- D) 4  
**Answer**: B) 2  
**Explanation**: Let the numbers be 32a and 32b. Then 32(a + b) = 256, which gives a + b = 8. The pairs (a, b) are (1, 7) and (3, 5), so there are 2 pairs.

### Q10. What is the remainder when 17^23 is divided by 16?
- A) 1
- B) 2
- C) 3
- D) 5  
**Answer**: A) 1  
**Explanation**: Using Fermat's Little Theorem, for any prime p, a^(p-1) ≡ 1 (mod p). Here, since 17 ≡ 1 (mod 16), 17^23 ≡ 1^23 = 1 (mod 16).

### Q11. The least number which when divided by 5, 6, 7, 8 leaves a remainder of 3, but when divided by 9 leaves no remainder, is:
- A) 1677
- B) 1683
- C) 2523
- D) 3363  
**Answer**: B) 1683  
**Explanation**: The LCM of 5, 6, 7, 8 is 840. The number is of the form 840n + 3. Checking, we find that for n = 2, the number 1683 satisfies the conditions.

### Q12. The least number of five digits which is divisible by 16, 24, 36, and 54 is:
- A) 10080
- B) 10368
- C) 10416
- D) 10752  
**Answer**: C) 10416  
**Explanation**: The LCM of 16, 24, 36, and 54 is 432. The smallest five-digit number divisible by 432 is 10416.

### Q13. Find the number of zeros at the end of 100 factorial (100!).
- A) 24
- B) 25
- C) 20
- D) 22  
**Answer**: B) 25  
**Explanation**: The number of trailing zeros in a factorial is determined by the number of factors of 5. For 100!, the count is ⌊100/5⌋ + ⌊100/25⌋ = 20 + 5 = 25.

### Q14. When 1256 is divided by a certain divisor, the quotient is 28 and the remainder is 8. What is the divisor?
- A) 44
- B) 48
- C) 42
- D) 45  
**Answer**: C) 44  
**Explanation**: Let the divisor be d. Then 1256 = 28d + 8. Solving, we get d = (1256 - 8)/28 = 44.

### Q15. What is the smallest number that leaves a remainder of 2 when divided by 3, 5, 7, and 9?
- A) 317
- B) 317
- C) 317
- D) 314  
**Answer**: D) 314  
**Explanation**: The LCM of 3, 5, 7, and 9 is 315. The smallest number that leaves a remainder of 2 is 315 - 1 = 314.

### Q16. The largest number of four digits which is divisible by 15, 25, 40, and 75 is:
- A) 9600
- B) 9400
- C) 9200
- D) 9000  
**Answer**: A) 9600  
**Explanation**: The LCM of 15, 25, 40, and 75 is 600. The largest four-digit number divisible by 600 is 9600.

### Q17. What is the largest power of 2 that divides 80! exactly?
- A) 73
- B) 74
- C) 75
- D) 76  
**Answer**: C) 75  
**Explanation**: The number of factors of 2 in 80! is ⌊80/2⌋ + ⌊80/4⌋ + ⌊80/8⌋ + ⌊80/16⌋ + ⌊80/32⌋ + ⌊80/64⌋ = 40 + 20 + 10 + 5 + 2 + 1 = 75.

### Q18. The difference between a two-digit number and the number obtained by interchanging the digits is 36. What is the difference between the digits of the number?
- A) 3
- B) 4
- C) 5
- D) 6  
**Answer**: B) 4  
**Explanation**: Let the number be 10x + y. Then the number formed by interchanging the digits is 10y + x. The difference is 36, i.e., (10x + y) - (10y + x) = 36, which simplifies to 9(x - y) = 36. Hence, x - y = 4.

### Q19. Find the smallest five-digit number which when divided by 16, 18, 20, and 25 leaves a remainder of 10 in each case.
- A) 10290
- B) 10010
- C) 10090
- D) 10190  
**Answer**: C) 10090  
**Explanation**: The LCM of 16, 18, 20, and 25 is 3600. The smallest number divisible by 3600 and leaving a remainder of 10 is 3600 + 10 = 10090.

### Q20. What is the remainder when 7^89 is divided by 6?
- A) 1
- B) 3
- C) 5
- D) 2  
**Answer**: A) 1  
**Explanation**: By Fermat’s Little Theorem, 7 ≡ 1 (mod 6). Therefore, 7^89 ≡ 1^89 = 1 (mod 6).

---

Here are 20 medium-to-hard level ratio and proportion questions with detailed explanations in Markdown format:

---

### 1. **If two numbers are in the ratio 5:7 and their sum is 120, find the numbers.**

The ratio is given as 5:7, and their sum is 120.  
Let the numbers be 5x and 7x.

\[
5x + 7x = 120
\]

\[
12x = 120
\]

\[
x = 120 / 12 = 10
\]

Thus, the numbers are:

\[
5x = 5 \times 10 = 50 \quad \text{and} \quad 7x = 7 \times 10 = 70
\]

**Answer:** a) 50, 70

---

### 2. **The salaries of A and B are in the ratio 2:3. If their total salary is $5000, what is the salary of A?**

Let A's salary be 2x and B's salary be 3x. The total salary is $5000.

\[
2x + 3x = 5000
\]

\[
5x = 5000
\]

\[
x = 5000 / 5 = 1000
\]

Thus, A's salary is:

\[
2x = 2 \times 1000 = 2000
\]

**Answer:** c) $2000

---

### 3. **Two numbers are in the ratio 3:4. If 8 is added to each number, the ratio becomes 5:6. Find the original numbers.**

Let the numbers be 3x and 4x. When 8 is added to each, the new ratio is 5:6.

\[
\frac{3x + 8}{4x + 8} = \frac{5}{6}
\]

Cross-multiply:

\[
6(3x + 8) = 5(4x + 8)
\]

\[
18x + 48 = 20x + 40
\]

\[
48 - 40 = 20x - 18x
\]

\[
8 = 2x
\]

\[
x = 4
\]

Thus, the original numbers are:

\[
3x = 3 \times 4 = 12 \quad \text{and} \quad 4x = 4 \times 4 = 16
\]

**Answer:** b) 12, 16

---

### 4. **The incomes of A, B, and C are in the ratio 7:9:12, and their expenses are in the ratio 8:9:15. If A saves $200, what is their income?**

Let the incomes of A, B, and C be 7x, 9x, and 12x, respectively, and let the expenses be 8y, 9y, and 15y. The savings of A is given as:

\[
\text{Savings of A} = 7x - 8y = 200
\]

This is one equation. Additional data is required to find the exact income.

**Answer:** Not enough information for a complete solution

---

### 5. **Two numbers are in the ratio 3:5. If the difference between them is 18, what are the numbers?**

Let the numbers be 3x and 5x. The difference between them is 18.

\[
5x - 3x = 18
\]

\[
2x = 18
\]

\[
x = 9
\]

Thus, the numbers are:

\[
3x = 3 \times 9 = 27 \quad \text{and} \quad 5x = 5 \times 9 = 45
\]

**Answer:** a) 27, 45

---

### 6. **The ratio of A’s age to B’s age is 4:5. After 6 years, the ratio will become 5:6. What is B’s current age?**

Let A’s age be 4x and B’s age be 5x. After 6 years, their ages will be in the ratio 5:6.

\[
\frac{4x + 6}{5x + 6} = \frac{5}{6}
\]

Cross-multiply:

\[
6(4x + 6) = 5(5x + 6)
\]

\[
24x + 36 = 25x + 30
\]

\[
36 - 30 = 25x - 24x
\]

\[
x = 6
\]

Thus, B's current age is:

\[
5x = 5 \times 6 = 30
\]

**Answer:** b) 30

---

### 7. **A sum of money is divided between A, B, and C in the ratio 2:3:5. If C’s share is $300 more than A’s, find the total amount.**

Let A’s share be 2x, B’s share be 3x, and C’s share be 5x. The difference between C’s and A’s share is $300.

\[
5x - 2x = 300
\]

\[
3x = 300
\]

\[
x = 100
\]

Thus, the total amount is:

\[
2x + 3x + 5x = 10x = 10 \times 100 = 1000
\]

**Answer:** c) $1000

---

### 8. **The ratio of A’s salary to B’s salary is 4:5. If A’s salary is increased by 20% and B’s by 10%, the ratio becomes 5:6. What is A’s salary?**

Let A’s salary be 4x and B’s salary be 5x. After the increase:

\[
\frac{4x \times 1.20}{5x \times 1.10} = \frac{5}{6}
\]

\[
\frac{4.8x}{5.5x} = \frac{5}{6}
\]

Cross-multiply:

\[
6(4.8x) = 5(5.5x)
\]

\[
28.8x = 27.5x
\]

This implies a contradiction. Check the input data.

---

### 9. **If the ratio of the present ages of A and B is 5:7, and after 6 years, the ratio becomes 3:4, find their present ages.**

Let A’s age be 5x and B’s age be 7x. After 6 years:

\[
\frac{5x + 6}{7x + 6} = \frac{3}{4}
\]

Cross-multiply:

\[
4(5x + 6) = 3(7x + 6)
\]

\[
20x + 24 = 21x + 18
\]

\[
24 - 18 = 21x - 20x
\]

\[
x = 6
\]

Thus, A’s and B’s current ages are:

\[
5x = 30 \quad \text{and} \quad 7x = 42
\]

**Answer:** d) 30, 42

---

### 10. **The weights of two people are in the ratio 4:5. If both of them gain 5 kg, the ratio becomes 5:6. Find their original weights.**

Let the original weights be 4x and 5x. After both gain 5 kg:

\[
\frac{4x + 5}{5x + 5} = \frac{5}{6}
\]

Cross-multiply:

\[
6(4x + 5) = 5(5x + 5)
\]

\[
24x + 30 = 25x + 25
\]

\[
30 - 25 = 25x - 24x
\]

\[
x = 5
\]

Thus, their original weights are:

\[
4x = 4 \times 5 = 20 \quad \text{and} \quad 5x = 5 \times 5 = 25
\]

**Answer:** a) 20, 25

---


