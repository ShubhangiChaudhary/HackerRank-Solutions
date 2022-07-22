## Day 3: Arrays
## Objective

In this challenge, we learn about Arrays. Check out the attached tutorial for more details.


## Task

Complete the getSecondLargest function in the editor below. It has one parameter: an array, **nums**, of **n** numbers. The function must find and return the second largest number in **nums**.

 
## Input Format

Locked stub code in the editor reads the following input from stdin and passes it to the function: <br/>
The first line contains an integer, **n**, denoting the size of the **nums** array. <br/>
The second line contains **n** space-separated numbers describing the elements in **nums**.

 
## Constraints
- **1 <= n <= 10**
- **0 <= nums <= 100**, where **nums** is the number at index **i**.
- The numbers in  are not distinct.


## Output Format

Return the value of the second largest number in the **nums** array.


## Sample Input 0

```
5
2 3 6 6 5
```


## Sample Output 0

```
5
```


## Explanation

Given the array **nums = [2,3,6,6,5]**, we see that the largest value in the array is **6** and the second largest value is **5**. Thus, we return **5** as our answer.

<br/>
<br/>

---

## Solution 

```javascript

/**
*   Return the second largest number in the array.
*   @param {Number[]} nums - An array of numbers.
*   @return {Number} The second largest number in the array.
**/
function getSecondLargest(nums) {
    // Complete the function
    const max = Math.max(...nums);
    nums =nums.filter(num => num != max);
    return Math.max(...nums);
}

```


