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


