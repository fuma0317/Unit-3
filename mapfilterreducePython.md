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
   
## Filter function ##
```
