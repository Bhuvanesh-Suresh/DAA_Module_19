# EX 1A Reverse a String
## DATE:22-02-2025
## AIM:
To write a program to create a recursive function to reverse a string.

## Algorithm
1.Define a recursive function revstr that takes a string as input.

2.Check if the length of the string is zero (base case).

3.If true, return the string.

4.Otherwise, call revstr on the substring excluding the first character and concatenate the first character at the end.

5.Take input from the user and call the recursive function.

6.Print the result 
 

## Program:
```
Program to implement Reverse a String
Developed by: Bhuvanesh S R
Register Number: 212223240017
```
```py
def rev(a):
    if len(a)==0:
        return a
    return rev(a[1:]) + a[0]
    
a=input()
print(rev(a))
```

## Output:
![image](https://github.com/user-attachments/assets/c9c73f00-243c-4dcf-aa77-8dbd5d2df114)




## Result:
The program successfully reverses the input string using recursion. When the user provides an input string, the output displays the reversed version of the string
