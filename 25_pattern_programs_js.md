# 25+ Pattern Programs - Complete JavaScript Solutions
## All Famous Patterns with Full Code, Complexity & Intuition

---

## 🎯 Why Should You Complete This?

**Pattern problems are the foundation of programming skills. Here's why you must master them:**

### 1. **Master Nested Loops**
- Nested loops are used in 90% of real-world problems
- Understanding patterns helps you visualize loop behavior
- Build confidence with iteration concepts

### 2. **Improve Logical Thinking**
- Patterns force you to think step-by-step
- Develop problem-solving approach
- Learn to break complex problems into smaller parts

### 3. **Code Optimization Skills**
- Learn Time & Space Complexity analysis
- Understand how to write efficient code
- Practice optimization techniques

### 4. **Interview Preparation**
- Interviewers love testing with pattern problems
- Shows your basic programming strength
- Quick gauge of your coding fundamentals
- Confidence builder for technical interviews

### 5. **Build Programming Intuition**
- Learn to visualize output before coding
- Develop mental models for algorithms
- Understand spacing, alignment, and boundaries
- Critical thinking about edge cases

### 6. **Real-World Applications**
- Matrix operations (Image processing)
- Grid-based games (Chess, Sudoku)
- Data visualization
- UI rendering logic
- Algorithm design foundations

### 7. **Speed & Accuracy**
- Solve similar problems faster after practice
- Reduce debugging time
- Write cleaner, more readable code
- Better code quality overall

### 8. **Foundation for Advanced DSA**
- Before learning Trees, Graphs, Dynamic Programming
- Pattern mastery is the prerequisite
- Easy to hard progression ensures strong foundation
- Confidence to tackle complex algorithms

**💪 Bottom Line:** Master patterns = Master programming fundamentals = Crack interviews = Build real applications

---

## PATTERN 1: Simple Star Triangle

**Problem Statement:**
Print a triangle of stars where row i contains i stars.

**Input/Output:**
```
Input: 5
Output:
*
* *
* * *
* * * *
* * * * *
```

**Code with Intuition:**

```javascript
function simpleStarTriangle(n) {
    // INTUITION:
    // - Outer loop: iterate for n rows
    // - Inner loop: print stars equal to row number
    // - Each row has i stars
    
    for (let i = 1; i <= n; i++) {
        let row = "";
        for (let j = 1; j <= i; j++) {
            row += "* ";
        }
        console.log(row.trim());
    }
}

simpleStarTriangle(5);
```

**Time Complexity:** O(N²) - Outer loop N times, inner loop 1 to N times
**Space Complexity:** O(1) - No extra data structure (excluding output)

---

## PATTERN 2: Inverted Star Triangle

**Problem Statement:**
Print inverted triangle where top has N stars and decreases.

**Input/Output:**
```
Input: 5
Output:
* * * * *
* * * *
* * *
* *
*
```

**Code:**

```javascript
function invertedStarTriangle(n) {
    // INTUITION:
    // - Start from n and go down to 1
    // - Outer loop: n down to 1
    // - Inner loop: j stars for current i value
    
    for (let i = n; i >= 1; i--) {
        let row = "";
        for (let j = 1; j <= i; j++) {
            row += "* ";
        }
        console.log(row.trim());
    }
}

invertedStarTriangle(5);
```

**Time Complexity:** O(N²)
**Space Complexity:** O(1)

---

## PATTERN 3: Number Triangle

**Problem Statement:**
Print triangle where row i contains numbers 1 to i.

**Input/Output:**
```
Input: 4
Output:
1
1 2
1 2 3
1 2 3 4
```

**Code:**

```javascript
function numberTriangle(n) {
    // INTUITION:
    // - Same as star triangle but print numbers
    // - Numbers increment from 1 to i in each row
    
    for (let i = 1; i <= n; i++) {
        let row = "";
        for (let j = 1; j <= i; j++) {
            row += j + " ";
        }
        console.log(row.trim());
    }
}

numberTriangle(4);
```

