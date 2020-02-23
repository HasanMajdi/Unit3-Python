# ① Graph one

```.py

import matplotlib.pyplot as pyplot
import math
min_x = -2
max_x = 2
step = 0.004
num_points = int((max_x - min_x)/step)
x = []
for i in range(num_points):
    x.append(min_x + step*i)
y = [((n+1)**2)-1 for n in x]

pyplot.plot(x, y)
pyplot.show()

```

# ② Graph two (HL)

```.py

import matplotlib.pyplot as pyplot
import math
min_x = 0
max_x = 30
step = 0.05

num_points = int((max_x - min_x)/step)
x = []
for i in range(num_points):
    x.append(min_x + step*i)
m = [(i**2) for i in x]
g = [0.1*(math.sin(0.05*n)) for n in m]

pyplot.plot(x, g)
pyplot.show()

```

