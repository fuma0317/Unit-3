# Unit3 Map, Filter and Reduce function #
## Map function ##
```
mport math

def area(r):
    """Area of a circle with radius 'r' ."""
    return math.pi * (r**2)

radii = [2, 5, 7.1, 0.3, 10]

map(area, radii)

list(map(area, radii))
```
Map function automatically replace the vales of list into a function.
```
Data: a1, a2..., an
Function: f
map(f, data)
```
**Examplar code for map function that converts Celsius to Fahrenheit**
```
temps = [("Berlin", 29), ("Cairo", 36), ("Buenos Aires", 19), ("Los Angeles", 26), ("Tokyo", 27), ("New York", 28), ("London", 22), ("Beijing", 32)]

c_to_f = lambda data: (data[0], (9/5)*data[1] + 32)

list(map(c_to_f, temps))
```
For example, if you have a list [("Tokyo", 27)], you can get first value as [0] and second value as [1].
   And also "lambda" has a same role as function.
   
-----------------------------------------------------
   
## Filter function ##
```
import statistics
data = [1.3, 2.7, 0.8, 4.1, 4.3, -0.1]
avg = statistics.mean(data)

l1 = list(filter(lambda x: x > avg, data))
l2 = list(filter(lambda x: x < avg, data))
```
Filter function literally removes specified values in the list.  First, import statistics and make a list named "data".  And calculate the average of the list by
```
statistic.mean()
```
Secondly, remove the numbers that are smaller than the average. Filter removes the numbers or values that are not mentioned or specified by user. So, in this case, filter function removes the numbers in the list except numbers bigger than the average. And the output of "l1" would be 
```
[2.7], [4.1], [4.3]
```
Additionally, lambda is used as substitute of "def". It works in only one row. So it enable you to define the function in one row.
```
list(filter(lambda x: xxx, xxx))
```
**Remove missing data**
```
#remove missing data
countries = ["", "Argentina", "", "Brazil", "Chile", "", "Colombia", "", "Ecuador", "", "", "Venezuela" ]

l3 = list(filter(None, countries))
```
Filter function is also used to remove the missing parts. If you want to remove all empty values in a list, 
```
list(filter(None, xxx)
```
Put "None" and "name of the list" in the bracket. In this case, the output of "l3" would be
```
['Argentina', 'Brazil', 'Chile', 'Colombia', 'Ecuador', 'Venezuela']
```