**Time Complexity:** O(N²)
**Space Complexity:** O(1)

---

## PATTERN 4: Inverted Number Triangle

**Problem Statement:**
Print inverted number triangle.

**Input/Output:**
```
Input: 4
Output:
1 2 3 4
1 2 3
1 2
1
```

**Code:**

```javascript
function invertedNumberTriangle(n) {
    // INTUITION:
    // - Outer loop: n down to 1
    // - Inner loop: 1 to i for each row
    
    for (let i = n; i >= 1; i--) {
        let row = "";
        for (let j = 1; j <= i; j++) {
            row += j + " ";
        }
        console.log(row.trim());
    }
}

invertedNumberTriangle(4);
```

**Time Complexity:** O(N²)
**Space Complexity:** O(1)

---

## PATTERN 5: Number Pyramid (Left Aligned)

**Problem Statement:**
Print pyramid with numbers 1 to i in row i.

**Input/Output:**
```
Input: 5
Output:
1
2 3
4 5 6
7 8 9 10
11 12 13 14 15
```

**Code:**

```javascript
function numberPyramidSequence(n) {
    // INTUITION:
    // - Maintain a counter that increments globally
    // - Each row has i numbers
    // - Numbers continue sequentially
    
    let counter = 1;
    for (let i = 1; i <= n; i++) {
        let row = "";
        for (let j = 1; j <= i; j++) {
            row += counter + " ";
            counter++;
        }
        console.log(row.trim());
    }
}

numberPyramidSequence(5);
```

**Time Complexity:** O(N²) - Total N(N+1)/2 numbers printed
**Space Complexity:** O(1)

---

## PATTERN 6: Floyd's Triangle

**Problem Statement:**
Print Floyd's triangle with sequential numbers.

**Input/Output:**
```
Input: 5
Output:
1
2 3
4 5 6
7 8 9 10
11 12 13 14 15
```

**Code:**

```javascript
function floydsTriangle(n) {
    // INTUITION:
    // - Counter starts at 1
    // - Row i has i numbers
    // - Numbers increment sequentially
    // (Same as Pattern 5 - classic Floyd's Triangle)
    
    let counter = 1;
    for (let i = 1; i <= n; i++) {
        let row = "";
        for (let j = 1; j <= i; j++) {
            row += counter + " ";
            counter++;
        }
        console.log(row.trim());
    }
}

floydsTriangle(5);
```

**Time Complexity:** O(N²)
**Space Complexity:** O(1)

---

## PATTERN 7: Star Pyramid (Center Aligned)

**Problem Statement:**
Print centered pyramid with stars.

**Input/Output:**
```
Input: 5
Output:
    *
   * *
  * * *
 * * * *
* * * * *
```

**Code:**

```javascript
function starPyramid(n) {
    // INTUITION:
    // - Add leading spaces: n-i for row i
    // - Then print i stars
    // - Spaces control center alignment
    
    for (let i = 1; i <= n; i++) {
        let spaces = " ".repeat(n - i);
        let stars = "* ".repeat(i);
        console.log(spaces + stars.trim());
    }
}

starPyramid(5);
```

**Time Complexity:** O(N²)
**Space Complexity:** O(N) - String length up to 2N

---

## PATTERN 8: Diamond Pattern

**Problem Statement:**
Print diamond shape with stars.

**Input/Output:**
```
Input: 5
Output:
  *
 * *
* * *
 * *
  *
```

**Code:**

```javascript
function diamondPattern(n) {
    // INTUITION:
    // - Upper half: spaces decrease, stars increase
    // - Lower half: reverse of upper
    // - Creates diamond shape
    
    let mid = Math.ceil(n / 2);
    
    // Upper half
    for (let i = 1; i <= mid; i++) {
        let spaces = " ".repeat(mid - i);
        let stars = "* ".repeat(i);
        console.log(spaces + stars.trim());
    }
    
    // Lower half
    for (let i = mid - 1; i >= 1; i--) {
        let spaces = " ".repeat(mid - i);
        let stars = "* ".repeat(i);
        console.log(spaces + stars.trim());
    }
}

diamondPattern(5);
```

