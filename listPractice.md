# ① Even Indices

```.py
#this program will find and print all the list elements with an even index number.

#pythonic way
print(' '.join(input().split()[::2]))

#normal way
a = input().split()
for i in range(0, len(a), 2):
    print(a[i])

```

# ② Even Elements

```.py
#this program will find and print all elements that are an even number.

#identify the list in an input
num = [int(a) for a in input().split()]
for elem in num: #put the num in a loop
    if elem % 2 == 0: #use the even num equation
        print(elem)

```

# ③ Greater Than Previous


```.py
#this program will find and print all the elements that are greater than the previous element.

num = [int(a) for a in input().split()] #using split to seperate list
for i in range(1, len(num)): #putting all the input into loop
    if num[i] > num[i - 1]: #checking if the number is bigger than the previous num
        print(num[i]) #print that num

```

# ④ Neighbors of the same sign

```.py

#this program will find and print the first adjacent elements which have the same sign

num = [int(s) for s in input().split()] #using split to seperate list
for i in range(1, len(num)): #putting all the input into loop
    if num[i] * num[i-1] > 0: #checking if the multiple of the numbers who are next to each other are bigger than 0
        print(num[i-1], num[i])
        break

```

# ⑤ Greater than neighbours

```.py
#this program will print how many number who are greater than the number who are left and right next to them

num = [int(s) for s in input().split()] #using split to seperate list
сount = 0 #this variable will count how many numbers in the list who are bigger than their neighbours
for i in range(1, len(num)-1): #putting all the input into loop
    if num[i - 1] < num[i] > num[i + 1]: #checking if the current number is bigger than its neighbours
        сount += 1 #adding to the count variable
print(сount)

```
