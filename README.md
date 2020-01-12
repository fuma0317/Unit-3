# Unit-3

***Protocols***
*:HTTP*: Hyper Text Transfer Protocol
 
 Inventor: Tim John Berners-Lee
 
 Used in: when a client get web page but it is not encrypted 
 
 encrypted version: HTTPs
 
## PROGRAMS ##
**HOMEWOEK 1**

*1. Write a C program to check whether a given number is even or odd*
```
//this program checks whether a given number is even or odd
#include <stdio.h>

int main() {
  int num= 0;
  //get random number from user
  printf("Please type one random integer");
  scanf("%d",&num);
  //check reminder of number is 0 if it is divided by 2 
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
//this program checks whether a given number is positive or negative
#include <stdio.h>

int main() {
  int num= 0;
  //get random number from user
  printf("Please type one random number");
  scanf("%d",&num);
  //check if the number is bigger or smaller than 0
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
//this program check wether candidates is eligible for casting their own vote with their ages 
#include <stdio.h>

int main() {
  int num= 0;
  //get number from user
  printf("Please type your age");
  scanf("%d",&num);
  //check if the age is bigger than 18
  if (num >= 18)  {
    printf("Congratulations! You are eligible for casting your vote");
  }
  else{
    printf("Sorry.. You are not eligible for casting your vote");
  }
  
  return 0;
}
```
*4. Write a C program to find the largest of three numbers.*
```
//this program finds the largest of three numbers
#include <stdio.h>

//

int main() {
  int num1= 0; 
  int num2= 0;
  int num3= 0;
  
  //get three random numbers from user
  printf("please type random three numbers");
  scanf("%d %d %d",&num1,&num2,&num3);
  printf("1st Number = %d,",num1);
  printf(" 2nd Number = %d,",num2);
  printf(" 3rd Number = %d,",num3);

  //find which number is the biggest and print a suitable message
  if (num1 > num2 & num1 > num3) { 
    printf("The 1st Number is the greatest amoung three");
  }
  else if(num2 > num1 & num2 > num3){
    printf("The 2nd Number is the greatest amoung three");
  }
  else if(num3 > num1 & num3 > num2){
    printf("The 3rd Number is the greatest amoung three");
    
  }
  return 0;
}
```
*5. Write a C program to accept a coordinate point in a XY coordinate system and determine in which quadrant the coordinate point lies*
```
//this program 
#include <stdio.h>


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
*8. Write a C program to check whether a triangle is Equilateral, Isosceles or Scalene.*
```
#include <stdio.h>

//

int main() {
  int ang1= 0;
  int ang2= 0;
  int ang3= 0;
  printf("please type three angles of triangle");
  scanf("%d %d %d",&ang1,&ang2,&ang3);

  if (ang1 == ang2 & ang2 == ang3) {
    printf("This is an equilateral triangle");
  }
  else if(ang1 == ang2 | ang1 == ang3 | ang2 == ang3){
    printf("This is an isosceles triangle");
  }
  else {
    printf("This is a scalene triangle");
  }
  return 0;
}
```
*9. Write a C program to check whether a triangle can be formed by the given value for the angles.*
```
#include <stdio.h>

//

int main() {
  int ang1= 0;
  int ang2= 0;
  int ang3= 0;
  printf("please type three angles");
  scanf("%d %d %d",&ang1,&ang2,&ang3);

  if (ang1+ang2+ang3 == 180) {
    printf("The triangle is valid");
  }
  else {
    printf("The triangle is not valid");
  }
  return 0;
}
```
*10 Write a program in C to calculate and print the Electricity bill of a given customer. The customer id, name and unit consumed by the user should be taken from the keyboard and display the total amount to pay to the customer. The charge are as follows:*
```
Unit              Charge/Unit
upto 199          @1.20   
200-399           @1.50
400-599           @1.80
600-              @2.00
```
If bill exceeds ¥400 then a surcharge of 15% will be charged and the minimum bill should be of ¥100/-
```
#include <stdio.h>

//

int main() {
  int uni= 0;
  int amc= 0;
  int sua= 0;
  int nap= 0;
  char cid[1000];
  char name[1000];
  printf("please type CUSTOMER id, NAME and UNIT");
  scanf("%s %s",&cid,&name);
  scanf("%d",&uni);

  printf("Customer IDNO: %s",cid);

  printf("Customer Name: %s",name);
  
  printf("Unit Consumed: %d",uni);

  if (uni < 199) {
    amc = uni * 1.20;
    printf("Amount charges@Rs.1.20 per unit: %d", amc);
  }
  else if(200 <= uni & uni < 400){
    amc = uni * 1.50;
    printf("Amount charges@Rs.1.50 per unit: %d",amc);
  }
  else if(400 <= uni & uni < 600){
    amc = uni * 1.80;
    printf("Amount charges@Rs.1.80 per unit: %d",amc);
    sua = amc * 0.15;
    nap = amc + sua;
    printf("Surcharge Amount: %d", sua);
    printf("Net Amount Paid By the Customer: %d", nap);
  }
  else if(600 <= uni){
    amc = uni * 2.00;
    printf("Amount charges@Rs.2.00 per unit: %d",amc);
    sua = amc * 0.15;
    nap = amc + sua;
    printf("Surcharge Amount: %d", sua);
    printf("Net Amount paid By the Customer: %d", nap);
  }
  return 0;
}
```
**HOMEWORK 2**

*1. Write a C program to read 10 numbers from keyboard and find their sum and average* **DOESNT WORK/ shows 9.00 instead of 9.600**
```
//this program finds their sum and average
#include <stdio.h>

int main() {
  int num1= 0;
  int num2= 0;
  int num3= 0;
  int num4= 0;
  int num5= 0;
  int num6= 0;
  int num7= 0;
  int num8= 0;
  int num9= 0;
  int num10= 0;
  int sum= 0;
  float ave= 0;
  //get random 10 numbers from user
  printf("Please type 10 random numbers");
  scanf("%d %d %d %d %d %d %d %d %d %d",&num1,&num2,&num3,&num4,&num5,&num6,&num7,&num8,&num9,&num10);
  //caluculate the sum and average of the 10 numbers
  sum= num1+num2+num3+num4+num5+num6+num7+num8+num9+num10;

  ave= sum / 10;
printf("The Sum of 10 numbers is: %d",sum);
printf(" ");
printf("The Average is: %f", ave);
return 0;
}
```
*2. Write a C program to display the cube of the number upto given an integer*
```
//display the cube of the number upto given an integer
#include <stdio.h>
//the function allows us to use "cube caluculation"
#include <math.h>

int main() {
  int num= 0;
  

  //get random one number from user
  printf("Please type one random number");
  scanf("%d",&num);
  //for loop for n times to repeat calculating
  for(int i=0; i < num; i++ ){
    printf("Number is: %d and cube of the %d is: %f",i+1,i+1, pow(i + 1, 3.0));
  }
  

return 0;
}
```
*3. Write a C program to calculate the factorial of a given number.*
```
//this program calculates the factorial of a given number
#include <stdio.h>

int main() {
  int i= 0;

  int num;
  int fact =1;
  //get random one integer from user
  printf("Please type one integer");
  scanf("%d",&num);
  //for loop for n times to repeat calculating
  for(i=1; i <=num; i++ ){
    fact = fact*i;
  };
  printf("The factorial of %d is:%d",num,fact);
  

return 0;
}
```