**Time Complexity:** O(N²)
**Space Complexity:** O(N)

---

## PATTERN 9: Hollow Rectangle

**Problem Statement:**
Print hollow rectangle with stars.

**Input/Output:**
```
Input: 4 6
Output:
* * * * * *
*         *
*         *
* * * * * *
```

**Code:**

```javascript
function hollowRectangle(rows, cols) {
    // INTUITION:
    // - First/last row: all stars
    // - Middle rows: stars at start and end only
    // - Creates hollow effect
    
    for (let i = 1; i <= rows; i++) {
        let row = "";
        for (let j = 1; j <= cols; j++) {
            // Print star at border positions
            if (i === 1 || i === rows || j === 1 || j === cols) {
                row += "* ";
            } else {
                row += "  ";
            }
        }
        console.log(row.trim());
    }
}

hollowRectangle(4, 6);
```

**Time Complexity:** O(rows × cols)
**Space Complexity:** O(cols)

---

## PATTERN 10: Hollow Diamond

**Problem Statement:**
Print hollow diamond pattern.

**Input/Output:**
```
Input: 5
Output:
    *
   * *
  *   *
 *     *
*       *
 *     *
  *   *
   * *
    *
```

**Code:**

```javascript
function hollowDiamond(n) {
    // INTUITION:
    // - Upper half: spaces and stars only at edges
    // - Lower half: reverse of upper
    // - Middle spacing increases then decreases
    
    let mid = Math.ceil(n / 2);
    
    // Upper half
    for (let i = 1; i <= mid; i++) {
        let spaces = " ".repeat(mid - i);
        let middleSpace = i === 1 ? "" : " ".repeat(2 * i - 3);
        
        if (i === 1) {
            console.log(spaces + "*");
        } else {
            console.log(spaces + "*" + middleSpace + "*");
        }
    }
    
    // Lower half
    for (let i = mid - 1; i >= 1; i--) {
        let spaces = " ".repeat(mid - i);
        let middleSpace = i === 1 ? "" : " ".repeat(2 * i - 3);
        
        if (i === 1) {
            console.log(spaces + "*");
        } else {
            console.log(spaces + "*" + middleSpace + "*");
        }
    }
}

hollowDiamond(5);
```

**Time Complexity:** O(N²)
**Space Complexity:** O(N)

---

## PATTERN 11: Butterfly Pattern

**Problem Statement:**
Print butterfly shape.

**Input/Output:**
```
Input: 5
Output:
*       *
* *   * *
* * * * *
* *   * *
*       *
```

**Code:**

```javascript
function butterflyPattern(n) {
    // INTUITION:
    // - Left side: stars increasing
    // - Middle: spaces decreasing then increasing
    // - Right side: mirror of left
    // - Creates butterfly symmetry
    
    for (let i = 1; i <= n; i++) {
        let left = "* ".repeat(i).trim();
        let middle = " ".repeat(2 * (n - i));
        let right = "* ".repeat(i).trim();
        console.log(left + middle + right);
    }
    
    for (let i = n - 1; i >= 1; i--) {
        let left = "* ".repeat(i).trim();
        let middle = " ".repeat(2 * (n - i));
        let right = "* ".repeat(i).trim();
        console.log(left + middle + right);
    }
}

butterflyPattern(5);
```

**Time Complexity:** O(N²)
**Space Complexity:** O(N)

---

## PATTERN 12: Pascal's Triangle

**Problem Statement:**
Print Pascal's triangle where each element is sum of two above.

**Input/Output:**
```
Input: 6
Output:
     1
    1 1
   1 2 1
  1 3 3 1
 1 4 6 4 1
1 5 10 10 5 1
```

**Code:**

