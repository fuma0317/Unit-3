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

