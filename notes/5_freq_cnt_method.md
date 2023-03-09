5. [Frequency Count Method](#5) [(Click for Video)](https://www.youtube.com/watch?v=0IAPZzGSbME&list=PLDN4rrl48XKpZkf03iYFl-O29szjTrs_O&index=5)

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