```javascript
function pascalsTriangle(n) {
    // INTUITION:
    // - Build 2D array storing values
    // - Each element: triangle[i][j] = triangle[i-1][j-1] + triangle[i-1][j]
    // - First and last of each row is 1
    // - Add spaces for center alignment
    
    let triangle = [];
    
    for (let i = 0; i < n; i++) {
        triangle[i] = [];
        
        for (let j = 0; j <= i; j++) {
            if (j === 0 || j === i) {
                triangle[i][j] = 1;
            } else {
                triangle[i][j] = triangle[i - 1][j - 1] + triangle[i - 1][j];
            }
        }
        
        // Print with spaces
        let spaces = " ".repeat(n - i - 1);
        let row = triangle[i].join(" ");
        console.log(spaces + row);
    }
}

pascalsTriangle(6);
```

**Time Complexity:** O(N²)
**Space Complexity:** O(N²)

---

## PATTERN 13: Alphabet Triangle

**Problem Statement:**
Print triangle with alphabets.

**Input/Output:**
```
Input: 5
Output:
A
A B
A B C
A B C D
A B C D E
```

**Code:**

```javascript
function alphabetTriangle(n) {
    // INTUITION:
    // - Convert number to character using ASCII
    // - A = 65, B = 66, etc
    // - Row i contains A to character[i]
    
    for (let i = 0; i < n; i++) {
        let row = "";
        for (let j = 0; j <= i; j++) {
            row += String.fromCharCode(65 + j) + " ";
        }
        console.log(row.trim());
    }
}

alphabetTriangle(5);
```

**Time Complexity:** O(N²)
**Space Complexity:** O(1)

---

## PATTERN 14: Inverted Alphabet Triangle

**Problem Statement:**
Print inverted alphabet triangle.

**Input/Output:**
```
Input: 5
Output:
A B C D E
A B C D
A B C
A B
A
```

**Code:**

```javascript
function invertedAlphabetTriangle(n) {
    // INTUITION:
    // - Outer loop from n to 1
    // - Inner loop prints A to character[i]
    
    for (let i = n; i >= 1; i--) {
        let row = "";
        for (let j = 0; j < i; j++) {
            row += String.fromCharCode(65 + j) + " ";
        }
        console.log(row.trim());
    }
}

invertedAlphabetTriangle(5);
```

**Time Complexity:** O(N²)
**Space Complexity:** O(1)

---

## PATTERN 15: Alphabet Pyramid

**Problem Statement:**
Print centered alphabet pyramid.

**Input/Output:**
```
Input: 5
Output:
    A
   A B
  A B C
 A B C D
A B C D E
```

**Code:**

```javascript
function alphabetPyramid(n) {
    // INTUITION:
    // - Add leading spaces
    // - Print A to character[i]
    // - Spaces decrease, letters increase
    
    for (let i = 0; i < n; i++) {
        let spaces = " ".repeat(n - i - 1);
        let chars = "";
        for (let j = 0; j <= i; j++) {
            chars += String.fromCharCode(65 + j) + " ";
        }
        console.log(spaces + chars.trim());
    }
}

alphabetPyramid(5);
```

**Time Complexity:** O(N²)
**Space Complexity:** O(N)

---

## PATTERN 16: Square Pattern (Solid)

**Problem Statement:**
Print solid square with numbers.

**Input/Output:**
```
Input: 4
Output:
1 2 3 4
5 6 7 8
9 10 11 12
13 14 15 16
```

**Code:**

```javascript
function solidSquare(n) {
    // INTUITION:
    // - Nested loops for n×n grid
    // - Counter increments for each position
    
    let counter = 1;
    for (let i = 0; i < n; i++) {
        let row = "";
        for (let j = 0; j < n; j++) {
            row += counter + " ";
            counter++;
        }
        console.log(row.trim());
    }
}

solidSquare(4);
```

**Time Complexity:** O(N²)
**Space Complexity:** O(1)

---

