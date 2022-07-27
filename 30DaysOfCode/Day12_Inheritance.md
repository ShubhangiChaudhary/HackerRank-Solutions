# Day 12: Inheritance
## Objective

Today, we're delving into Inheritance. Check out the attached tutorial for learning materials and an instructional video!

## Task

You are given two classes, Person and Student, where Person is the base class and Student is the derived class. Completed code for Person and a declaration for Student are provided for you in the editor. Observe that Student inherits all the properties of Person.

Complete the Student class by writing the following:

- A Student class constructor, which has **4** parameters:

1. A string, **firstName**.
2. A string, **lastName**.
3. An integer, **id**.
4. An integer array (or vector) of test scores, **scores**.

- A char calculate() method that calculates a Student object's average and returns the grade character representative of their calculated average:

![Grading Scale](https://s3.amazonaws.com/hr-challenge-images/17165/1458142706-3073bc9143-Grading.png)


## Input Format

The locked stub code in your editor calls your Student class constructor and passes it the necessary arguments. It also calls the calculate method (which takes no arguments).

You are not responsible for reading the following input from stdin: 
The first line contains **firstName**, **lastName**, and **id**, respectively. The second line contains the number of test scores. The third line of space-separated integers describes **scores**.


## Constraints
   
- **1 <= |firstName|,|lastName| <= 10**
- **|id| = 7**
- **0 <= score,average <= 100**


## Output Format

This is handled by the locked stub code in your editor. Your output will be correct if your Student class constructor and calculate() method are properly implemented.


## Sample Input

```
Heraldo Memelli 8135627
2
100 80
```


## Sample Output

```
 Name: Memelli, Heraldo
 ID: 8135627
 Grade: O
```


## Explanation

This student had **2** scores to average: **100** and **80**. The student's average grade is **https://latex.codecogs.com/svg.latex?\frac{(100&space;&plus;&space;80)}{2} = 90**. An average grade of **90** corresponds to the letter grade **O**, so our calculate() method should return the character'O'.

<br/>
<br/>

---


## Solution 

```javascript
class Student extends Person {
    /*	
    *   Class Constructor
    *   
    *   @param firstName - A string denoting the Person's first name.
    *   @param lastName - A string denoting the Person's last name.
    *   @param id - An integer denoting the Person's ID number.
    *   @param scores - An array of integers denoting the Person's test scores.
    */
    // Write your constructor here
    constructor(firstName, lastName, idNumber, testScores){
    super(firstName, lastName, idNumber);
    this.testScores = testScores;
    }
    /*	
    *   Method Name: calculate
    *   @return A character denoting the grade.
    */
    // Write your method here
    calculate(){
        var sum = this.testScores.reduce((acc, num) => {
      acc += num;
      return acc;
    });
    var avg = sum / this.testScores.length;
    
    if (avg >= 90) {
      return "O";
    }
    else if (avg >= 80) {
      return "E";
    }
    else if (avg >= 70) {
      return "A";
    }
    else if (avg >= 55) {
      return "P";
    }
    else if (avg >= 40) {
      return "D";
    }
    else {
      return "T";
    }
  }
}

```
