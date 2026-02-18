# 🔥 Interview Practice Questions — Medium Level
> **Topics:** Arrays · 2D Arrays · Strings · Basic Math  
> **Level:** Medium
> **Goal:** Crack real interview rounds with pattern-based thinking

---

## 📌 How to Use This Sheet
- Read the problem + constraints carefully before coding
- Identify the pattern (sliding window, two pointer, hashing, etc.)
- Write brute force first, then optimize
- Always mention TC and SC after your solution
- Preferred language: **JavaScript**

---

# 📂 SECTION 1 — ARRAYS (1D)

---

### Q1. Two Sum

**Definition:**  
Given an array of integers and a target value, return the **indices** of the two numbers that add up to the target. Assume exactly one solution exists and you cannot use the same element twice.

**Example:**
```
Input:  nums = [2, 7, 11, 15], target = 9
Output: [0, 1]   (nums[0] + nums[1] = 2 + 7 = 9)

Input:  nums = [3, 2, 4], target = 6
Output: [1, 2]
```

**Constraints:**
- Each input has exactly one solution
- Cannot use the same index twice
- Brute force: O(n²) → optimize using HashMap to O(n)

**TC:** O(n) | **SC:** O(n)

---

### Q2. Best Time to Buy and Sell Stock

**Definition:**  
Given an array `prices` where `prices[i]` is the price of a stock on day `i`, return the **maximum profit** you can achieve by buying on one day and selling on a later day. If no profit is possible, return `0`.

**Example:**
```
Input:  [7, 1, 5, 3, 6, 4]
Output: 5   (buy at 1, sell at 6)

Input:  [7, 6, 4, 3, 1]
Output: 0   (prices only go down, no profit)
```

**Constraints:**
- You must buy before you sell
- Only one transaction allowed
- Track minimum price seen so far

**TC:** O(n) | **SC:** O(1)

---

### Q3. Maximum Subarray Sum (Kadane's Algorithm)

**Definition:**  
Given an array of integers (can include negatives), find the contiguous subarray that has the **largest sum** and return that sum.

**Example:**
```
Input:  [-2, 1, -3, 4, -1, 2, 1, -5, 4]
Output: 6   (subarray: [4, -1, 2, 1])

Input:  [1]
Output: 1
```

**Constraints:**
- Array has at least one element
- Elements can be negative
- Classic Kadane's Algorithm problem

**TC:** O(n) | **SC:** O(1)

---

### Q4. Find Missing Number in Array (0 to N)

**Definition:**  
Given an array containing `n` distinct numbers in the range `[0, n]`, find the **one number that is missing**.

**Example:**
```
Input:  [3, 0, 1]
Output: 2

Input:  [9,6,4,2,3,5,7,0,1]
Output: 8
```

**Constraints:**
- Array has `n` elements, range is `[0, n]`
- Use math formula: sum of `n` numbers = `n*(n+1)/2`
- XOR approach also works

**TC:** O(n) | **SC:** O(1)

---

### Q5. Subarray with Given Sum (Sliding Window)

**Definition:**  
Given an array of **non-negative** integers and a target sum `S`, find if there exists a contiguous subarray whose sum equals `S`. Return `true`/`false`, or return the start and end indices.

**Example:**
```
Input:  arr = [1, 4, 20, 3, 10, 5], S = 33
Output: true  (subarray [20, 3, 10])

Input:  arr = [1, 2, 3, 4, 5], S = 9
Output: true  (subarray [2, 3, 4])
```

**Constraints:**
- Array contains only non-negative integers
- Use sliding window technique (two pointers)

**TC:** O(n) | **SC:** O(1)

---

### Q6. Merge Two Sorted Arrays

**Definition:**  
Given two sorted arrays, merge them into a single sorted array and return it.

**Example:**
```
Input:  arr1 = [1, 3, 5], arr2 = [2, 4, 6]
Output: [1, 2, 3, 4, 5, 6]

Input:  arr1 = [1, 2, 3], arr2 = []
Output: [1, 2, 3]
```

**Constraints:**
- Both arrays are sorted in ascending order
- Do not use `.sort()` on combined array
- Use two pointer technique