## PATTERN 17: Square Pattern (Boundary)

**Problem Statement:**
Print square with only boundary.

**Input/Output:**
```
Input: 4
Output:
1 2 3 4
5     8
9     12
13 14 15 16
```

**Code:**

```javascript
function boundarySquare(n) {
    // INTUITION:
    // - Print number only at boundaries
    // - Outer cells (i==1, i==n, j==1, j==n) print value
    // - Others print spaces
    
    let counter = 1;
    for (let i = 1; i <= n; i++) {
        let row = "";
        for (let j = 1; j <= n; j++) {
            if (i === 1 || i === n || j === 1 || j === n) {
                row += counter + " ";
            } else {
                row += "  ";
            }
            counter++;
        }
        console.log(row.trim());
    }
}

boundarySquare(4);
```

**Time Complexity:** O(N²)
**Space Complexity:** O(1)

---

## PATTERN 18: Spiral Pattern

**Problem Statement:**
Print numbers in spiral order.

**Input/Output:**
```
Input: 4
Output:
1  2  3  4
12 13 14 5
11 16 15 6
10  9  8  7
```

**Code:**

```javascript
function spiralPattern(n) {
    // INTUITION:
    // - Create NxN matrix
    // - Fill by moving: right, down, left, up
    // - Track boundaries that shrink inward
    
    let matrix = Array(n).fill(null).map(() => Array(n).fill(0));
    
    let top = 0, bottom = n - 1, left = 0, right = n - 1;
    let num = 1;
    
    while (top <= bottom && left <= right) {
        // Move right
        for (let col = left; col <= right; col++) {
            matrix[top][col] = num++;
        }
        top++;
        
        // Move down
        for (let row = top; row <= bottom; row++) {
            matrix[row][right] = num++;
        }
        right--;
        
        // Move left
        if (top <= bottom) {
            for (let col = right; col >= left; col--) {
                matrix[bottom][col] = num++;
            }
            bottom--;
        }
        
        // Move up
        if (left <= right) {
            for (let row = bottom; row >= top; row--) {
                matrix[row][left] = num++;
            }
            left++;
        }
    }
    
    // Print matrix
    for (let i = 0; i < n; i++) {
        let row = "";
        for (let j = 0; j < n; j++) {
            row += matrix[i][j].toString().padStart(2, " ") + " ";
        }
        console.log(row);
    }
}

spiralPattern(4);
```

**Time Complexity:** O(N²)
**Space Complexity:** O(N²)

---

## PATTERN 19: Zigzag Pattern

**Problem Statement:**
Print numbers in zigzag diagonal order.

**Input/Output:**
```
Input: 4
Output:
1
2 3
4 5 6
7 8 9 10
11 12 13 14 15
...
```

**Code:**

```javascript
function zigzagPattern(n) {
    // INTUITION:
    // - Traverse diagonals
    // - Alternate direction for each diagonal
    // - Print diagonal values
    
    let counter = 1;
    let total = n * (n + 1) / 2;
    
    for (let diag = 0; diag < n; diag++) {
        if (counter > total) break;
        
        if (diag % 2 === 0) {
            // Go up-right
            for (let i = diag; i >= 0; i--) {
                console.log(counter++);
                if (counter > total) break;
            }
        } else {
            // Go down-left
            for (let i = 0; i <= diag; i++) {
                console.log(counter++);
                if (counter > total) break;
            }
        }
    }
}

zigzagPattern(4);
```

**Time Complexity:** O(N²)
**Space Complexity:** O(1)

---

## PATTERN 20: Number Diamond

**Problem Statement:**
Print diamond with numbers.

**Input/Output:**
```
Input: 5
Output:
    1
   1 2 1
  1 2 3 2 1
 1 2 3 4 3 2 1
1 2 3 4 5 4 3 2 1
 1 2 3 4 3 2 1
  1 2 3 2 1
   1 2 1
    1
```

**Code:**

