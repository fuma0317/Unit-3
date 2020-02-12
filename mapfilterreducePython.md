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
