## Table of Contents
[Guess A Number](https://github.com/Professor-Sathish/GE8151-UNIT-ILLUSTRATIVE-PROGRAMS/blob/master/MiNumInAList.md#Table-of-Contents)

- [Problem Statement](https://github.com/Professor-Sathish/GE8151-UNIT-ILLUSTRATIVE-PROGRAMS/blob/master/MinNumInAList.md#problem-statement)
- [Python Code](https://github.com/Professor-Sathish/GE8151-UNIT-ILLUSTRATIVE-PROGRAMS/blob/master/MinNumInAList.md#python-code)
- [Replit Link](https://github.com/Professor-Sathish/GE8151-UNIT-ILLUSTRATIVE-PROGRAMS/blob/master/MinNumInAList.md#replit-link)
- [PythonTutor Link](https://github.com/Professor-Sathish/GE8151-UNIT-ILLUSTRATIVE-PROGRAMS/blob/master/MinNumInAList.md#pythontutor-link)

# Problem Statement
### Minimum Number In a List
**we will see  Python program to find the smallest number in a List.**
### For example
- If the list is [15, 20, 10, 16] then the program should display number 10 as the output (the smallest number in the given list).

## Python Code
~~~python
#find minimum of two numbers
# a and b are parameters''


def find_min(a, b):
    if a < b:
        return a
    return b


print("Enter two values :")
a = int(input())
b = int(input())
print("Minimum number is ", find_min(a, b))
~~~

~~~python
#find minimum of three numbers

def find_min(a, b):
    if a < b:
        return a
    return b

# a, b and c are parameters
def min_of_three(a, b, c):
    minVal = find_min(a, b)
    if c < minVal:
        return c
    return minVal


print("Enter three numbers: ")
a = int(input())
b = int(input())
c = int(input())

print("Minimum number is ", min_of_three(a, b, c))
~~~


~~~python
# find minimum of a list
def min_of_list(aList):
    if not aList:
        return None
    minVal = aList[0]
    for number in aList[1:]:
        if number < minVal:
            minVal = number
    return minVal


myList = []
limit = int(input("Enter the limit: "))
print("Enter the elements:\n")
for i in range(limit):
    element = int(input())
    myList.append(element)

print("Minimum of list is ", min_of_list(myList))
~~~

## Replit Link
https://cutt.ly/MinimumNumberInAList

<img src="./img/MinNumRepl.png" style="width:100px;"/>


## PythonTutor Link

https://cutt.ly/MinimumNumberInAListVisualize

<img src="./img/MinNumInAListVisual.png" style="width:100px;"/>
