```.python
What is a Prime number?
Ans - They are numbers that are only divisible by 1 or themselves

#====first Try====#
# this code is very slow as it can't a lot of time to check if you provide a lot of data or numbers.
import math
import time
def is_prime_v1(n):
    # return True if n is a prime number. False otherwise
    if n == 1:
        return False # 1 is not a prime

    for d in range(2, n):
        if n % d == 0:
            return False
    return True

# test function
for n in range(1, 21):
    print(n, is_prime_v1(n))

#====Second Try====# 
# this code is a lot faster as it does the exact same function as the frist one but much faster in processing a data.
import math
import time
def is_prime_v1(n):
    if n == 1:
        return False
    max_divisor = int(math.floor(math.sqrt(n)))
    for d in range(2, 1 + max_divisor):
        if n % d == 0:
            return False
    return True

# time function
t0 = time.time()
for n in range(1, 100000):
    is_prime_v1(n)
t1 = time.time()
print("Time required: ", t1 - t0)
```

#====Third Try====# 
# this code is much improved one as it processes all the data twice as fast as the second one.
```.python
import math
import time
def is_prime_v3(n):
    # return True if n is a prime number . False otherwise
    if n == 1:
        return False # 1 is not a prime
    # if its even and not 2, then its not a prime
    if n == 2:
        return True
    if n > 2 and n % 2 == 0:
        return False
    max_divisor = int(math.floor(math.sqrt(n)))
    for d in range(3, 1 + max_divisor, 2):
        if n % d == 0:
            return False
    return True

# time function
t0 = time.time()
for n in range(1, 100000):
    is_prime_v3(n)
t1 = time.time()
print("Time required: ", t1 - t0)
```
