``` 
# this program automatically generates a fixed number of random strings
import random, string
hm = int(input("Please type how many passwords you want"))

def randomname(n):  #function that generates random strings based on ascii
    return ''.join(random.choices(string.ascii_letters + string.digits, k=n))
    #combine all of random digits and letters into one sentence

for i in range(1, hm+1):
    print(randomname(20))
```

