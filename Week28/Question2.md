```
#With a given integral number n, write a program to generate a dictionary that contains (i, i*i) such that i is an integral number between 1 and n (both included). The program should print the dictionary.
n = int(input(print("Please type a number")))
d = {} #create dictionary list

for i in range(1, n+1):
    d[str(i)] = ( i**2) #convert i to string in order to put it in dictionary
print(d)
```
