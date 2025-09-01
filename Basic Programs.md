##1.WRITE A C PROGRAM TO ACCEPT TWO INTEGERS AND CHECK WHETHER THEY ARE EQUAL OR 
NOT? 
```c
#include<stdio.h>
int main()
{
    int n1,n2;
    printf("Enter first number:");
    scanf("%d",&n1);
    printf("Enter second number:");
    scanf("%d",&n2);
    if(n1==n2)
    {
        printf("The numbers are equal.");
    }
    else
    {
        printf("The numbers are not equal.");
    }
   return 0; 
}
```
##2.WRITE A C PROGRAM TO CHECK WHETHER A GIVEN NUMBER IS EVEN OR ODD?
```c
#include<stdio.h>
int main()
{
    int n;
    printf("Enter a number:");
    scanf("%d",&n);
    if(n%2==0)
    {
        printf("%d is Even.",n);
    }
    else
    {
        printf("%d is Odd.",n);
    }
   return 0; 
}
```
##3.WRITE A C PROGRAM TO CHECK WHETHER A GIVEN NUMBER IS POSITIVE OR NEGATIVE?
```c
#include<stdio.h>
int main()
{
    int n;
    printf("Enter a number:");
    scanf("%d",&n);
    if(n<0)
    {
        printf("%d is Negative",n);
    }
    else if(n==0)
    {
    printf("%d is neither Positive nor Negative.",n);
    }
    else
    {
        printf("%d is positive",n);
    }
    
   return 0; 
}
```
##4.WRITE A C PROGRAM TO FIND WHETHER A GIVEN YEAR IS A LEAP YEAR OR NOT? 
```c
#include<stdio.h>
int main()
{
    int year;
    printf("Enter a year:");
    scanf("%d",&year);
    if(year%400==0||(year%4==0&&(year%100!=0)))
    {
        printf("%d is a Leap year",year);
    }
    else
    {
        printf("%d is not a Leap year",year);
    }
    return 0;
    
}
```
##5.WRITE A C PROGRAM TO READ THE AGE OF A CANDIDATE AND DETERMINE WHETHER HE IS 
ELIGIBLE TO CAST HIS/HER OWN VOTE?
```c
#include<stdio.h>
int main()
{
    int age;
    printf("Enter age:");
    scanf("%d",&age);
    if(age<0)
    {
        printf("Invalid entery age. ");
    }
    else if(age<18)
    {
        printf("You are not eligiable to cast your vote");
    }
    else
    {
    printf("You are eligiable to cast your vote");
    }
    return 0;
    
}
```
##6.WRITE A C PROGRAM TO READ THE VALUE OF AN INTEGER M AND DISPLAY THE VALUE OF N IS 
1 WHEN M IS LARGER THAN 0, 0 WHEN M IS 0 AND -1 WHEN M IS LESS THAN 0. 
```c
#include<stdio.h>
int main()
{
    int m,n;
    printf("Enter value of m:");
    scanf("%d",&m);
    if(m>0)
    {
       n=1;
    }
    else if(m==0)
    {
       n=0; 
    }
    else
    {
   n=-1;
    }
    printf("value of N=%d",n);
    return 0;
    
}
```
##7.WRITE A C PROGRAM TO FIND THE LARGEST OF THREE NUMBERS? 
```c
#include<stdio.h>
int main()
{
    int n1,n2,n3;
    printf("Enter three numbers:");
    scanf("%d%d%d",&n1,&n2,&n3);
    if(n1>=n2&&n1>=n3)
    {
      printf("The largest number is %d",n1);
    }
    else if(n2>=n1&&n2>=n3)
    {
        printf("The largest number is %d",n2);
    }
    else
    {
     printf("The largest number is %d",n3);
    }
    return 0;
}
```
##8.WRITE A C PROGRAM TO CHECK WHETHER A CHARACTER IS A VOWEL OR CONSONANT? 
```c
#include<stdio.h>
int main()
{
    char ch;
    printf("Enter a character:");
    scanf("%c",&ch);
    if(ch>=65&&ch<=90||ch>=97&&ch<=122)
    {
        if(ch=='A'||ch=='E'||ch=='I'||ch=='O'||ch=='U'||ch=='a'||ch=='e'||ch=='i'||ch=='o'||ch=='u')
        {
            printf("%c is a vowel",ch);
        }
    else
    {
        printf("%c is a consonant",ch);
    }
    }
    
    return 0;
}
```
##9.WRITE A C PROGRAM TO CHECK WHETHER A CHARACTER IS AN ALPHABET OR NOT? 
```c
#include<stdio.h>
int main()
{
    char ch;
    printf("Enter a character:");
    scanf("%c",&ch);
    if(ch>=65&&ch<=90||ch>=97&&ch<=122)
    {
        printf("%c is an alphabet",ch);
    }
    else
    {
        printf("%c is not an alphabet",ch);
    }
    return 0;
}
```
##10.WRITE A C PROGRAM TO FIND MINIMUM OR MAXIMUM BETWEEN TWO NUMBERS?
```c
#include<stdio.h>
int main()
{
    int n1,n2;
    printf("Enter two number:");
    scanf("%d%d",&n1,&n2);
    if(n1>n2)
    {
        printf("Maximum number=%d\nMinimum number=%d",n1,n2);
    }
    else if(n2>n1)
    {
       printf("Maximum number=%d\nMinimum number=%d",n2,n1);
    }
    else
    {
        printf(" Both  numbers are equal ");
    }
    return 0;
}
```
##11.WRITE A C PROGRAM TO ENTER WEEK NUMBER AND PRINT DAY OF WEEK?
```c
#include<stdio.h>
int main()
{
    int n;
    printf("Enter Week nummber (1-7):");
    scanf("%d",&n);
    switch(n)
    {
        case 1:
        printf("Sunday");
        break;
        case 2:
        printf("Monday");
        break;
        case 3:
        printf("Tuesuday");
        break;
        case 4:
        printf("Wednesday");
        break;
        case 5:
        printf("Thursday");
        break;
        case 6:
        printf("friday");
        break;
        case 7:
        printf("Saturday");
        break;
        default:
        printf("Invalid input! Please enter week number between 1-7.");
    }
    return 0;
}
```
##12.WRITE A C PROGRAM TO CHECK WHETHER A CHARACTER IS UPPERCASE OR LOWERCASE? 
```c
#include<stdio.h>
int main()
{
    char ch;
    printf("Enter a character:");
    scanf("%c",&ch);
    if(ch>='A'&&ch<='Z')
    {
     printf("%c is an uppercase letter",ch);
    }
    else if(ch>='a'&&ch<='z')
    {
      printf("%c is an lowercase letter",ch); 
    }
    else
    {
     printf("%c is not an alphabet character",ch);
    }
    
    return 0;
}
```
##13.WRITE A C PROGRAM TO FIND NUMBER OF DAYS IN MONTH?
```c
#include<stdio.h>
int main()
{
    int month;
    printf("Enter month number(1-12):");
    scanf("%d",&month);
    switch(month)
    {
        case 1:
        printf("January has 31 days");
        break;
        case 2:
        printf(" February has 28 days");
        break;
        case 3:
        printf(" March has 31 days");
        break;
        case 4:
        printf("April has 30 days");
        break;
        case 5:
        printf("May has 31 days");
        break;
        case 6:
        printf("June has 30 days");
        break;
        case 7:
        printf("July has 31 days");
        break;
        case 8:
        printf(" August has 31 days");
        break;
        case 9:
        printf(" September has 30 days");
        break;
        case 10:
        printf("October has 31 days");
        break;
        case 11:
        printf("November has 30 days");
        break;
        case 12:
        printf("December has 31 days");
        break;
        default:
        printf("Invalid month number!");
    }
     return 0;
}
```
##14.WRITE A C PROGRAM TO FIND MAXIMUM BETWEEN TWO NUMBERS USING SWITCH CASE?
```c
#include<stdio.h>
int main()
{
    int n1,n2;
    printf("Enter two numbers:");
    scanf("%d%d",&n1,&n2);
    switch(n1>n2)
    {
        case 1:
        printf("Maximum number=%d",n1);
        break;
    case 0:
    switch(n2>n1)
    {
        case 1:
       printf("Maximun number=%d",n2);
       break;
       case 0:
       printf("Both are equal numbers");
       break;
    }
    break;
    }
     return 0;
}
```
##15.WRITE A C PROGRAM TO PRINT EVEN NUMBERS BETWEEN 1 TO 20 USING A FOR LOOP?
```c
#include<stdio.h>
int main()
{
    int i;
    printf("Even numbers between 1 to 20 are:\n");
    for(i=1;i<=20;i++)
    {
        if(i%2==0)
        {
            printf("%d ",i);
        }
    }
    return 0;
}
```
##16.WRITE A C PROGRAM TO CALCULATE THE SUM OF NUMBERS FROM 1 TO 100 USING A WHILE 
LOOP? 
```c
#include<stdio.h>
int main()
{
    int i=1,sum=0;
    while(i<=100)
    {
        sum=sum+i;
        i++;
    }
    printf("The sum of numbers from 1 to 100:%d",sum);
    return 0;
}
```
##17.WRITE A C PROGRAM TO FIND THE FACTORIAL OF A GIVEN NUMBER USING A FOR LOOP?
```c
#include<stdio.h>
int main()
{
    int i,n,product=1;
    printf("Enter a number:");
    scanf("%d",&n);
    for(i=1;i<=n;i++)
    {
        product*=i;
    }
    printf(" factorial of %d = %d",n,product);
    return 0;
}
```
##18.WRITE A C PROGRAM TO CHECK WHETHER A GIVEN NUMBER IS PRIME OR NOT USING A 
WHILE LOOP?
```c
#include<stdio.h>
int main()
{
    int i=2,n,count =0;
    printf("Enter a number:");
    scanf("%d",&n);
    if(n==1)
    {
        printf("%d is not a prime number",n);
        return 0;
    }
    while(i<=n/2)
    {
        if(n%i==0)
        {
           count++;
        }
        i++;
    }
    if(count==0)
    {
        printf("%d is a prime number",n);
    }
    else
    {
       printf("%d is not a prime number",n);
    }
    
    
    return 0;
}
```
##19.WRITE A C PROGRAM TO FIND THE SUM OF DIGITS OF A NUMBER USING A WHILE LOOP?
```c
#include<stdio.h>
int main()
{
    int n,sum=0,rem;
    printf("Enter a number:");
    scanf("%d",&n);
    int i=n;
    while(i>0)
    {
        rem=i%10;
        sum=sum+rem;
        i=i/10;
    }
    printf("Sum of digits=%d",sum);
    return 0;
}
```
##20.WRITE A C PROGRAM TO PRINT FIBONACCI SERIES UP TO N TERMS USING A FOR LOOP? 
```c
#include<stdio.h>
int main()
{
    int n,i;
    printf("Enter a number:");
    scanf("%d",&n);
    int n1=0,n2=1;
    int next=n1+n2;
  printf("Fibonacci Series:%d %d ",n1,n2);
  for(i=3;i<=n;i++)
  {
      printf("%d ",next);
      n1=n2;
      n2=next;
      next=n1+n2;
  }
    return 0;
}
```
##21.WRITE A C PROGRAM TO REVERSE A GIVEN NUMBER USING A WHILE LOOP?
```c
#include<stdio.h>
int main()
{
    int n,temp,rem,rev=0;
    printf("Enter a number:");
    scanf("%d",&n);
    int sing=0;
    if(n<0)
    {
     n=-n; 
     sing=-1;
    }
    temp=n;
    while(temp>0)
    {
        rem=temp%10;
        rev=rev*10+rem;
        temp=temp/10;
    }
    if(sing==-1)
    {
    rev=-rev;
    }
    printf("%d",rev);
    
    
    return 0;
}
```
##22.WRITE A C PROGRAM TO FIND THE POWER OF A NUMBER USING A FOR LOOP?
```c
#include<stdio.h>
int main()
{
    int b,e,res=1,i;
    printf("Enter base:");
    scanf("%d",&b);
    printf("Enter exponent:");
    scanf("%d",&e);
    for(i=1;i<=e;i++)
    {
        res=res*b;
    }
    printf("%d^%d=%d",b,e,res);
    return 0;
}
```
##23.WRITE A C PROGRAM TO FIND THE FACTORIAL OF A NUMBER USING A WHILE LOOP?
```c
#include<stdio.h>
int main()
{
    int n,i=1,product=1;
    printf("Enter number:");
    scanf("%d",&n);
    while(i<=n)
    {
       product*=i; 
        i++;
    }
    printf("Factorial of number %d:%d",n,product);
    return 0;
}
```
##24.WRITE A C PROGRAM TO PRINT THE MULTIPLICATION TABLE OF A GIVEN NUMBER USING A FOR LOOP? 
```c
#include<stdio.h>
 int main()
{
 int n,i;
 printf("Enter number:");
scanf("%d",&n);
 if(n<0)
 {
 printf("There is no table.");
 return 0;
 }
printf("Multiplication of table %d:\n",n);
 for(i=1;i<=10;i++)
 {
printf("%dX%d=%d\n",n,i,n*i);
 }
return 0;
}
```
##25.WRITE A PROGRAM IN C TO PRINT THE ARMSTRONG NUMBERS BETWEEN 1 AND 1000 USING A FOR LOOP? 
```c
#include<stdio.h>
#include<math.h>
int main()
{
    int i,count,rem,sum,temp;
    printf("Armstrong numbers between 1 to 1000:\n");
    for(i=1;i<=1000;i++)
    {
        sum=0;
        temp=i;
        count=0;
        while(temp>0)
        {
            count++;
            temp=temp/10;
        }
        temp=i;
        while(temp>0)
        {
            rem=temp%10;
            sum=sum+pow(rem,count);
            temp=temp/10;
        }
        if(sum==i)
        {
         printf("%d\n",sum);
        }
    }
    return 0;
}
```
##26.WRITE A PROGRAM IN C TO IMPLEMENT A SIMPLE CALCULATOR USING SWITCH-CASE STATEMENTS? 
```c
#include<stdio.h>
int main()
{
    int a,b;
    char op;
    printf("Enter two numbers:");
    scanf("%d%d",&a,&b);
    printf("Enter an operator (+, -, *, /):");
    scanf(" %c",&op);
    switch(op)
    {
        case '+':
        printf("Result=%d",a+b);
        break;
         case '-':
        printf("Result=%d",a-b);
        break;
         case '*':
        printf("Result=%d",a*b);
        break;
         case '/':
        if(b!=0)
                printf("Result = %d",a/b);
            else
                printf("Error: Division by zero not allowed");
            break;
        default:
            printf("Invalid operator");
    }
    
    return 0;
}
```
##27.WRITE A PROGRAM IN C TO CHECK WHETHER A GIVEN NUMBER IS A PALINDROME OR NOT USING WHILE LOOPS AND IF-ELSE STATEMENTS?
```c
#include<stdio.h>
int main()
{
int n,i,rem,rev=0;
printf("Enter a number:");
scanf("%d",&n);
int org=n;
i=n;
while(i>0)
{
rem=i%10;
rev=rev*10+rem;
i=i/10;
}
if(n==rev)
{
printf("%d is a palindrome number.",n);
}
else
{
printf("%d is not a palindrome number.",n);
}
return 0;
}
```
##28.WRITE A PROGRAM IN C TO FIND THE SUM OF ELEMENTS IN THE UPPER TRIANGULAR MATRIX USING LOOPS AND IF-ELSE STATEMENTS?
```c
#include<stdio.h>
int main()
{
    int rows,cols;
    printf("Enter rows and cols:");
    scanf("%d%d",&rows,&cols);
    int a[rows][cols],i,j,sum=0;
    printf("Enter elements:");
    for(i=0;i<rows;i++)
    {
        for(j=0;j<cols;j++)
        {
            scanf("%d",&a[i][j]);
        }
    }
    for(i=0;i<rows;i++)
    {
        for(j=0;j<cols;j++)
        {
            if(i<=j)
            {
                sum=sum+a[i][j];
            }
        }
    }
    printf("Sum of lower triangular matrix elements = %d",sum);

return 0;
}
```
##29.WRITE A PROGRAM IN C TO FIND THE SUM OF ELEMENTS IN THE LOWER TRIANGULAR MATRIX USING LOOPS AND IF-ELSE STATEMENTS? 
```c
#include<stdio.h>
int main()
{
    int rows,cols;
    printf("Enter rows and cols:");
    scanf("%d%d",&rows,&cols);
    int a[rows][cols],i,j,sum=0;
    printf("Enter elements:");
    for(i=0;i<rows;i++)
    {
        for(j=0;j<cols;j++)
        {
            scanf("%d",&a[i][j]);
        }
    }
    for(i=0;i<rows;i++)
    {
        for(j=0;j<cols;j++)
        {
            if(i>=j)
            {
                sum=sum+a[i][j];
            }
        }
    }
    printf("Sum of lower triangular matrix elements = %d",sum);

return 0;
}
```
##30.WRITE A C PROGRAM TO PRINT ALL THE ODD NUMBERS BETWEEN 1 TO 50 USING A FOR LOOP? 
```c
#include<stdio.h>
int main()
{
    int i;
    printf("Odd numbers between 1 to 50:\n");
    for(i=1;i<=50;i++)
    {
        if(i%2!=0)
        {
            printf("%d ",i);
        }
    }
    return 0;
}
```



