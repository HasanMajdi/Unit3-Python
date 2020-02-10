What is map function?
The map function method creates a new array with the results of calling a function for every array element. 
The map function method calls the provided function once for each element in an array, in order.

the code below will provide the area of a given radii.
```.python
import math

def area(r):
    return math.pi * (r**2)
radii = [2, 5, 7.1, 0.3, 10]
a = list(map(area, radii))
print(a)
```


What is filter function?
You can chose the specific data that you need to chose by using filter. You can also remove or unselect all the data that 
you don't need.

the code below will filter or show only the numbers that are above the avg.
```.python
import statistics

data = [1.3, 2.7, 0.8, 4.1, 4.3, -0.1]
avg = statisics.mean(data)
print(avg)
a = list(filter(lambda x: x > avg, data))
print(a)
```

What is Reduce function?
The reduce function is a method that that executes a provided function for each value of the array.

The code shown below will print the total of data when you multiple all of them together. 
```.python
from functools import reduce

data = [2, 3, 4, 5, 6, 7, 8, 9]
multiplier = lambda x, y: x*y
a = reduce(multiplier, data)
print(a)
```
