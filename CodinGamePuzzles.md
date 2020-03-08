# ONBOARDING

```.pyo

# game loop
while 1:
    enemy_1 = input()  # name of enemy 1
    dist_1 = int(input())  # distance to enemy 1
    enemy_2 = input()  # name of enemy 2
    dist_2 = int(input())  # distance to enemy 2

    # Write an action using print

    if dist_1 < dist_2: #if distance enemy one is less than enemy 2 then 
        print(enemy_1) #print enemy1
    else:
        print(enemy_2) #print enemy2
    # Enter the code here

```

# The Decent

```.py

import sys
import math

# The while loop represents the game.
# Each iteration represents a turn of the game
# where you are given inputs (the heights of the mountains)
# and where you have to print an output (the index of the mountain to fire on)
# The inputs you are given are automatically updated according to your last actions.


# game loop
while True:
    height = 0
    in_hight = -1
    for i in range(8):
        mountain_h = int(input())  # represents the height of one mountain.
        if mountain_h > height: #check if the mountain height is bigger than the actual height
            height = mountain_h # if yes then set them equal to each other
            in_hight = i # the in_height changes repeating the loop
            
        

    # Write an action using print
    # To debug: print("Debug messages...", file=sys.stderr)

    # The index of the mountain to fire on.
    print(in_hight)

```

# Power of Thor - Episode 1

```.py

import sys
import math

# Auto-generated code below aims at helping you parse
# the standard input according to the problem statement.
# ---
# Hint: You can use the debug stream to print initialTX and initialTY, if Thor seems not follow your orders.

# light_x: the X position of the light of power
# light_y: the Y position of the light of power
# initial_tx: Thor's starting X position
# initial_ty: Thor's starting Y position
light_x, light_y, initial_tx, initial_ty = [int(i) for i in input().split()]
current_x, current_y = initial_tx, initial_ty # define new variable and they hold the initial_tx and initial_ty
# game loop
while True:
    remaining_turns = int(input())  # The remaining amount of turns Thor can move. Do not remove this line.
    move_string = "" # create empty string
    if current_y<light_y: #checking if the current_y is less than where the light is which is light y
        move_string = "S" # put the string in S
        current_y += 1 # add one, or moving thor
    elif current_y>light_y:
        move_string = "N"
        current_y -= 1 # moving thor forwards
    if current_x<light_x:
        move_string = move_string + "E"
        current_x += 1
    elif current_x>light_x:
        move_string = move_string + "W"
        current_x -= 1
    # A single line providing the move to be made: N NE E SE S SW W or NW
    print (move_string)

```

# There is No Spoon - Episode 1 (HL)

I couldn't do this one so I got help from the internet

```.py

import sys
import math

# Don't let the machines win. You are humanity's last hope...

width = int(input())  # the number of cells on the X axis
height = int(input())  # the number of cells on the Y axis
lines = []
for i in range(height):
    line = input()  # width characters, each either 0 or .
    lines.append(list(line))
for y in range(height):
    for x in range(width):
       if lines[y][x]==".":
           continue
       rx = ry = bx = by = -1
       try:
           for tx in range(x+1,width):
               if(lines[y][tx]=='0'):
                   rx = tx
                   ry = y
                   break
       except Exception:
           pass
       try:
           for ty in range(y+1, height):
               if(lines[ty][x]=='0'):
                   bx = x
                   by =ty
                   break
       except Exception:
           pass
       print("{0} {1} {2} {3} {4} {5}".format(x, y, rx, ry, bx, by))

```
