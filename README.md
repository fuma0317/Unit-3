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
```
#include <stdio.h>

int main() {
  int num= 0;
  printf("Please type your age");
  scanf("%d",&num);
  if (num >= 18)  {
    printf("Congratulations! You are eligible for casting your vote");
  }
  else{
    printf("Sorry.. You are not eligible for casting your vote");
  }
  
  return 0;
}
```
*6. Write a C program to find the eligibility of admission for a professional course based on the following criteria

Marks in Math >=65
Marks in Phy >=55
Marks in Chem >=50
Total in all three subject >=180
or
Total in Math and Phy >=140*

```
#include <stdio.h>

//

int main() {
  int math= 0;
  int phy= 0;
  int che= 0;
  printf("Please type your makes in MATH, PHYSICS, CHEMISTRY");
  scanf("%d %d %d",&math,&phy,&che);

  if (math >=65 & phy >=55 & che >=50 & math+phy+che >=180 ) {
    printf("The candidate is eligible for admission");
  }
  else if(math >=65 & phy >=55 & che >=50 & math+phy >= 140){
    printf("The candidate is eligible for admission");
  }
  
  else{
    printf("The candidate is not eligible");
  }
  return 0;
}
```
