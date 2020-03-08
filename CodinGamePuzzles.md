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
    youheight = 9
    mountain_in = []
    mountain_in.append(9, 8, 7, 6, 5, 4, 3, 2)
    for i in range(8):
        youheight = youheight - 1
        l = list(filter(lambda x: x < youheight, mountain_in))
        print(max(l))
 ```
 I wanted to make a code that repeat 9-1(your index) and each time the max index of mountains by filtering the index which is bigger than your index. However, this code is not working somehow. I probably misread the concept of the problem.
