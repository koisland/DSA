# [Algorithms](https://www.youtube.com/playlist?list=PLDN4rrl48XKpZkf03iYFl-O29szjTrs_O)

## Table of Contents
1. [Introduction to Algorithms](#1) [(Click for Video)](https://www.youtube.com/watch?v=0IAPZzGSbME&list=PLDN4rrl48XKpZkf03iYFl-O29szjTrs_O&index=1)
2. [Priori and Posteriori Testing](#2) [(Click for Video)](https://www.youtube.com/watch?v=0IAPZzGSbME&list=PLDN4rrl48XKpZkf03iYFl-O29szjTrs_O&index=2)
3. [Characteristics of Algorithms](#3) [(Click for Video)](https://www.youtube.com/watch?v=0IAPZzGSbME&list=PLDN4rrl48XKpZkf03iYFl-O29szjTrs_O&index=3)
4. [How to Write and Analyze Algorithms](#4) [(Click for Video)](https://www.youtube.com/watch?v=0IAPZzGSbME&list=PLDN4rrl48XKpZkf03iYFl-O29szjTrs_O&index=4)

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
  * 
* Space