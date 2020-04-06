```
#This program accepts a string and calculate the number of digits and letters
word = input("Please type text")
num = 0
str = 0

for i in word:
    if i.isalpha(): #check if it is alphabet
        str += 1
    elif i.isdigit(): #check if it is digit
        num += 1
    

print("letters{}, digits{}".format(str, num))
```
