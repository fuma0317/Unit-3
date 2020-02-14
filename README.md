# Unit-3

 ### Journals ###
*

*1/22 2020*
 Today, we discussed about the issue about allowed extent of automated system in workplace. The background is that a programmer made his own scripts for his data collecting job so that he can play games and whatever he wants to. Then a manager of his company gets upset at him. I felt that both sides have each problems. For programmer side, he should have told his manager that he made his own scripts that automatize his work so that the manager can assign other works.  For campany side, the point is whether they knew the guy was a programmer because if they knew that fact, they should get him automatize his work and give other tasks instead.
 
 ## Python things I have to remember ##
 ### Basic calculations ###
 Inputs
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
Outputs
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
**How to use "append"**
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

### CTS (conputational thinking) ###
1. DECOMPOSITION
 Break the complicated problem into small pieces which is able to solve
1. PATTERN RECOGNITION
1. ABSTRACTION
1. ALGORITHM DESIGN

**Journals 2/14**
Today, I learned the basics of string data. More specifically, I learned how to open txtfile in python, how to split words on the txt file by spaces, how to check how many particular word in the txt and the other of "format" string. And also we reviewed "map, filter, lambda". I felt that there is so many ways to do one thing but it will be very efficient if I memorize the sysntaxes and be able to find a best way every time.

