https://www.youtube.com/watch?v=p1EnSvS3urU&list=PLDN4rrl48XKpZkf03iYFl-O29szjTrs_O&index=8

### Increment
```
i = 0;
while (i < n) {
    stmt;
    i++;
}
```

* `i + (n+1) + n + n = 3n + 2 = O(n)`
* Condition is n + 1 as executes n times and once more on exit condition.


### Multiply
```
a = 1;
while (a < b) {
    stmt;
    a = a * 2;
}
```

| a |
|-|
| `1 = 2^0` |
| `2 = 2^1` |
| `4 = 2^2` |
| `8 = 2^3` |

`2^k = b`

**log_2(b)**

### Multiple Increments
```
(i, k) = (1, 1);
while (k < n) {
    stmt;
    k = k + i;
    i++;
}
```
Define `m` as the unknown value of i at the end of the loop.

|`i`|`k`|
|-|-|
|1|1|
|2|1+1|
|3|2+2|
|4|2+2+3|
|5|2+2+3+4|
|`m`|2+2+3+4 + ... + `m` |


Roughly, `k` is equal to `m(m + 1) / 2`
* 2+2+3+4 almost like 1+2+3+4
* This value is the sum of [all natural numbers](https://www.cuemath.com/sum-of-natural-numbers-formula/)

Loop ends when reaching `n`.
* `k >= n`
* `m(m+1)/2 >= n`
* `m^2 >= n`
* `m = sqrt(n)`

**O(sqrt(n))**

### Equality Conditions
```
while (m != x) {
    if (m > x) {
        m = m - x
    } else {
        x = x - m
    }
}
```
#### First case.
|m|x|
|-|-|
|6|3|
|3|3|

Only one execution. (1)

#### Minimum Time.
|m|x|
|-|-|
|5|5|

Equal so no execution. (0) so `O(1)`

#### Maximum Time.
|m|x|
|-|-|
|16|2|
|14|2|
|12|2|
|10|2|
|8|2|
|6|2|
|4|2|
|2|2|

8 executions. `16/2` = `n/2` = `O(n)`

### Breaking Down a Function
```rust
fn algo_test(n: u32) {
    if n < 5 {
        println!("{n}")
    } else {
        for i in 0..n {
            println!("{i}")
        }
    }
}
```

Best case is `if` block where a single statement is executed once. 
* **O(1)**

Worst case is `else` where must execute for loop `n + 1` times.
* **O(n)**