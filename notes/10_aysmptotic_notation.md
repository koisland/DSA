https://www.youtube.com/watch?v=A03oI0znAoc&list=PLDN4rrl48XKpZkf03iYFl-O29szjTrs_O&index=11

https://www.youtube.com/watch?v=Nd0XDY-jVHs&list=PLDN4rrl48XKpZkf03iYFl-O29szjTrs_O&index=12

# Asymptotic Notations
|Symbol|Pronunciation|Definition|
|-|-|-|
|Ο|big-oh|upper bound
|Ω|big-omega|lower bound
|Θ|theta|average bound


### Big-Oh
The function `f(n) = O(g(n))` if and only if it has these positive constants `c` and `n_0` such that **`f(n) <= c * g(n)`** for all `n >= n_0`.

Example: `f(n) = 2n + 3`
* `2n + 3 <= 10n` if `n >= 1`
* Breaking this down.
    |`f(n)`|`c`|`g(n)`|
    |-|-|-|
    |`2n + 3`|`10`|`n`|
* Therefore, `f(n) = O(g(n))` or `f(n) = O(n)`
    * `g(n)` can be any function as long as its order is greater than or equal to `f(n)`.

Write the lowest upper-bound function as closest to average bound and most representative of an algo.

### Big-Omega
The function `f(n) = Ω(g(n))` if and only if it has these positive constants `c` and `n_0` such that **`f(n) >= c * g(n)`** for all `n >= n_0`.

Example: `f(n) = 2n + 3`
* `2n + 3 >= 1n` if `n >= 1`
* Breaking this down.
    |`f(n)`|`c`|`g(n)`|
    |-|-|-|
    |`2n + 3`|`1`|`n`|

* Therefore, `f(n) = Ω(g(n))` or `f(n) = Ω(n)`
    * Or any lower bound like `Ω(log(n))`

### Theta
The function `f(n) = Θ(g(n))` if and only if it has these positive constants `c_1`, `c_2`, and `n_0` such that **`c_1 * g(n) <= f(n) <= c_2 * g(n)`** for all `n >= n_0`.

Example: `f(n) = 2n + 3`
* `1n <= 2n + 3 <= 5n`
* Breaking this down.
    |`f(n)`|`c_1`|`c_2`|`g(n)`|
    |-|-|-|-|
    |`2n + 3`|`1`|`5`|`n`|
    * Notice than `n` is identical. Can only be single value.

* Therefore, `f(n) = Θ(g(n))` or `f(n) = Θ(n)`. This is the average bound.

**Not to be confused for best case or worst case.**
* Big-Oh not restricted for worst-case.
* **Any notation can be used for either.**


# More Examples

### n!
`f(n) = n!` = `n * (n-1) * (n-2) * ... 3 * 2 * 1`

Can also be described as `1 * 2 * 3 ... * n`

The representation of the equality.
* `1 * 1 * 1 .. * 1` <= `1 * 2 * 3 ... * n` <= `n * n * n ... * n`
* Which simplifies to `1 <= n! <= n ^ n`
* Because the sides do not share the same variable, the average theta cannot be calculated.
* `Ω(1)` is lower bound.
* `O(n^n)` is upper bound.

### log n!

`f(n) = log n!`
* `log(1 * 1 * 1 .. * 1)` <= `log(1 * 2 * 3 ... * n)` <= `log(n * n * n ... * n)`
* Which simplifies to `1 <= log n! <= log n ^ n` and then into **`1 <= log n! <= n log n`**
* `Ω(1)` is lower bound.
* `O(n log n)` is upper bound.

### Take-aways
1. Use Big-Oh when you're not sure of the exact value.
2. Always use a notation that is closest to the best representation of an algo. Usually theta `Θ`.
3. Any notation can be used for worst-case or best-case of an algo.
