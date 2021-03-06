# Day 7: Arrays
## Objective

Today, we're learning about the Array data structure. Check out the Tutorial tab for learning materials and an instructional video!

## Task

Given an array, **A**, of **N** integers, print **A**'s elements in reverse order as a single line of space-separated numbers.


## Input Format

The first line contains an integer, **N** (the size of our array). 
The second line contains **N** space-separated integers describing array **A**'s elements.


## Constraints
   
- **1 <= N <= 1000**
- **1 <= A<sub>i</sub> <= 10000**, where **Ai** is the **i<sup>th</sup>** integer in the array.


## Output Format

Print the elements of array **A** in reverse order as a single line of space-separated numbers.



## Sample Input

```
4
1 4 3 2
```


## Sample Output

```
2 3 4 1
```

<br/>
<br/>

---


## Solution 1
### JavaScript

```javascript
function main() {
    const n = parseInt(readLine(), 10);

    const arr = readLine().split(' ').map(arrTemp => parseInt(arrTemp, 10));
    console.log(arr.reverse().join(' '));
}
```

## Solution 2
### C

```javascript


```
