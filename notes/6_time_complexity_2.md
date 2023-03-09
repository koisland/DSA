# [Time Complexity Example #2](https://www.youtube.com/watch?v=9SgLBjXqwd4&list=PLDN4rrl48XKpZkf03iYFl-O29szjTrs_O&index=7)

### Initial Problem
```
for (i = 1; i < n; i = i * 2) {
    stmt -> log n
}
```

Set `i` to `1`. Start is `i = 1`.

> We cannot say that executes in N time as we are not incrementing by 1.

|     i     |
|-----------|
| 1 * 2 = 2 |
| 2 * 2 = 2 ^ 2 |
| 2 * 2 * 2 = 2 ^ 3 |
| ... |
| 2 ^ k |

Assume at some point `i >= n`.

Since `i = 2 ^ k`

Therefore, `2 ^ k >= n`

`2 ^ k = n`

**k = log_2(n) so the complexity is O(log_2(n))**

> So, if we have a loop where the counter variable is not incrementing by 1 but is getting multiplied by some value, it is considered log base 2 times.

### More Examples
`n = 8`
| i |
|---|
| 1 |
| 2 |
| 4 |
| 8 |

Three iterations.

`log 8 = 3`

`log_2(2^3) = 3`

---
`n = 10`
| i |
|---|
| 1 |
| 2 |
| 4 |
| 8 |
| 16 |

Four iterations.

`log 10 = 3.2 != 4`

Take a ceiled valued so `[log n]` (imagine a half bracket)

### Division Example
```
for (i = 1; i >= n ; i = i/2) {
    stmt
}
```
Similar to multiplication example.

| i |
| - |
| 1 / 2 ^ 1 |
| 1 / 2 ^ 2 |
| 1 / 2 ^ 3 |

`n / 2 ^ k < 1`

`n = 2 ^ k`

Also `O(log_2 n)`.

### Sqrt Example
```
for (i=1; i*i<n; i++) {
    stmt;
}
```

`i * i <= n`

`i^2 = n`

`i = sqrt(n)`

`O(sqrt(n))`


### Multiple Consecutive Loops
Not nested.

```
for (i = 1; i< n ; i++) {
    stmt; --> n
}

for (j = 1; j< n ; j++) {
    stmt; --> j
}
```
O(n + n) = O(2n) = `O(n)` 

### Multiple Consecutive loops with Shared Variable

```
p = 0

for (i = 1; i < n; i = i * 2) {
    p++; -> log n
}
for (j = 1; j < p; j = j * 2) {
    stmt; -> log p
}
```
1st loop is `O(log n)`

2nd loop iterates based on the value of `p` so and its limit grows by a power of 2. This is `O(log p)`.

`p` is equal to the complexity of the first loop so `p = log n`

**O(log log n)**

### Nested Loops With `log(n)`
```
for i in (i=0; i < n; i++){
    for j in (j=1; j < n; j = j * 2) {

    }
}
```

https://youtu.be/9SgLBjXqwd4?list=PLDN4rrl48XKpZkf03iYFl-O29szjTrs_O&t=704