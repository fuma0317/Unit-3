## The function that generates 1000 random numbers between 1 to 100. ##
```
import random
for i in range(1, 1001):
    print random.randint(1,100)
```
It works as I intended. 

## Create a graph for this numbers where the x axis are the numbers 1 to 1000, and the y axis are the random numbers. ##
```
import matplotlib.pyplot as pyplot
#create the values for the x variable from 1 to 1000
x = [i for i in range(1, 1000)]
#define the parabola function y=x**2
y = [i**2 for i in x]
```
'matplotlib' doesn't work somehow. Other parts are fine I guess


