```
#this program automatically creates a txt file based on the user name and number
l = []
base = input("Please type your first name, last name and number(1 to 100)")
n_base = base.split(" ")
l.append(n_base)    #put 3 elements in a list separately
times = [int(s) for s in l[3]]

for i in range (1, times + 1):
    print("{}.{}{}@uwcisak.jp".format(l[1], l[2], l[3]))
    i += 1
```
This program doesn't work somehow. I think the problem is the code that converts a element of list to integer type.
That's why the for loop is probably not working as well.
