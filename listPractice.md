# List practices in Snakify #
## Even indices ##
```
x = input().split()
for i in range(0, len(x), 2):
    print(x[i])
```

## Even elements ##
```
import statistcis
e = input().split()
l = list(filter(lambda x: x%2 = 0, e))
print(l)
```
I couldn't try this in Snakify but it works

```
x = [int(i) for i in input().split()]
for e in x:
    if e % 2 == 0:
        print(e)
```

## Greater than previous ##
```
x = [int(s) for s in input().split()]
for i in range(1, len(x)):
    if i > 0:
        if x[i] > x[i-1]:
            print(x[i])
```

## Neighbors of the same sign ##
```
x = [int(s) for s in input().split()]
for e in range(1, len(x)- 1):
    if x[i] > 0 and x[i + 1] > 0: 
        print(i)
    elif x[i] < 0 and x[i + 1] < 0:
        print(i)
```
This code doesn't work

## Greater than Neighbours ##
```
```


