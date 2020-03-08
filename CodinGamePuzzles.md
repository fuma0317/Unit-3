# Coding Games and programming #
## Profile ##
Name: fuma

## ONBOARDING ##
```
if dist_1 < dist_2: #if the distance 1 is smaller than distance 2
                    #which means enemy_1 is closer than enermy_2
    print(enemy_1)  #destory enemy_1
else:               
    print(enemy_2)  #destory enemy_2
```

## The Descent ## 
```
import statistics
while True:
    youindex = 9
    mountain_in = []
    mountain_in.append(9, 8, 7, 6, 5, 4, 3, 2)
    for i in range(8):
        youindex = youindex - 1
        l = list(filter(lambda x: x < youheight, mountain_in))
        print(max(l))
 ```
 I wanted to make a code that repeat 9-1(your index) and each time the max index of mountains by filtering the index which is bigger than your index. However, this code is not working somehow. I probably misread the concept of the problem.

## Power of Thor Episode 1 ##
```
# game loop
while True:
    remaining_turns = int(input())  # The remaining amount of turns Thor can move. Do not remove this line.
    move =""
    if light_x > initial_tx:
        move = "E"
    elif light_x < initial_tx:
        move = "W"
    elif light_y > initial_ty:
        move = "S"
    elif light_y < initial_ty:
        move = "N"
    elif light_x > initial_tx and light_y > initial_ty:
        move = "SE"
    elif light_x < initial_tx and light_y < initial_ty:
        move = "NW"
    elif light_x < initial_tx and light_y > initial_ty:
        move = "NE"
    elif light_x > initial_tx and light_y < initial_ty:
        move = "SW"
    print(move)
```
This code passes the test 1,2 but it doesn't work anymore after that...