**TC:** O(n + m) | **SC:** O(n + m)

---

### Q7. Container With Most Water

**Definition:**  
Given an array `height` where each element represents the height of a vertical line at position `i`, find two lines that together with the x-axis form a container that holds the **most water**. Return the maximum water volume.

**Example:**
```
Input:  height = [1, 8, 6, 2, 5, 4, 8, 3, 7]
Output: 49

Input:  height = [1, 1]
Output: 1
```

**Constraints:**
- Water = `min(height[l], height[r]) × (r - l)`
- Use two pointer approach (start from both ends)
- Move the pointer with the smaller height inward

**TC:** O(n) | **SC:** O(1)

---

### Q8. Product of Array Except Self

**Definition:**  
Given an array, return a new array `result` where `result[i]` is the product of all elements in the array **except** `nums[i]`. Do not use division.

**Example:**
```
Input:  [1, 2, 3, 4]
Output: [24, 12, 8, 6]

Input:  [-1, 1, 0, -3, 3]
Output: [0, 0, 9, 0, 0]
```

**Constraints:**
- **Cannot use division operator**
- Use prefix and suffix product arrays

**TC:** O(n) | **SC:** O(n)

---

### Q9. Longest Consecutive Sequence

**Definition:**  
Given an unsorted array of integers, return the **length of the longest consecutive sequence** (elements in a row like 1,2,3,4).

**Example:**
```
Input:  [100, 4, 200, 1, 3, 2]
Output: 4   (sequence: 1, 2, 3, 4)

Input:  [0, 3, 7, 2, 5, 8, 4, 6, 0, 1]
Output: 9
```

**Constraints:**
- Sequence elements don't need to be contiguous in the array
- Use a Set for O(1) lookups
- Only start counting from the beginning of a sequence

**TC:** O(n) | **SC:** O(n)

---

### Q10. 3Sum — Find All Triplets with Zero Sum

**Definition:**  
Given an array of integers, find all **unique triplets** `[a, b, c]` such that `a + b + c = 0`.

**Example:**
```
Input:  [-1, 0, 1, 2, -1, -4]
Output: [[-1, -1, 2], [-1, 0, 1]]

Input:  [0, 0, 0]
Output: [[0, 0, 0]]
```

**Constraints:**
- Result must not contain duplicate triplets
- Sort the array first, then use two pointers
- Skip duplicate elements during traversal

**TC:** O(n²) | **SC:** O(1) (output space not counted)

---

# 📂 SECTION 2 — 2D ARRAYS (MATRIX)

---

### Q11. Transpose of a Matrix

**Definition:**  
Given an `n × m` matrix, return its **transpose** — where rows become columns and columns become rows. Element at `[i][j]` moves to `[j][i]`.

**Example:**
```
Input:
[
  [1, 2, 3],
  [4, 5, 6],
  [7, 8, 9]
]

Output:
[
  [1, 4, 7],
  [2, 5, 8],
  [3, 6, 9]
]
```

**Constraints:**
- Matrix can be non-square (`n × m`)
- Create a new matrix for non-square; swap in-place for square

**TC:** O(n × m) | **SC:** O(n × m)

---

### Q12. Rotate Matrix 90 Degrees Clockwise

**Definition:**  
Given an `n × n` square matrix, rotate it **90 degrees clockwise** in-place.

**Example:**
```
Input:
[
  [1, 2, 3],
  [4, 5, 6],
  [7, 8, 9]
]

Output:
[
  [7, 4, 1],
  [8, 5, 2],
  [9, 6, 3]
]
```

**Approach:**
1. Transpose the matrix
2. Reverse each row

**Constraints:**
- Must be done **in-place** (no extra matrix)
- Only for square matrices (n × n)

**TC:** O(n²) | **SC:** O(1)

---

### Q13. Search in a Row-wise and Column-wise Sorted Matrix

**Definition:**  
Given an `n × m` matrix where each row is sorted left to right and each column is sorted top to bottom, check if a given target value exists in the matrix. Return `true` or `false`.

