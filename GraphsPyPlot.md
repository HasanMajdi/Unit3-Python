# this program will generate 1000 random number between 1 to 100. 
# this program will also calculate the average of these generated number
# it will also sort the numbers from smallest to biggest
# at the end, it will print out all the numbers from the smallest to biggest

```.py
import matplotlib.pyplot as pyplot
import random
import math
# generate some integers
sum = 0
value = []
for r in range(0,1000):
    x = random.randint(1,100)
    value.append(x)

print(value)
for num in value:
    sum += num
    avg = sum/1000
print("the Average is: ", round(avg))

def bubbleSort(value):
    for n in range(len(value)-1,0,-1):
        for i in range(n):
            if value[i]>value[i+1]:
                temp = value[i]
                value[i] = value[i+1]
                value[i+1] = temp

bubbleSort(value)
print("Order of the random numbers are :", value)


x = [i for i in range (0, 1000)]
y = value

pyplot.plot(x, y)
pyplot.xlabel('x')
pyplot.ylabel('random numbers')
pyplot.show(value)

```

# this program will graph the sin function

```.py

import matplotlib.pyplot as pyplot
import math
x = [i for i in range (-10, 10)]
y = [14*(math.sin(0.5*i)) for i in x]

pyplot.plot(x, y)
pyplot.xlabel('x')
pyplot.ylabel('random numbers')
pyplot.show()

```

# this program below will show a graph the absolute value 

```.py
import matplotlib.pyplot as pyplot
import math
x = [i for i in range (-10, 10)]
y = [abs(i) for i in x]

pyplot.plot(x, y)
pyplot.xlabel('x')
pyplot.ylabel('random numbers')
pyplot.show()
```
