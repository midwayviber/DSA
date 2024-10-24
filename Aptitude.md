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

These notes should help you cover all the key points for your test! Good luck!