**Example:**
```
Input:
matrix = [
  [1,  4,  7,  11],
  [2,  5,  8,  12],
  [3,  6,  9,  16],
  [10, 13, 14, 17]
]
target = 5
Output: true

target = 20
Output: false
```

**Approach:**
- Start from top-right corner
- If current > target → move left
- If current < target → move down

**TC:** O(n + m) | **SC:** O(1)

---

### Q14. Spiral Order Traversal of a Matrix

**Definition:**  
Given an `m × n` matrix, return all elements in **spiral order** (clockwise from outside to inside).

**Example:**
```
Input:
[
  [1,  2,  3],
  [4,  5,  6],
  [7,  8,  9]
]

Output: [1, 2, 3, 6, 9, 8, 7, 4, 5]
```

**Constraints:**
- Use four boundary pointers: top, bottom, left, right
- Shrink boundaries after each direction pass

**TC:** O(n × m) | **SC:** O(n × m)

---

### Q15. Find the Diagonal Sum of a Matrix

**Definition:**  
Given a square matrix of size `n × n`, return the sum of elements on the **primary diagonal** (top-left to bottom-right) and **secondary diagonal** (top-right to bottom-left). If `n` is odd, do not double-count the center element.

**Example:**
```
Input:
[
  [1, 2, 3],
  [4, 5, 6],
  [7, 8, 9]
]

Output: 25
Explanation: Primary [1,5,9] + Secondary [3,5,7] = 25 (5 counted once)
```

**Constraints:**
- `n × n` square matrix
- Center element counted only once when `n` is odd

**TC:** O(n) | **SC:** O(1)

---

### Q16. Set Matrix Zeroes

**Definition:**  
Given an `m × n` matrix, if any element is `0`, set its **entire row and column** to `0`. Do this in-place.

**Example:**
```
Input:
[
  [1, 1, 1],
  [1, 0, 1],
  [1, 1, 1]
]

Output:
[
  [1, 0, 1],
  [0, 0, 0],
  [1, 0, 1]
]
```

**Constraints:**
- Don't change rows/columns as you scan (mark first, then update)
- Brute: use extra boolean arrays → Optimize to O(1) space using first row/column as markers

**TC:** O(m × n) | **SC:** O(1) optimized

---

# 📂 SECTION 3 — STRINGS

---

### Q18. Longest Substring Without Repeating Characters

**Definition:**  
Given a string, find the length of the **longest substring** that contains no repeating characters.

**Example:**
```
Input:  "abcabcbb"
Output: 3   (substring: "abc")

Input:  "bbbbb"
Output: 1   (substring: "b")

Input:  "pwwkew"
Output: 3   (substring: "wke")
```

**Approach:**  
Use sliding window + a Set or HashMap to track characters in current window.

**TC:** O(n) | **SC:** O(min(n, 26)) ≈ O(1)

---

### Q19. Longest Palindromic Substring

**Definition:**  
Given a string, return the **longest substring** that is a palindrome.

**Example:**
```
Input:  "babad"
Output: "bab"  (or "aba")

Input:  "cbbd"
Output: "bb"
```

**Approach:**  
Expand around center — for each character (and pair), expand outward while palindrome holds.

**TC:** O(n²) | **SC:** O(1)

---

### Q20. Group Anagrams Together

**Definition:**  
Given an array of strings, group all **anagrams** together and return them as a list of lists.

**Example:**
```
Input:  ["eat","tea","tan","ate","nat","bat"]
Output: [["bat"],["nat","tan"],["ate","eat","tea"]]
```

**Approach:**  
Sort each string → use it as a HashMap key → group by same key.

**Constraints:**
- All strings contain lowercase English letters
- Order of groups doesn't matter

**TC:** O(n × k log k) where k = max string length | **SC:** O(n × k)

---

### Q21. Valid Parentheses

**Definition:**  
Given a string of just brackets (`(`, `)`, `{`, `}`, `[`, `]`), determine if the brackets are **valid** — every open bracket is closed in the correct order.

**Example:**
```
Input:  "()"
Output: true

Input:  "()[]{}"
Output: true

Input:  "(]"
Output: false

Input:  "([)]"
Output: false
```

