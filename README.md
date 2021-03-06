# Unit-3

Contents
----------
1. [Python Skills](#pythonskills)
1. [CTS (computational thinking)](#computationalthinking)
1. [Journals](#journals)
1. [Profession](#profession)
 
PythonSkills
-----------
 ### Basic calculations ###
**Mathematical operators(Inputs)**
```
print(5 + 10)
print(3 * 7, (17 - 2) * 8)
print(2 ** 16)  # two stars are used for exponentiation (2 to the power of 16)
print(37 / 3)  # single forward slash is a division
print(37 // 3)  # double forward slash is an integer division
        # it returns only the quotient of the division (i.e. no remainder)
print(37 % 3)  # percent sign is a modulus operator
        # it gives the remainder of the left value divided by the right value
```
**Mathematical operators(Outputs)**
```
15
21 120
65536
12.333333333333334
12
1
```
**how to use round**
```
print(round(1.3))   # gives 1
print(round(1.7))   # gives 2
print(round(-1.3))  # gives -1
print(round(-1.7))  # gives -2
```
**if it's "Int"**
```
print(int(1.3))   # gives 1
print(int(1.7))   # gives 1
print(int(-1.3))  # gives -1
print(int(-1.7))  # gives -1
```
**How to get absolute value**
```
x = int(input())
print(abs(x))
```
**Nested conditions**
```
x = int(input())
y = int(input())
if x > 0:
    if y > 0:
        # x is greater than 0, y is greater than 0
        print("Quadrant I")
    else:    
        # x is greater than 0, y is less or equal than 0
        print("Quadrant IV")
else:
    if y > 0:
        # x is less or equal than 0, y is greater than 0
        print("Quadrant II")
    else:    
        # x is less or equal than 0, y is less or equal than 0
        print("Quadrant III")
  ```
 **How to use "range" in for loop**
 ```
 for i in range(5, 8):
    print(i, i ** 2)
print('end of loop')
# 5 25
# 6 36
# 7 49
# end of loop
```
**How to set start_value, end_value, step in for loop**
```
for i in range(10, 0, -2):
    print(i)
# 10
# 8
# 6
# 4
# 2
```
**How to arrange "print"**
Input
```
print(1, 2, 3)
print(4, 5, 6)
print(1, 2, 3, sep=', ', end='. ')
print(4, 5, 6, sep=', ', end='. ')
print()
print(1, 2, 3, sep='', end=' -- ')
print(4, 5, 6, sep=' * ', end='.')
```
Output
```
1 2 3
4 5 6
1, 2, 3. 4, 5, 6. 
123 -- 4 * 5 * 6
```
**How to check if it is alphabet or digit**
```
.isalpha(): #check if it is alphabet

.isdigit(): #check if it is digit
```

## How to use "append" ##
```
l = list(range(3))
print(l)
# [0, 1, 2]

l.append(100)
print(l)
# [0, 1, 2, 100]

l.append('new')
print(l)
# [0, 1, 2, 100, 'new']
```


## Lists ##
**print the elements of lists**
```
Rainbow = ['Red', 'Orange', 'Yellow', 'Green', 'Blue', 'Indigo', 'Violet']
print(Rainbow[0])
Rainbow[0] = 'red'
print('Print the rainbow')
for i in range(len(Rainbow)):
    print(Rainbow[i])
```
```
Red
Print the rainbow
red
Orange
Yellow
Green
Blue
Indigo
Violet
```
Make a list with [''] and get 1st elemtent of lists (Rainbow[0]).
If you want to get all of elements in order, use for loop with range of length of the lists.

**Empty list and add elements**
```
a = [] # start an empty list
n = int(input()) # read number of element in the list
for i in range(n): 
    new_element = int(input()) # read next element
    a.append(new_element) # add it to the list
    # the last two lines could be replaced by one:
    # a.append(int(input()))
print(a)
```
```
[1809, 1854, 1860, 1891, 1925]
```
Make an empty list with []. And add elements with xxx.append().

**Operations for list**
```
a = [1, 2, 3]
b = [4, 5]
c = a + b
d = b * 3
print([7, 8] + [9])
print([0, 1] * 3)
print(c)
print(d)
```
``` 
[7, 8, 9]
[0, 1, 0, 1, 0, 1]
[1, 2, 3, 4, 5]
[4, 5, 4, 5, 4, 5]
```
If you add two lists together, they are combined into one list. If you muliply a list by 3, it repeats the elements of the list three times. Be careful, it doesn't mean that elements times three.

**display elements of list in one row**
```
a = [1, 2, 3, 4, 5]
for elem in a:
    print(elem, end=' ')
``` 
```
1 2 3 4 5 
```

**split string input**
```
# the input is a string
# 1 2 3
s = input() # s == '1 2 3'
a = s.split() # a == ['1', '2', '3']
print(a)
```
Split the string by
```
split()
```
**one line spliting string input**
```
a = [int(s) for s in input().split()]
print(a)
```
The line converts the string input into int input.

**split string input where you want to do**
```
a = '192.168.0.1'.split('.')
print(a)
```
This will split '192.168.0.1' where it encountered "."    The output would be 
```
'192', '168', '0', '1'
```

## Class ##
**init method**
```
    def __init__(self,name, nationality, age):
        self.name = name
        self.nationality = nationality
        self.age = age
```
init method initializes instances. Class requires this method to store data of instances. 'Method' means a function in class.

**What is self**

self represents instances themselves.
```
 def say_hello(self, name):
        print('Hello, {}. I am {} '.format(name, self.name))
```
In this case, name is argument and self.name is instance named 'Fuma'. So if you open say_hello method like below
```
print(Fuma.say_hello('mike'))
```
Output would be 
```
Hello, mike. I am Fuma
```
**Inheritance**

If you inherit class 'Person', type person as argument 
```
class Saiyan(Person):
    
    def __init__(self, name, nationality, age, strength):
        super().__init__(name, nationality, age)
        self.strength = strength
 ```
 First, write what information you want to store in child class with init method. Secondly, write what information you want to inherit from parent class with 'super().__ init__' 

```
goku = Saiyan('Goku', 'Space', 65, 10000)
print (goku.name)
print(goku.say_hello('mike'))
```
In case you made an instance, you are still able to use the method in parent class
```
Goku
Hello, mike. I am Goku
```



ComputationalThinking
---------------
**Main 4 steps**

*1. DECOMPOSITION*

 Break the complicated problem into small pieces which is able to solve
 
*1. PATTERN RECOGNITION*

 Find out a regulations and patterns
 
*1. ABSTRACTION*

 Remove the unnecesarry factors and get only important factors
 
*1. ALGORITHM DESIGN*

 Clarify steps to solve a issue step by step.
 
 **Reflection**
 When I heard the term "computational thinking" at first, I thought we use the thought process for programming or computational stuff. However, I've learned that it can be applied to any problems. It helps us to tackle with a problem logically and efficiently. 
 

Journals  
------------
**Journals 1/22**
Today, we discussed about the issue about allowed extent of automated system in workplace. The background is that a programmer made his own scripts for his data collecting job so that he can play games and whatever he wants to. Then a manager of his company gets upset at him. I felt that both sides have each problems. For programmer side, he should have told his manager that he made his own scripts that automatize his work so that the manager can assign other works.  For campany side, the point is whether they knew the guy was a programmer because if they knew that fact, they should get him automatize his work and give other tasks instead.


**Journals 2/11**
Today, we tackeld with "salesman problem" in Python. Through the activity, we learned how to make an array and take out one value from it. And also we started to use "mylib" library to store the important function so that it can be used wehenever I want. I felt that I got used to calculation in Python but I was not very used to calculation regarding to math(import).

**Journals 2/12**
Today, we started off by calculating how long Bolt and cheetah take to ge to the goal by calculating a accelation. We also reviewed how to calculate root and suquared and stuff regarding to math. And also we learned how to make a system that gets password from user and add random numbers to the end of the password so that it is secure. I felt that hash function was bit confusing for me but it must be useful when we make stronger log-in system.

**Journals 2/14**
Today, I learned the basics of string data. More specifically, I learned how to open txtfile in python, how to split words on the txt file by spaces, how to check how many particular word in the txt and the other of "format" string. And also we reviewed "map, filter, lambda". I felt that there is so many ways to do one thing but it will be very efficient if I memorize the sysntaxes and be able to find a best way every time.

**Journals 2/17**
Today, We started off by learning how to graph in Python. I felt that it was very interesting because Python provides activities beyond just coding. 

**Journals 2/24**
Today, we learned how to graph sin function with three points and calculate the distance between them. I was so confused of the coding part. I guess I need to have a meeting.

**Journals 3/6**
self study interface

**Journals 3/9**
interface combined together
**Journals 3/11**
interface
## Profession ##
**Occupation**: Architect

**Software**: Auto CAD that allows users to create a 2d drawing of interior and also create 3d model of architectures and it's similar to C4d, Maya and Blender. 3ds Max provides the function which renders the 3d model of architectures and make it possible to see and show how does it look like. Lastly, with Homestyler, you can create 3d model of interior by combining the samples such as doors, furnitures and lights.

**Input**: Mouse, Keyboard

**Output**: Moniter, papers
