# 🧠 Interview Practice Questions — Easy Level
> **Topics:** Arrays · Strings · Basic Math  
> **Level:** Easy
> **Goal:** Build strong DSA fundamentals before interviews

---

## 📌 How to Use This Sheet
- Read the problem carefully
- Understand the Input/Output examples
- Think about the approach before jumping to code
- Write the solution in JavaScript (preferred for MERN)
- Check Time Complexity (TC) and Space Complexity (SC) after solving

---

# 📂 SECTION 1 — ARRAYS

---

### Q1. Find the Maximum Element in an Array

**Definition:**  
Given an array of integers, find and return the largest number present in the array.

**Example:**
```
Input:  [3, 7, 1, 9, 4]
Output: 9
```

**Constraints:**
- Array will have at least 1 element
- Elements can be negative

**TC:** O(n) | **SC:** O(1)

---

### Q2. Reverse an Array

**Definition:**  
Given an array, return a new array with all elements in reverse order.

**Example:**
```
Input:  [1, 2, 3, 4, 5]
Output: [5, 4, 3, 2, 1]
```

**Constraints:**
- Do not use built-in `.reverse()` method
- Array can contain any integers

**TC:** O(n) | **SC:** O(1) (in-place) or O(n) (new array)

---

### Q3. Find the Second Largest Element

**Definition:**  
Given an array of integers, find the second largest unique element. If no second largest exists, return -1.

**Example:**
```
Input:  [10, 5, 8, 20, 15]
Output: 15

Input:  [5, 5, 5]
Output: -1
```

**Constraints:**
- Array length ≥ 1
- Elements can repeat

**TC:** O(n) | **SC:** O(1)

---

### Q4. Check if Array is Sorted (Ascending)

**Definition:**  
Given an array of integers, return `true` if the array is sorted in non-decreasing (ascending) order, otherwise return `false`.

**Example:**
```
Input:  [1, 2, 3, 4, 5]
Output: true

Input:  [1, 3, 2, 5]
Output: false
```

**Constraints:**
- Array can have duplicate elements
- Empty array is considered sorted → return `true`

**TC:** O(n) | **SC:** O(1)

---

### Q5. Find All Duplicates in an Array

**Definition:**  
Given an array of integers, return all the elements that appear more than once. Return them in any order.

**Example:**
```
Input:  [1, 2, 3, 2, 4, 3, 5]
Output: [2, 3]
```

**Constraints:**
- Result order doesn't matter
- Each duplicate should appear only once in the output

**TC:** O(n) | **SC:** O(n)

---

### Q6. Move All Zeros to the End

**Definition:**  
Given an array of integers, move all `0`s to the end while maintaining the relative order of non-zero elements. Do this in-place.

**Example:**
```
Input:  [0, 1, 0, 3, 12]
Output: [1, 3, 12, 0, 0]

Input:  [0, 0, 1]
Output: [1, 0, 0]
```

**Constraints:**
- Modify the array in-place
- Preserve relative order of non-zero elements

**TC:** O(n) | **SC:** O(1)

---

### Q7. Sum of All Elements in an Array

**Definition:**  
Given an array of numbers, return the sum of all elements.

**Example:**
```
Input:  [1, 2, 3, 4, 5]
Output: 15

Input:  [-1, -2, 3]
Output: 0
```

**Constraints:**
- Array can have negative numbers
- Array can be empty → return 0

**TC:** O(n) | **SC:** O(1)

---

### Q8. Count Even and Odd Numbers

**Definition:**  
Given an array of integers, return an object (or two values) showing how many numbers are even and how many are odd.

**Example:**
```
Input:  [1, 2, 3, 4, 5, 6]
Output: { even: 3, odd: 3 }
```

**Constraints:**
- Include 0 as even
- Array can have negative numbers (−4 is even, −3 is odd)

**TC:** O(n) | **SC:** O(1)

---

# 📂 SECTION 2 — STRINGS

---

### Q9. Reverse a String

**Definition:**  
Given a string, return the string in reversed order.

**Example:**
```
Input:  "hello"
Output: "olleh"

Input:  "interview"
Output: "weivretnI"  ← wait, case preserved
Output: "weivretni"
```

**Constraints:**
- Do not use built-in `.reverse()` method directly
- Preserve case as-is

**TC:** O(n) | **SC:** O(n)

---

### Q10. Check if a String is a Palindrome

**Definition:**  
A string is a palindrome if it reads the same forward and backward. Return `true` if palindrome, else `false`. Ignore case and spaces.