```javascript
function numberDiamond(n) {
    // INTUITION:
    // - Upper half: increasing numbers then decreasing
    // - Lower half: reverse of upper
    // - Add spaces for alignment
    
    let mid = Math.ceil(n / 2);
    
    // Upper half
    for (let i = 1; i <= mid; i++) {
        let spaces = " ".repeat(mid - i);
        let nums = "";
        
        // Increasing part
        for (let j = 1; j <= i; j++) {
            nums += j + " ";
        }
        
        // Decreasing part
        for (let j = i - 1; j >= 1; j--) {
            nums += j + " ";
        }
        
        console.log(spaces + nums.trim());
    }
    
    // Lower half
    for (let i = mid - 1; i >= 1; i--) {
        let spaces = " ".repeat(mid - i);
        let nums = "";
        
        for (let j = 1; j <= i; j++) {
            nums += j + " ";
        }
        
        for (let j = i - 1; j >= 1; j--) {
            nums += j + " ";
        }
        
        console.log(spaces + nums.trim());
    }
}

numberDiamond(5);
```

**Time Complexity:** O(N²)
**Space Complexity:** O(N)

---

## PATTERN 21: Hourglass Pattern

**Problem Statement:**
Print hourglass (two triangles meeting at a point).

**Input/Output:**
```
Input: 5
Output:
1 2 3 4 5
  2 3 4
    3
  2 3 4
1 2 3 4 5
```

**Code:**

```javascript
function hourglassPattern(n) {
    // INTUITION:
    // - Upper half: numbers decrease spacing, decrease range
    // - Middle: single number
    // - Lower half: reverse of upper
    
    // Upper half
    for (let i = 0; i < n; i++) {
        let spaces = " ".repeat(i);
        let nums = "";
        
        for (let j = i + 1; j < n; j++) {
            nums += j + " ";
        }
        for (let j = n - 1; j > i; j--) {
            nums += j + " ";
        }
        
        console.log(spaces + nums.trim());
    }
    
    // Lower half
    for (let i = n - 2; i >= 0; i--) {
        let spaces = " ".repeat(i);
        let nums = "";
        
        for (let j = i + 1; j < n; j++) {
            nums += j + " ";
        }
        for (let j = n - 1; j > i; j--) {
            nums += j + " ";
        }
        
        console.log(spaces + nums.trim());
    }
}

hourglassPattern(5);
```

**Time Complexity:** O(N²)
**Space Complexity:** O(N)

---

## PATTERN 22: Fibonacci Series Pattern

**Problem Statement:**
Print Fibonacci series numbers.

**Input/Output:**
```
Input: 10
Output:
0 1 1 2 3 5 8 13 21 34
```

**Code:**

```javascript
function fibonacciSeries(n) {
    // INTUITION:
    // - F(0) = 0, F(1) = 1
    // - F(i) = F(i-1) + F(i-2)
    // - Generate n terms
    
    let a = 0, b = 1;
    let result = [a];
    
    for (let i = 1; i < n; i++) {
        result.push(b);
        let temp = b;
        b = a + b;
        a = temp;
    }
    
    console.log(result.join(" "));
}

fibonacciSeries(10);
```

**Time Complexity:** O(N)
**Space Complexity:** O(N)

---

## PATTERN 23: Prime Numbers Pattern

**Problem Statement:**
Print first N prime numbers.

**Input/Output:**
```
Input: 10
Output:
2 3 5 7 11 13 17 19 23 29
```

**Code:**

```javascript
function primeNumbers(n) {
    // INTUITION:
    // - Check each number for primality
    // - Count primes until we have n primes
    // - Prime: divisible only by 1 and itself
    
    function isPrime(num) {
        if (num < 2) return false;
        if (num === 2) return true;
        if (num % 2 === 0) return false;
        
        for (let i = 3; i * i <= num; i += 2) {
            if (num % i === 0) return false;
        }
        return true;
    }
    
    let primes = [];
    let num = 2;
    
    while (primes.length < n) {
        if (isPrime(num)) {
            primes.push(num);
        }
        num++;
    }
    
    console.log(primes.join(" "));
}

primeNumbers(10);
```