**Approach:**  
Use a Stack. Push opening brackets, pop and match when a closing bracket appears.

**TC:** O(n) | **SC:** O(n)

---

### Q22. Minimum Window Substring

**Definition:**  
Given strings `s` and `t`, return the **minimum length substring** of `s` that contains all characters of `t` (including duplicates). If no such window exists, return `""`.

**Example:**
```
Input:  s = "ADOBECODEBANC", t = "ABC"
Output: "BANC"

Input:  s = "a", t = "a"
Output: "a"

Input:  s = "a", t = "aa"
Output: ""
```

**Approach:**  
Sliding window with two frequency maps. Expand right pointer, shrink left when all characters are covered.

**TC:** O(n + m) | **SC:** O(n + m)

---

### Q23. String Compression

**Definition:**  
Given a string, compress it using the **counts of repeated characters**. If the compressed string is not smaller than the original, return the original string.

**Example:**
```
Input:  "aabcccccaaa"
Output: "a2b1c5a3"

Input:  "abc"
Output: "abc"   (compressed "a1b1c1" is longer)
```

**Constraints:**
- Lowercase letters only
- If compressed length ≥ original, return original

**TC:** O(n) | **SC:** O(n)

---

# 📂 SECTION 4 — BASIC MATH (MEDIUM)

---

### Q24. Power Function (Fast Exponentiation)

**Definition:**  
Implement `pow(x, n)` — raise `x` to the power `n`. Do **not** use built-in `Math.pow()`. Handle negative exponents.

**Example:**
```
Input:  x = 2.0, n = 10
Output: 1024.0

Input:  x = 2.0, n = -2
Output: 0.25   (= 1 / 2² = 1/4)
```

**Approach:**  
Use **Binary Exponentiation** (fast power):  
- If `n` is even: `pow(x, n) = pow(x*x, n/2)`  
- If `n` is odd: `pow(x, n) = x * pow(x, n-1)`

**TC:** O(log n) | **SC:** O(log n)

---

### Q25. Find All Prime Numbers up to N (Sieve of Eratosthenes)

**Definition:**  
Given a number `n`, return all prime numbers from `2` to `n` using the **Sieve of Eratosthenes**.

**Example:**
```
Input:  n = 20
Output: [2, 3, 5, 7, 11, 13, 17, 19]

Input:  n = 10
Output: [2, 3, 5, 7]
```

**Approach:**
1. Create a boolean array of size `n+1`, initialized to `true`
2. Mark multiples of each prime as `false` starting from `p²`

**TC:** O(n log log n) | **SC:** O(n)

---

### Q26. Count Number of Trailing Zeros in Factorial

**Definition:**  
Given `n`, find the number of **trailing zeros** in `n!` (n factorial). Trailing zeros come from factors of 10 = 2 × 5. Count how many times 5 divides into `n!`.

**Example:**
```
Input:  5
Output: 1   (5! = 120 → one trailing zero)

Input:  25
Output: 6
```

**Formula:**  
`count = floor(n/5) + floor(n/25) + floor(n/125) + ...`

**TC:** O(log n) | **SC:** O(1)

---

### Q27. Find LCM of Two Numbers

**Definition:**  
Given two positive integers, return their **Least Common Multiple** (LCM) — the smallest number that is divisible by both.

**Example:**
```
Input:  12, 18
Output: 36

Input:  4, 6
Output: 12
```

**Formula:**  
`LCM(a, b) = (a × b) / GCD(a, b)`  
Use Euclidean algorithm for GCD first.

**TC:** O(log(min(a,b))) | **SC:** O(1)

---

### Q28. Check if a Number is a Perfect Number

**Definition:**  
A **perfect number** is a positive integer equal to the sum of its proper divisors (divisors excluding itself). Return `true` or `false`.

**Example:**
```
Input:  28
Output: true   (divisors: 1+2+4+7+14 = 28)

Input:  6
Output: true   (divisors: 1+2+3 = 6)

Input:  12
Output: false  (divisors: 1+2+3+4+6 = 16 ≠ 12)
```

**Constraints:**
- Loop only up to `√n` to find divisors efficiently

