```
s = input("Please type comma-separated words")
a = s.split(",") #split comma-separated words by comma
b = sorted(a)   #sort the splited words in abc order
c = ','.join(b) #combine the words with comma
print(c)
```
