# [Algorithms](https://www.youtube.com/playlist?list=PLDN4rrl48XKpZkf03iYFl-O29szjTrs_O)

## Table of Contents
1. [Introduction to Algorithms](#1) [(Click for Video)](https://www.youtube.com/watch?v=0IAPZzGSbME&list=PLDN4rrl48XKpZkf03iYFl-O29szjTrs_O&index=1)
2. [Priori and Posteriori Testing](#2) [(Click for Video)](https://www.youtube.com/watch?v=0IAPZzGSbME&list=PLDN4rrl48XKpZkf03iYFl-O29szjTrs_O&index=2)
3. [Characteristics of Algorithms](#3) [(Click for Video)](https://www.youtube.com/watch?v=0IAPZzGSbME&list=PLDN4rrl48XKpZkf03iYFl-O29szjTrs_O&index=3)
4. [How to Write and Analyze Algorithms](#4) [(Click for Video)](https://www.youtube.com/watch?v=0IAPZzGSbME&list=PLDN4rrl48XKpZkf03iYFl-O29szjTrs_O&index=4)
5. [Frequency Count Method](#5) [(Click for Video)](https://www.youtube.com/watch?v=0IAPZzGSbME&list=PLDN4rrl48XKpZkf03iYFl-O29szjTrs_O&index=5)

## Introduction to Algorithms <a name="1"></a>
* Software Development Projects
   * Design Phase
      * Cannot create something on trial and error basis.
      * **Write in easy, english-like syntax.**
   * Implementation Phase
* Algorithms vs. Program
   1. Algorithms
      1. Written during the **design phase**.
      2. Written by someone with knowledge of subject. 
         1. Ex. statistician on EM algorithm
      3. Written in any language 
         1. English or mathematical notations.
         2. **Mathematical notations is best.**
      4. Hardware and software independent.
      5. Analyze and optimize for time and space.
   2. Programs
      1. Written during the **implementation phase**.
      2. Written by a programmer.
      3. Written in a programming language.
      4. Hardware and software dependent. 
         1. Questions like what OS will it run on and with what computer specs will need to be considered.
      5. Test it.

## Priori and Posteriori Testing <a name="2"></a>
* Priori Analysis
   * Algorithm
   * Hardware and language independent.
   * Time and space consumed.
* Posteriori Analysis
   * Program
    * Hardware and language dependent.
   * Watch time and memory usage.

## Characteristics of Algorithms <a name="3"></a>
1. Input
   1. Will take 0 or more inputs
2. Output
   1. Must generate 1 or more outputs
3. Definiteness
   1. Statement written must be unambiguous and clear.
   2. Ex. sqrt(-1) -> Imaginary (i)
4. Finiteness
   1. Must terminate at some point.
5. Effectiveness
   1. Statements should serve some purpose and move towards the output.

## How to Write and Analyze Algorithms <a name="4"></a>
Example:
```
algorithm swap(a, b) {
    temp = a;
    a = b,
    b = temp;
}
```
* C-like function
   * Don't worry about data-types or var declarations. Not important in algos.
* Time
   * How much time it is taking?
   * Should be time efficient.
   * In form of a function time.
* Space
   * How much memory/space it consumes.
* Data Transfer
   * Application running algorithm is web-based or network based. 
* Power Consumption
   * Devices like PCs have very different power consumption than a phone.
* CPU Registers
   * How many registers is it consuming?
   * Device drivers or systems level programming.
* In the above example:
   * Time 
      * Every statement takes **1 unit of time**.
         * **3 units of time total.**
         * *f(n) = 3* so fixed time.
         * Can also represent as *O(1)*
         * This is a simplification as code may be more detailed.
   * Space
      * Variable take **1 unit of space**.
         * **3 variables used.**
         * *s(n) = 3 words* so constant space.
         * Can also represent as *O(1)*

## Frequency Count Method <a name="5"></a>
```
algorithm sum(A, n) {
   s = 0;
   for (i = 0; i < n; i++) {
      s = s + A[i];
   }
   return s;
}
```
   * A = [8, 3, 9, 7, 2]   
   * n = 5
   * Time 
      * Steps
         1. s assignment - **1 unit of time**
         2. for loop
            * i starts at 0 and is checked n+1 times
            * Incremented by 1 and stops at n+1 as i < n
            * **n+1 units of time**
         3. for loop - s reassignment
            * **n units of time**
         4. return s - **1 unit of time**
      * Function
         * *f(n) = 1 + (n + 1) + n + 1 = 2n + 3*
         * Degree of *f(n) = 2n + 3* is *n* so **O(n)**
   * Space
      * A - n
      * n - 1
      * s - 1
      * i - 1
      * Function
         * *s(n) = n + 1 + 1 + 1 = n + 3*
         * Degree of *s(n) = n + 3* is *n* so **O(n)**

```
algorithm add(A, B, n) {
   C = matrix(n, n);
   for (i = 0; i < n; i++) {
      for (j = 0; j < n; j++) {
         C[i, j] = A[i, j] + B[i, j];
      }
   }
   return C;
}
```
   * Matrix addition with A and B which are n x n matrices
      * [[0 1 2]
        [3 4 5]
        [6 7 8]]
   * n = 3
   * Time
      * Steps
         1. C assignment - **1 unit of time**
         2. for loop (i) - **n + 1 units of time**
         3. for loop (j) - **n * (n + 1) units of time**
            * Because within for loop(i) executes n times in addition to n + 1 times
         4. C index assignment - **n * n**
      * Function
         * *f(n) = 1 + n + 1 + n^2 + n + n^2 = 2n^2 + 2n + 2*
         * Degree of *f(n) = 2n^2 + 2n + 2* so **O(n^2)**
   * Space
      * A - n^2
      * B - n^2
      * C - n^2
      * n - 1
      * i - 1
      * j - 1
      * Function
         * *s(n) = 3n^2 + 3*
         * Degree of *s(n) = 3n^2 + 3* so **O(n^2)**

```
algorithm multiply(A, B, n) {
   C = matrix(n, n);
   for (i = 0; i < n; i++) {
      for (j = 0; j < n; j++) {
         C[i, j] = 0;
         for (k = 0; k < n; k++) {
            C[i, j] = C[i, j] + A[i, k] * B[k, j];
         }
      }
   }
   return C;
}
```
   * Matrix multiplication with A and B which are n x n matrices.
   * Time
      * Steps
         1. C assignment - **1 unit of time**
         2. for loop (i) - **n + 1 units of time**
         3. for loop (j) - **n * (n + 1) units of time = n^2 + n units of time**
         4. C index assignment - **n * n * 1 units of time = n^2 units of time**
         5. for loop (k) - **n * n * (n + 1) units of time = n^3 + n^2 units of time**
         6. C index assignment **n * n * n * 1 units of time = n^3 units of time**
      * Function
         * *f(n) = 1 + n + 1 + n^2 + n + n^2 + n^3+ n^2 + n^3 = 2n^3 + 3n^2 + 2n + 2*
         * Degree of *f(n) = 2n^3 + 3n^2 + 2n + 2* so **O(n^3)**
   * Space
      * A - n ^ 2
      * B - n ^ 2 
      * C - n ^ 2
      * n - 1
      * i - 1
      * j - 1
      * k - 1
      * Function
         * *s(n) = 3n^2 + 4*
         * Degree of *s(n) = 3n^2 + 4* so **O(n^2)**