**TC:** O(√n) | **SC:** O(1)

---

### Q29. Excel Column Number (Letter to Number)

**Definition:**  
Given a column title as it appears in an Excel spreadsheet (A=1, B=2, ..., Z=26, AA=27, AB=28...), return its corresponding column number.

**Example:**
```
Input:  "A"
Output: 1

Input:  "AB"
Output: 28

Input:  "ZY"
Output: 701
```

**Approach:**  
Treat it like base-26 number conversion.  
`result = result * 26 + (char - 'A' + 1)`

**TC:** O(n) | **SC:** O(1)

---

## 🎯 Pattern Cheat Sheet

| Pattern | Used In |
|---|---|
| **Two Pointers** | Two Sum (sorted), Container Water, 3Sum, Merge Sorted Arrays |
| **Sliding Window** | Longest Substring, Subarray with Sum, Minimum Window |
| **HashMap / Set** | Two Sum, Group Anagrams, Longest Consecutive |
| **Kadane's Algorithm** | Maximum Subarray Sum |
| **Stack** | Valid Parentheses |
| **Prefix / Suffix** | Product Except Self |
| **Expand Around Center** | Longest Palindromic Substring |
| **Sieve** | All Primes up to N |
| **Binary Exponentiation** | Fast Power |

---

## 🏁 Quick Complexity Reminder

| Complexity | When to Expect |
|---|---|
| O(1) | Math tricks, formula-based |
| O(log n) | Binary search, fast exponentiation |
| O(n) | Single pass, sliding window |
| O(n log n) | Sorting-based problems |
| O(n²) | Two nested loops, brute force |
| O(m × n) | Matrix traversal |

---

## ✅ Progress Tracker

| # | Problem | Pattern | Solved | Reviewed |
|---|---------|---------|--------|----------|
| 1 | Two Sum | HashMap | ☐ | ☐ |
| 2 | Best Time to Buy & Sell Stock | Greedy | ☐ | ☐ |
| 3 | Maximum Subarray Sum | Kadane's | ☐ | ☐ |
| 4 | Missing Number | Math/XOR | ☐ | ☐ |
| 5 | Subarray with Given Sum | Sliding Window | ☐ | ☐ |
| 6 | Merge Two Sorted Arrays | Two Pointers | ☐ | ☐ |
| 7 | Container With Most Water | Two Pointers | ☐ | ☐ |
| 8 | Product Except Self | Prefix/Suffix | ☐ | ☐ |
| 9 | Longest Consecutive Sequence | HashSet | ☐ | ☐ |
| 10 | 3Sum | Sort + Two Pointers | ☐ | ☐ |
| 11 | Transpose of Matrix | 2D Array | ☐ | ☐ |
| 12 | Rotate Matrix 90° | 2D Array | ☐ | ☐ |
| 13 | Search in Sorted Matrix | Two Pointers | ☐ | ☐ |
| 14 | Spiral Order Traversal | 2D Array | ☐ | ☐ |
| 15 | Diagonal Sum | 2D Array | ☐ | ☐ |
| 16 | Set Matrix Zeroes | 2D Array | ☐ | ☐ |
| 18 | Longest Substring No Repeat | Sliding Window | ☐ | ☐ |
| 19 | Longest Palindromic Substring | Expand Center | ☐ | ☐ |
| 20 | Group Anagrams | HashMap | ☐ | ☐ |
| 21 | Valid Parentheses | Stack | ☐ | ☐ |
| 22 | Minimum Window Substring | Sliding Window | ☐ | ☐ |
| 23 | String Compression | Two Pointers | ☐ | ☐ |
| 24 | Fast Power (x^n) | Binary Exponentiation | ☐ | ☐ |
| 25 | Sieve of Eratosthenes | Math | ☐ | ☐ |
| 26 | Trailing Zeros in Factorial | Math | ☐ | ☐ |
| 27 | LCM of Two Numbers | Math/GCD | ☐ | ☐ |
| 28 | Perfect Number | Math | ☐ | ☐ |
| 29 | Excel Column Number | Base Conversion | ☐ | ☐ |

---
