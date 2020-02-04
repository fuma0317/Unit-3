# Unit3 Snakify practices
## 1. Input, print and numbers ##
### Sum of three numbers ###
```
# This program reads three numbers and prints their sum:
a = int(input())
b = int(input())
c = int(input())
print(a + b + c)
```
### Square ###
```
a = int(input())
print(a ** 2)
```
### Apple Sharing ###
```
N = int(input())
K = int(input())
print(K // N)
print(K % N)
```
### Previous and next ###
```
a = int(input())
a1 = (a + 1)
a2 = (a - 1)
str1 = "The next number for the number"
str2 = "is"
str3 = "The previous number for the number"
print(str1, a, str2, a1,'.')
print(str3, a, str2, a2,'.')
```
This code doesn't pass the test. The problem is I don't figure out how to print "180." not "180 ." 
### Two timestamps ###
```
h = int(input())
m = int(input())
s = int(input())
h2 = int(input())
m2 = int(input())
s2 = int(input())
hd = ((h2 - h) * 3600)
md = ((m2 - m) * 60)
sd = (s2 - s)
re =(hd + md + sd)
print(re)
```
## 2.Integer and float numbers ##
### Last digit of integer ###
```
a = int(input())
print(a % 10)
```
or
```
a = int(input())
lastdigit = int(repr(a)[-1])
print(lastdigit)
```
### Tens digit ###
```
n = int(input())
s = str(n)
le = (len(s))
if le > 1:
    print(s[-2])
else:
    print("0")

```
or
```
n = int(input())
print(n // 10 % 10)
```
### Car route ###
```
N = int(input())
M = int(input())
i = 0
while M < N:
    (N * i)
    i += 1 
else:
    print(i)
```
I tried to make a function that keeps multiplying 1,2,3,4... to N kilometers until I becomes larger than M kilometers.

### Digital clock ###
```
N = int(input())
H = (N // 60)
M = (N % 60)
print(H, M)
```

## 3. Conditions: if, then, else ##
### Minimum of two numbers ###
```
A = int(input())
B = int(input())
if A > B:
    print(B)
else:
    print(A)
```
### Sign function ###
```
X = int(input())
if X > 0:
    print("1")
elif X < 0:
    print("-1")
else:
    print("0")
```
### Rock move ###
```
A = int(input())
B = int(input())
C = int(input())
D = int(input())
if A == C:
    print("YES")
elif B == D:
    print("YES")
else:
    print("NO")
```
### Chocolate bar ###
英語がわからん

## 4.For loop with range ##
### Sum of N numbers ###
```
N = int(input())
data = [input() for _ in range(N)]
s = sum(data)
print(s)
```
Itt doesn't work. I couldn't figure out why
### The number of zeros ###
I searched out how to get N numbers and put them in list but I don't get how to break the list down to calculate

### Lost card ###
same reason as previous one


