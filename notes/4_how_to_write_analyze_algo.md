4. [How to Write and Analyze Algorithms](#4) [(Click for Video)](https://www.youtube.com/watch?v=0IAPZzGSbME&list=PLDN4rrl48XKpZkf03iYFl-O29szjTrs_O&index=4)

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