**Example:**
```
Input:  "racecar"
Output: true

Input:  "A man a plan a canal Panama"
Output: true

Input:  "hello"
Output: false
```

**Constraints:**
- Ignore spaces and case
- Only consider alphanumeric characters

**TC:** O(n) | **SC:** O(1)

---

### Q11. Count the Number of Vowels

**Definition:**  
Given a string, count and return the number of vowels (`a, e, i, o, u`) present in it (case-insensitive).

**Example:**
```
Input:  "Hello World"
Output: 3   (e, o, o)

Input:  "rhythm"
Output: 0
```

**Constraints:**
- Both uppercase and lowercase vowels count
- Spaces and special characters are ignored

**TC:** O(n) | **SC:** O(1)

---

### Q12. Check if Two Strings are Anagrams

**Definition:**  
Two strings are anagrams if they contain the same characters with the same frequency, just in a different order. Return `true` or `false`.

**Example:**
```
Input:  "listen", "silent"
Output: true

Input:  "hello", "world"
Output: false
```

**Constraints:**
- Ignore case (treat as lowercase)
- Only consider alphabetic characters (ignore spaces/punctuation)

**TC:** O(n log n) or O(n) | **SC:** O(n)

---

### Q13. Find the First Non-Repeating Character

**Definition:**  
Given a string, find the first character that does not repeat. Return that character. If all characters repeat, return `null` or `"-1"`.

**Example:**
```
Input:  "aabbcde"
Output: "c"

Input:  "aabb"
Output: null
```

**Constraints:**
- String contains only lowercase letters
- Return just the character, not the index

**TC:** O(n) | **SC:** O(n)

---

### Q14. Count Words in a Sentence

**Definition:**  
Given a sentence (string), count the number of words in it. Words are separated by one or more spaces.

**Example:**
```
Input:  "Hello World this is JavaScript"
Output: 5

Input:  "  Hello   World  "
Output: 2
```

**Constraints:**
- Handle multiple spaces between words
- Handle leading/trailing spaces

**TC:** O(n) | **SC:** O(n)

---

### Q15. Capitalize First Letter of Each Word

**Definition:**  
Given a sentence, return it with the first letter of every word capitalized (Title Case).

**Example:**
```
Input:  "hello world from javascript"
Output: "Hello World From Javascript"
```

**Constraints:**
- Rest of the letters should remain as-is (or lowercase)
- Handle single-word strings

**TC:** O(n) | **SC:** O(n)

---

# 📂 SECTION 3 — BASIC MATH

---

### Q16. Check if a Number is Even or Odd

**Definition:**  
Given a number `n`, return `"Even"` if divisible by 2, otherwise return `"Odd"`.

**Example:**
```
Input:  4
Output: "Even"

Input:  7
Output: "Odd"
```

**Constraints:**
- `n` can be negative or zero
- Use modulo operator `%`

**TC:** O(1) | **SC:** O(1)

---

### Q17. Check if a Number is Prime

**Definition:**  
A prime number is greater than 1 and divisible only by 1 and itself. Return `true` if prime, else `false`.

**Example:**
```
Input:  7
Output: true

Input:  12
Output: false

Input:  1
Output: false
```

**Constraints:**
- `n ≥ 1`
- Optimize to loop only up to √n

**TC:** O(√n) | **SC:** O(1)

---

### Q18. Find Factorial of a Number

**Definition:**  
Given a non-negative integer `n`, return its factorial.  
Factorial of `n` = `n × (n-1) × (n-2) × ... × 1`.  
Factorial of `0` = `1`.

**Example:**
```
Input:  5
Output: 120  (5 × 4 × 3 × 2 × 1)

Input:  0
Output: 1
```

**Constraints:**
- `0 ≤ n ≤ 12` (to avoid overflow in JS)
- Can be solved iteratively or recursively

**TC:** O(n) | **SC:** O(1) iterative, O(n) recursive

---

### Q19. Fibonacci Number

**Definition:**  
Given a position `n`, return the `n`th Fibonacci number.  
Fibonacci sequence: 0, 1, 1, 2, 3, 5, 8, 13, 21, ...

**Example:**
```
Input:  6
Output: 8  (0,1,1,2,3,5,8 → index 6 = 8)

Input:  0
Output: 0

Input:  1
Output: 1
```

**Constraints:**
- `n ≥ 0`
- Try both iterative and recursive approach
- Recursive approach has TC: O(2ⁿ); iterative has TC: O(n)

