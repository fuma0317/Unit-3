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

##  Calculate the average of the 1000 random numbers in ① using a loop. ##
```
import random
l = []
 l.append(for i in range(1, 1001): random.randint(1,100))
 from statistics import  mean
ave = mean(l)
print(ave)
```
I'm not sure the 'append' part. But other parts would work well

## Sin graph ##
```
#this program calculates 14*sin(0.5*x) in the range x = [-10, 10]with steps of 0.1
import matplotlib.pyplot as pyplot
import math
import numpy

x = [i for i in numpy.arange(-10, 10, 0.1)]
y = [14*math.sin(0.5*i) for i in x]

# Create graph
pyplot.plot(x, y)
# Title for axis
pyplot.xlabel('x')
pyplot.ylabel('$Y = 14 * sin(o.5 * x)$')
# Show graph
pyplot.show()
print(x)
print(y)
```

## Graph linear function ##
```
import numpy as np
import matplotlib.pyplot as plt

x = np.arenge(0, 6, 0.1)

y = 2*x
plt.plot(x, y)
plt.show()
```
import parts don't work well


