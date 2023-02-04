# gibonacci-sequence
gibonacci sequence

It is defined by 𝑔0=𝑥,𝑔1=𝑦 and 𝑔𝑛=𝑔𝑛−1−𝑔𝑛−2 for 𝑛≥2 . Different possible starting values of the gibonacci sequence may lead to different gibonacci sequences.

Task You are given three arguments: n, x, y. Your task is to find 𝑔𝑛 using the above definition of a gibonacci sequence starting with 𝑔0=𝑥,𝑔1=𝑦 Write a function gibonacci(n, x, y) that takes in 3 arguments.

Inputs It is guaranteed that 𝑛,𝑥,𝑦 are integers and 0≤𝑛,𝑥,𝑦≤109 .

Outputs gibonacci(n, x, y) should return 𝑔𝑛 given that 𝑔0=𝑥,𝑔1=𝑦 .

Examples gibonacci(0, 0, 1) = 0

gibonacci(1, 0, 1) = 1

gibonacci(2, 0, 1) = 1

gibonacci(3, 0, 1) = 0

APPROACH 1

1. get a function "gibonacci"  with three parameters as integers: "n", "x" and "y".

2. if n = 0 the function returns value "x". 

3. if n = 1 the function returns value "y".

4. if n >= 2, call recursively to gibonacci function, changing parameter "n" to "n-1", "x" is "y" and "y" is "y-x". 

Reasoning:   If Gibonacci function has a paramenter "n"  equals to "0" it will return the value of "x", which is the second parameter of the function.   If Gibonacci function has a parameter "n" equals to "1" it will return the value "y" which is the third parameter of the function.  The only way to finish the Gibonacci function is by having value of "n" equals to "0" or "1".  If Gibonacci function has a value of "n" greater of equal to integer "2", it will keep recursively calling th same function with "n" equal to "n-1" and "x" in "y" and "y" in "y-x" until "n" has a value of "one".   For each call to Gibonacci function the value of "n" changes to "n-1", the value of "x' changes to "y' and the value of  "y" changes to "y-x". In other words, the gibonacci function will keep recursively calling the same function until n is "one", and returning the value of "x" converted to "y" and the value of "y" converted to "y-x".
Overall, the function uses recursion to calculate the nth number in the Gibonacci sequence by breaking down the problem into smaller subproblems and calling itself until the base cases are reached.


<font size="4">TEst cases</font>

1. gibonacci(0, 0, 1) = 0

Reasoning:  since the value of n = "0", gibonacci function returns the value of "x" which is "0".

2. gibonacci(1, 0, 1) = 1

Reasoning: since the value of n "1", gibonacci function returns the value of "y" which is "1".

3. gibonacci(2, 0, 1) = 1

Reasoning: starting with value of n = "2", the gibonacci function with recursively call again the function with parameters "n" equal "n-1" which is "1", the value of "x" which is "y" with a value of "1", and the value of "y". which es "y-x" with a value of "1-0 = 1".  At this point the funcion has a value of n equals to "1", and with n equals "1", it returns he value of "y" which is "1". 

4. gibonacci(3, 0, 1) = 0

Reasoning: At beginning we said that gibonacci function for "n" greater or equals to "2" is equal to gibonacci function(n-1) - Gibonacci function (n-2).  Since gibonacci function (n-1) is "1" (test case no. 3) and gibonacci function (g-2) is "1", the value of gibonacci (3,0,1) should be "1 -1 = 0".  

5. gibonacci(4,2,3) = -3

Reasoning:  value of n changes to 3, x to y which is 3, and y to y-x which is 1, then,
            value of n changes to 2, x to y which is 1, and y to y-x which is -2 then,
            value of n changes to 1 x to y which is -2, and y to y-x which is -3.
            Since n = 1, then function returns value of y which is -3.
            
            
To check code click here. (code)