**TC:** O(n) iterative | **SC:** O(1) iterative

---

### Q20. Reverse a Number

**Definition:**  
Given an integer, return the number with its digits reversed. Ignore leading zeros in the result.

**Example:**
```
Input:  1234
Output: 4321

Input:  1200
Output: 21   (leading zeros dropped)

Input:  -123
Output: -321
```

**Constraints:**
- Handle negative numbers (preserve the sign)
- Handle trailing zeros in input

**TC:** O(d) where d = number of digits | **SC:** O(1)

---

### Q21. Sum of Digits

**Definition:**  
Given a positive integer, return the sum of all its digits.

**Example:**
```
Input:  1234
Output: 10  (1 + 2 + 3 + 4)

Input:  999
Output: 27
```

**Constraints:**
- `n > 0`
- Can use string conversion or modulo approach

**TC:** O(d) | **SC:** O(1)

---

### Q22. Count Digits in a Number

**Definition:**  
Given a positive integer `n`, return the total number of digits in it.

**Example:**
```
Input:  12345
Output: 5

Input:  7
Output: 1
```

**Constraints:**
- `n ≥ 1`
- Do not use string conversion (try math approach for bonus)

**TC:** O(log n) | **SC:** O(1)

---

### Q23. GCD (Greatest Common Divisor)

**Definition:**  
Given two positive integers, return their Greatest Common Divisor — the largest number that divides both without a remainder.

**Example:**
```
Input:  12, 8
Output: 4

Input:  100, 75
Output: 25
```

**Constraints:**
- Both numbers > 0
- Use the Euclidean algorithm: `gcd(a, b) = gcd(b, a % b)`

**TC:** O(log(min(a,b))) | **SC:** O(1)

---

### Q24. Check Armstrong Number

**Definition:**  
A number is an Armstrong number if the sum of its digits each raised to the power of the number of digits equals the number itself.  
Example: `153 = 1³ + 5³ + 3³ = 153` ✅

**Example:**
```
Input:  153
Output: true

Input:  9474
Output: true  (9⁴ + 4⁴ + 7⁴ + 4⁴ = 9474)

Input:  123
Output: false
```

**Constraints:**
- `n ≥ 0`

**TC:** O(d) | **SC:** O(1)

---

## 🏁 Quick Reference: Complexity Cheat Sheet

| Complexity | Meaning                        | Example Problem         |
|------------|--------------------------------|--------------------------|
| O(1)       | Constant — doesn't grow        | Check even/odd           |
| O(log n)   | Logarithmic — very fast        | Count digits (math way)  |
| O(√n)      | Square root                    | Check prime              |
| O(n)       | Linear — loops once            | Find max, reverse array  |
| O(n log n) | Linearithmic                   | Sort-based anagram check |
| O(n²)      | Quadratic — nested loops       | Brute force duplicates   |

---

## ✅ Progress Tracker

| # | Problem | Solved | Reviewed |
|---|---------|--------|----------|
| 1 | Find Maximum Element | ☐ | ☐ |
| 2 | Reverse an Array | ☐ | ☐ |
| 3 | Second Largest Element | ☐ | ☐ |
| 4 | Check Sorted Array | ☐ | ☐ |
| 5 | Find All Duplicates | ☐ | ☐ |
| 6 | Move Zeros to End | ☐ | ☐ |
| 7 | Sum of Array | ☐ | ☐ |
| 8 | Count Even & Odd | ☐ | ☐ |
| 9 | Reverse a String | ☐ | ☐ |
| 10 | Palindrome Check | ☐ | ☐ |
| 11 | Count Vowels | ☐ | ☐ |
| 12 | Anagram Check | ☐ | ☐ |
| 13 | First Non-Repeating Char | ☐ | ☐ |
| 14 | Count Words | ☐ | ☐ |
| 15 | Title Case | ☐ | ☐ |
| 16 | Even or Odd | ☐ | ☐ |
| 17 | Prime Number | ☐ | ☐ |
| 18 | Factorial | ☐ | ☐ |
| 19 | Fibonacci | ☐ | ☐ |
| 20 | Reverse a Number | ☐ | ☐ |
| 21 | Sum of Digits | ☐ | ☐ |
| 22 | Count Digits | ☐ | ☐ |
| 23 | GCD | ☐ | ☐ |
| 24 | Armstrong Number | ☐ | ☐ |

---
