# Day 10: Binary Numbers
## Objective

Today, we're working with binary numbers. Check out the Tutorial tab for learning materials and an instructional video!


## Task

Given a base-**10** integer, **n**, convert it to binary (base-**2**). Then find and print the base-**10** integer denoting the maximum number of consecutive **1**'s in **n**'s binary representation.


## Input Format

A single integer, **n**.


## Constraints
   
- **1 <= n <= 10<sup>6</sup>**


## Output Format

Print a single base-**10** integer denoting the maximum number of consecutive **1**'s in the binary representation of **n**.


## Sample Input 1

```
5
```


## Sample Output 1

```
1
```

## Sample Input 2

```
13
```


## Sample Output 2

```
2
```

## Explanation

Sample Case 1: 
The binary representation of **5** is **101**, so the maximum number of consecutive **1**'s is **1**.

Sample Case 2: 
The binary representation of **13** is **1101**, so the maximum number of consecutive **1**'s is **2**.

<br/>
<br/>

---


## Solution 
### C++

```
int main()
{
    string n_temp;
    getline(cin, n_temp);

    int n = stoi(ltrim(rtrim(n_temp)));
    cin >> n;
    int sum = 0;
    int max = 0;
    while (n > 0) {
        if (n % 2 == 1) {
            sum++;
            if (sum > max) max = sum;
        } else sum = 0;
        n = n / 2;
    }
    cout << max;
    return 0;
}
````
