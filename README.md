# Unit-3

***Protocols***
*:HTTP*: Hyper Text Transfer Protocol
 
 Inventor: Tim John Berners-Lee
 
 Used in: when a client get web page but it is not encrypted 
 
 encrypted version: HTTPs
 
***programs***
*1. Write a C program to check whether a given number is even or odd*
```
#include <stdio.h>

int main() {
  int num= 0;
  printf("Please type one random integer");
  scanf("%d",&num);
  if ((num % 2) == 0) {
    printf("%d is an even integer", num);
  }
  else{
    printf("%d is an odd integer", num);
  }
  
  return 0;
}
```

