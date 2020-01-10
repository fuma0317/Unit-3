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
*5. Write a C program to accept a coordinate point in a XY coordinate system and determine in which quadrant the coordinate point lies*
```
#include <stdio.h>

//

int main() {
  int x= 0;
  int y= 0;
  printf("Please type X coordinate and Y coordinate");
  scanf("%d %d",&x,&y);

  if (x >=1 & y >=1) {
    printf("The coordinate point (%d,%d) lies in the First quadrant.", x,y);
  }
  else if(x <0 & y >=1){
    printf("The coordinate point (%d,%d) lies in the Second quadrant.", x,y);
  }
  else if(x <0 & y <0){
    printf("The coordinate point (%d,%d) lies in  the Third quadrant.", x,y);
  }
  else{
    printf("The coordinate point (%d,%d) lies in  the Forth quadrant.", x,y);
  }
  return 0;
}
```
*6. Write a C program to find the eligibility of admission for a professional course based on the following criteria*

*Marks in Math >=65
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
*7. Write a C program to read temperature in centigrade and display a suitable message according to temperature state below:*

*Temp <0 then Freezing weather
Temp 0-10 then Very Cold weather
Temp 10-20 then Cold weather
Temp 20-30 then Normal in Temp
Temp 30-40 then It's Hot
Temp >=40 then It's Very Hot*
```
#include <stdio.h>

//

int main() {
  int temp= 0;
  printf("Please type current temperature");
  scanf("%d",&temp);

  if (temp < 0) {
    printf("Freezing weather");
  }
  else if(0 <= temp & temp < 10){
    printf("Very Cold weather");
  }
  else if(10 <= temp & temp < 20){
    printf("Cold weather");
  }
  else if(20 <= temp & temp < 30){
    printf("Normal in Temp");
  }
  else if(30 <= temp & temp < 40){
    printf("It's Hot");
  }
  else if(40 <= temp){
    printf("It's Very Hot");
  }
  return 0;
}
```