**Time Complexity:** O(N × √M) - N primes, M is Nth prime
**Space Complexity:** O(N)

---

## PATTERN 24: Number Pattern (Odd-Even)

**Problem Statement:**
Print pattern with odd and even numbers.

**Input/Output:**
```
Input: 5
Output:
1
2 3
4 5 6
7 8 9 10
11 12 13 14 15
```

**Code:**

```javascript
function numberPatternSequence(n) {
    // INTUITION:
    // - Counter continues throughout pattern
    // - Row i has i numbers
    // - Numbers increase sequentially
    
    let counter = 1;
    for (let i = 1; i <= n; i++) {
        let row = "";
        for (let j = 1; j <= i; j++) {
            row += counter + " ";
            counter++;
        }
        console.log(row.trim());
    }
}

numberPatternSequence(5);
```

**Time Complexity:** O(N²)
**Space Complexity:** O(1)

---

## PATTERN 25: Reverse Number Pattern

**Problem Statement:**
Print pattern with reverse numbers.

**Input/Output:**
```
Input: 5
Output:
5
5 4
5 4 3
5 4 3 2
5 4 3 2 1
```

**Code:**

```javascript
function reverseNumberPattern(n) {
    // INTUITION:
    // - Row i prints numbers from n down to n-i+1
    // - Each row starts from n
    
    for (let i = 1; i <= n; i++) {
        let row = "";
        for (let j = n; j > n - i; j--) {
            row += j + " ";
        }
        console.log(row.trim());
    }
}

reverseNumberPattern(5);
```

**Time Complexity:** O(N²)
**Space Complexity:** O(1)

---

## SUMMARY TABLE

| # | Pattern | Complexity | Category |
|---|---------|-----------|----------|
| 1 | Simple Star Triangle | O(N²) | Basic |
| 2 | Inverted Star Triangle | O(N²) | Basic |
| 3 | Number Triangle | O(N²) | Basic |
| 4 | Inverted Number Triangle | O(N²) | Basic |
| 5 | Number Pyramid (Sequence) | O(N²) | Intermediate |
| 6 | Floyd's Triangle | O(N²) | Intermediate |
| 7 | Star Pyramid | O(N²) | Intermediate |
| 8 | Diamond Pattern | O(N²) | Intermediate |
| 9 | Hollow Rectangle | O(N×M) | Intermediate |
| 10 | Hollow Diamond | O(N²) | Intermediate |
| 11 | Butterfly Pattern | O(N²) | Advanced |
| 12 | Pascal's Triangle | O(N²) | Advanced |
| 13 | Alphabet Triangle | O(N²) | Basic |
| 14 | Inverted Alphabet Triangle | O(N²) | Basic |
| 15 | Alphabet Pyramid | O(N²) | Intermediate |
| 16 | Solid Square | O(N²) | Intermediate |
| 17 | Boundary Square | O(N²) | Intermediate |
| 18 | Spiral Pattern | O(N²) | Advanced |
| 19 | Zigzag Pattern | O(N²) | Advanced |
| 20 | Number Diamond | O(N²) | Advanced |
| 21 | Hourglass Pattern | O(N²) | Advanced |
| 22 | Fibonacci Series | O(N) | Mathematical |
| 23 | Prime Numbers | O(N×√M) | Mathematical |
| 24 | Sequential Number | O(N²) | Basic |
| 25 | Reverse Number | O(N²) | Basic |

---

## 📊 Quick Reference

**Test all patterns with:**
- n = 1 (edge case)
- n = 3 (small)
- n = 5 (standard)
- n = 10 (larger)

**When Testing Verify:**
1. Output format matches exactly
2. No trailing spaces
3. Correct spacing and alignment
4. Numbers/characters in right order
5. Boundary conditions work
