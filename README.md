# Unit-3

***Protocols***
*:HTTP*: Hyper Text Transfer Protocol
 
 Inventor: Tim John Berners-Lee
 
 Used in: when a client get web page but it is not encrypted 
 
 encrypted version: HTTPs
 
## PROGRAMS ##

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
*2. Write a C program to check whether a given number is positive or negative*
```
#include <stdio.h>

int main() {
  int num= 0;
  printf("Please type one random number");
  scanf("%d",&num);
  if (num <= 0)  {
    printf("%d is a negative number", num);
  }
  else{
    printf("%d is a positive number", num);
  }
  
  return 0;
}
```
*3. Write a C program to read the age of a candidate and determine wether it is eligible for casting his/her own vote in Japan*
