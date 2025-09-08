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
##31.WRITE A C PROGRAM TO FIND THE SUM OF FIRST N NATURAL NUMBERS WHICH ARE NOT DIVISIBLE BY 3 OR 5 USING LOOPS AND IF-ELSE STATEMENTS?
```c
#include<stdio.h>
int main()
{
    int n,i,sum=0;
    printf("Enter n:");
    scanf("%d",&n);
    for(i=1;i<=n;i++)
    {
        if(i%3!=0&&i%5!=0)
        {
            sum=sum+i;
        }
    }
    printf("Sum=%d",sum);
}
```
##32.WRITE A C PROGRAM TO FIND THE SUM OF ALL EVEN NUMBERS BETWEEN TWO GIVEN NUMBERS USING LOOPS AND IF-ELSE STATEMENTS?
```c
#include<stdio.h>
int main()
{
    int start,end;
    printf("Enter two numbers:");
    scanf("%d%d",&start,&end);
    int i,sum=0;
    for(i=start;i<=end;i++)
    {
        if(i%2==0)
        {
            sum=sum+i;
        }
    }
    printf("Sum of even numbers between %d and %d =%d",start,end,sum);
    return 0;
}
```
##33.WRITE A C PROGRAM TO FIND THE SUM OF ALL ODD NUMBERS BETWEEN TWO GIVEN 
NUMBERS USING LOOPS AND IF-ELSE STATEMENTS?
```c
#include<stdio.h>
int main()
{
    int start,end;
    printf("Enter two numbers:");
    scanf("%d%d",&start,&end);
    int i,sum=0;
    for(i=start;i<=end;i++)
    {
        if(i%2!=0)
        {
            sum=sum+i;
        }
    }
    printf("Sum of odd numbers between %d and %d =%d",start,end,sum);
    return 0;
}
```
##34.WRITE A C PROGRAM TO CHECK WHETHER A GIVEN NUMBER IS A PERFECT SQUARE OR NOT USING LOOPS AND IF-ELSE STATEMENTS. 
```c
#include<stdio.h>
int main()
{
    int i,n;
    printf("Enter a number:");
    scanf("%d",&n);
    for(i=1;i<=n;i++)
    {
        if(i*i==n)
        {
            printf("%d is a perfect square.",n);
            return 0;
        }
    }
 printf("%d is not a perfect square.",n);
return 0;
}
```
##35.WRITE A C PROGRAM TO CHECK WHETHER A GIVEN NUMBER IS A PALINDROME IN BOTH DECIMAL AND BINARY REPRESENTATIONS USING LOOPS AND IF-ELSE STATEMENTS? 
```c
#include<stdio.h>
int main()
{
    int n,rem,rev=0,a[100],k=0,i,b[100],j=0;
    printf("Enter number:");
    scanf("%d",&n);
    int org=n,temp=n;
    while(temp>0)
    {
        rem=temp%10;
        rev=rev*10+rem;
        temp=temp/10;
    }
    if(rev!=org)
    {
        printf("%d is NOT a palindrome in decimal.",n);
    }
    else
    {
    printf("%d is  a palindrome in decimal.",n);
    }
    printf("\nBinary representaton:");
    while(n>0)
    {
       a[k++]=n%2;
       n=n/2;
    }
    for(i=0;i<k;i++)
    {
       b[j++]=a[i];
    }
    for(i=0;i<j/2;i++)
    {
        int temp=b[i];
        b[i]=b[j-i-1];
        b[j-i-1]=temp;
    }
    for(i=0;i<j;i++)
    {
        printf("%d",b[i]);
    }
    printf("\n");
    for(i=0;i<k;i++)
    {
        if(a[i]!=b[i])
        {
            printf("Binary is not palindrome\n");
            return 0;
        }
    }
    printf("Binary is a palindrome.\n");
    return 0;
    
}
```
##36.WRITE A C PROGRAM TO FIND THE ASCII VALUE OF A CHARACTER USING LOOPS AND IF-ELSE 
STATEMENTS?
```c
#include<stdio.h>
int main()
{
    char ch;
    printf("Enter a character:");
    scanf("%c",&ch);
        if(ch>='A'&&ch<='Z')
        {
            printf("The ASCII value of %c is %d",ch,ch);
            return 0;
        }
         else if(ch>='a'&&ch<='z')
         {
    printf("The ASCII value of %c is %d",ch,ch);
             return 0;
         }
         else if(ch>='0'&&ch<='9')
         {
    printf("The ASCII value of %c is %d",ch,ch);
             return 0;
         }
         else
         {
    printf("The ASCII value of %c is %d",ch,ch);
             return 0;
         }
         return 0;
}
```
##37.WRITE A C PROGRAM TO FIND THE SUM OF ALL PRIME NUMBERS BETWEEN 1 AND 1000 USING LOOPS AND IF-ELSE STATEMENTS?
```c
#include<stdio.h>
int main()
{
    int i,sum=0,count,j;
    printf("The prime numbers between 1 to 1000:\n");
    for(i=1;i<=1000;i++)
    {
        count=0;
        if(i==1)
        {
            continue;
        }
        for(j=2;j<i;j++)
        {
            if(i%j==0)
            {
                count++;
            }
        }
        if(count==0)
        {
            printf("%d ",i);
           sum=sum+i;
        }
    }
    printf("\nThe sum of all prime numbers between 1 and 1000 is %d",sum);
return 0;
}
```
##38.WRITE A C PROGRAM TO FIND THE SUM OF THE CUBES OF THE DIGITS OF A GIVEN NUMBER USING LOOPS AND IF-ELSE STATEMENTS? 
```c
#include<stdio.h>
#include<math.h>
int main()
{
    int n,temp,rem,sum=0;
    printf("Enter a number:");
    scanf("%d",&n);
    temp=n;
    while(temp>0)
    {
        rem=temp%10;
        sum=sum+pow(rem,3);
        temp=temp/10;
    }
    printf("Sum of cubes of digits=%d",sum);
return 0;
}
```
##40.WRITE A C PROGRAM TO FIND THE SUM OF THE EVEN DIGITS AND THE SUM OF THE ODD DIGITS SEPARATELY IN A GIVEN NUMBER USING LOOPS AND IF-ELSE STATEMENTS?
```c
#include<stdio.h>
#include<math.h>
int main()
{
    int n,i,rem,evensum=0,oddsum=0;
    printf("Enter a number:");
    scanf("%d",&n);
    for(i=n;i>0;i=i/10)
    {
        rem=i%10;
        if(rem%2==0)
        {
            evensum=evensum+rem;
        }
        else
        {
            oddsum=oddsum+rem;
        }
    }
    printf("Sum of even digits=%d\nSum of odd digits=%d",evensum,oddsum);
return 0;
}
```
##41.Write a program to input an integer n and count the number of trailing zeros in n!.
```c
#include<stdio.h>
int main()
{
    int n,i,rem,count=0;
    long long pod=1,temp;
    printf("Enter a number:");
    scanf("%d",&n);
    for(i=1;i<=n;i++)
    {
        pod=pod*i;
    }
    printf("%d!=%lld",n,pod);
    temp=pod;
    while(temp>0)
    {
        rem=temp%10;
        if(rem==0)
        {
            count++;
        }
        temp=temp/10;
    }
    printf("\nOutput=%d",count);
    
    return 0;
}
```
##42.A number is called Strong Number if the sum of the factorial of its digits equals the number itself.
```c
#include<stdio.h>
int main()
{
    int n,temp,i,pod,rem,sum=0;
    printf("Enter a number:");
    scanf("%d",&n);
    temp=n;
    while(temp>0)
    {
        rem=temp%10;
        pod=1;
        for(i=1;i<=rem;i++)
        {
            pod=pod*i;
        }
        sum=sum+pod;
        temp=temp/10;
    }
    if(sum==n)
    {
        printf("Strong Number.\n");
    }
    else
    {
        printf("Not a strong number.\n");
    }
    return 0;
}
```
##43.WRITE A C PROGRAM TO PRINT THE PATTERN OF STARS IN A HOLLOW SQUARE SHAPE USING LOOPS AND IF-ELSE STATEMENTS? 
```c
72)  #include <stdio.h>

int main()
{
    int n, i, j;
    printf("Enter the size of the square: ");
    scanf("%d", &n);
    for (i = 1; i <= n; i++)
    {
  for (j = 1; j <= n; j++)
   {
if (i == 1 || i == n || j == 1 || j == n)
      {
       printf("* ");
       }
      else
      {
      printf("  ");
      }
     }
   printf("\n");
    }
return 0;
}
```
##44.WRITE A C PROGRAM TO PRINT THE PATTERN OF STARS IN A RIGHT TRIANGLE SHAPE USING LOOPS AND IF-ELSE STATEMENTS.
```c
#include <stdio.h>
int main()
 {
    int n, i, j;
    printf("Enter the number of rows: ");
    scanf("%d", &n);
    for (i = 1; i <= n; i++)
     {
        for (j = 1; j <= n; j++)
          {
            if (j <= i)
                printf("* ");
            else
                printf("  ");
        }
        printf("\n");
    }

    return 0;
}
```
##45.WRITE A C PROGRAM TO PRINT THE PATTERN OF STARS IN A MIRRORED RIGHT TRIANGLE SHAPE USING LOOPS AND IF-ELSE STATEMENTS? 
```c
#include <stdio.h>
int main()
{
    int n, i, j;
    printf("Enter the number of rows: ");
    scanf("%d", &n);
    for (i = 1; i <= n; i++)
     {
        for (j = 1; j <= n; j++)
      {
            if (j >= n - i + 1)
                printf("* ");
            else
                printf("  ");
        }
        printf("\n");
    }

    return 0;
}
```
##46.WRITE A C PROGRAM TO PRINT THE PATTERN OF STARS IN A PYRAMID SHAPE USING LOOPS AND IF-ELSE STATEMENTS? 
```c
#include <stdio.h>
int main()
 {
    int n, i, j;
    printf("Enter the number of rows: ");
    scanf("%d", &n);
    for (i = 1; i <= n; i++)
     {
        for (j = 1; j <= 2 * n - 1; j++)
        {
            if (j >= n - i + 1 && j <= n + i - 1)
                printf("* ");
            else
                printf("  ");
        }
        printf("\n");
    }

    return 0;
}
```
##47.WRITE A C PROGRAM TO PRINT THE PATTERN OF STARS IN A MIRRORED PYRAMID SHAPE USING LOOPS AND IF-ELSE STATEMENTS?
```c
#include <stdio.h>
int main()
{
    int n, i, j;
    printf("Enter the number of rows: ");
    scanf("%d", &n);
    for (i = 1; i <= n; i++)
     {
        for (j = 1; j <= 2 * n - 1; j++)
         {
            if (j >= i && j <= 2 * n - i)
                printf("* ");
            else
                printf("  ");
        }
        printf("\n");
    }

    return 0;
}
```
##48.WRITE A C PROGRAM TO PRINT THE PATTERN OF STARS IN A DIAMOND SHAPE USING LOOPS AND IF-ELSE STATEMENTS? 
```c
#include <stdio.h>
int main()
 {
    int n, i, j;
    printf("Enter the number of rows: ");
    scanf("%d", &n);
    for (i = 1; i <= n; i++)
       {
        for (j = 1; j <= 2 * n - 1; j++)
          {
            if (j >= n - i + 1 && j <= n + i - 1)
                printf("* ");
            else
                printf("  ");
        }
        printf("\n");
    }

    for (i = n - 1; i >= 1; i--)
      {
        for (j = 1; j <= 2 * n - 1; j++)
          {
            if (j >= n - i + 1 && j <= n + i - 1)
                printf("* ");
            else
                printf("  ");
        }
        printf("\n");
    }
return 0;
}
```
##49.WRITE A C PROGRAM TO PRINT THE PATTERN OF STARS IN A HOLLOW DIAMOND SHAPE USING LOOPS AND IF-ELSE STATEMENTS? 
```c
#include <stdio.h>
int main() {
    int n, i, j;
    printf("Enter the number of rows: ");
    scanf("%d", &n);

    for (i = 1; i <= n; i++)
    {
        for (j = 1; j <= 2 * n - 1; j++)
        {
            if (j == n - i + 1 || j == n + i - 1)
                printf("* ");
            else
                printf("  ");
        }
        printf("\n");
    }

    for (i = n - 1; i >= 1; i--)
    {
        for (j = 1; j <= 2 * n - 1; j++)
         {
            if (j == n - i + 1 || j == n + i - 1)
                printf("* ");
            else
                printf("  ");
        }
        printf("\n");
    }
return 0;
}
```
##50.WRITE A C PROGRAM TO PRINT THE PATTERN OF NUMBERS IN A PYRAMID SHAPE USING LOOPS AND IF-ELSE STATEMENTS?
```c
#include <stdio.h>
int main()
 {
    int n, i, j, num;
    printf("Enter the number of rows: ");
    scanf("%d", &n);
    for (i = 1; i <= n; i++)
      {
        num = 1;
        for (j = 1; j <= 2 * n - 1; j++)
        {
            if (j >= n - i + 1 && j <= n + i - 1)
           {
                printf("%d ", num);
                if (j < n) 
                    num++;
                else 
                    num--;
            } else {
                printf("  ");
            }
        }
        printf("\n");
    }

    return 0;
}
```
##51.WRITE A C PROGRAM TO PRINT THE PATTERN OF NUMBERS IN A MIRRORED PYRAMID SHAPE USING LOOPS AND IF-ELSE STATEMENTS? 
```c
#include <stdio.h>
int main()
 {
    int n, i, j, num;
    printf("Enter the number of rows: ");
    scanf("%d", &n);
    for (i = n; i >= 1; i--)
      {
        num = 1;
        for (j = 1; j <= 2 * n - 1; j++)
          {
            if (j >= n - i + 1 && j <= n + i - 1)
               {
                printf("%d ", num);
                if (j < n)
                    num++;
                else
                    num--;
            }
             else
              {
                printf("  ");
            }
        }
        printf("\n");
    }
    return 0;
}
```
##52.WRITE A C PROGRAM TO PRINT THE PATTERN OF NUMBERS IN A RIGHT TRIANGLE SHAPE USING LOOPS AND IF-ELSE STATEMENTS? 
```c
include <stdio.h>
int main()
{
    int n, i, j;
    printf("Enter the number of rows: ");
    scanf("%d", &n);
    for (i = 1; i <= n; i++)
      {
        for (j = 1; j <= n; j++)
        {
            if (j <= i)
                printf("%d ", j);
            else
                printf("  ");
        }
        printf("\n");
    }

    return 0;
}
```
##53.WRITE A C PROGRAM TO PRINT THE PATTERN OF NUMBERS IN A MIRRORED RIGHT TRIANGLE SHAPE USING LOOPS AND IF-ELSE STATEMENTS? 
```c
#include <stdio.h>
int main()
 {
    int n, i, j;
    printf("Enter the number of rows: ");
    scanf("%d", &n);
    for (i = 1; i <= n; i++)
     {
        for (j = 1; j <= n; j++)
         {
            if (j >= n - i + 1)
                printf("%d ", j);
            else
                printf("  ");
        }
        printf("\n");
    }

    return 0;
}
```
##54.WRITE A C PROGRAM TO PRINT THE PATTERN OF ALPHABETS IN A PYRAMID SHAPE USING LOOPS AND IF-ELSE STATEMENTS? 
```c
#include <stdio.h>
int main()
 {
    int n, i, j;
    char ch;
    printf("Enter the number of rows: ");
    scanf("%d", &n);
    for (i = 1; i <= n; i++)
      {
        ch = 'A';
        for (j = 1; j <= 2 * n - 1; j++)
         {
            if (j >= n - i + 1 && j <= n + i - 1)
             {
                printf("%c ", ch);
                if (j < n)
                    ch++;
                else
                    ch--;
            }
          else
            {
            printf("  ");
            }
        }
        printf("\n");
    }

    return 0;
}
```
##55.WRITE A C PROGRAM TO PRINT THE PATTERN OF ALPHABETS IN A MIRRORED PYRAMID SHAPE USING LOOPS AND IF-ELSE STATEMENTS? 
```c
#include <stdio.h>
int main()
{
    int n, i, j;
    char ch;
    printf("Enter the number of rows: ");
    scanf("%d", &n);
    for (i = n; i >= 1; i--) {
        ch = 'A';
        for (j = 1; j <= 2 * n - 1; j++)
          {
            if (j >= n - i + 1 && j <= n + i - 1)
             {
                printf("%c ", ch);
                if (j < n)
                    ch++;
                else
                    ch--;
            }
           else
            {
                printf("  ");
            }
        }
        printf("\n");
    }

    return 0;
}
```
##56.WRITE A C PROGRAM TO PRINT THE PATTERN OF ALPHABETS IN A RIGHT TRIANGLE SHAPE USING LOOPS AND IF-ELSE STATEMENTS?
```c
#include <stdio.h>
int main()
{
    int n, i, j;
    char ch;
    printf("Enter the number of rows: ");
    scanf("%d", &n);
    for (i = 1; i <= n; i++)
     {
        ch = 'A';
        for (j = 1; j <= n; j++)
           {
            if (j <= i) {
                printf("%c ", ch);
                ch++;
            }
           else
             {
                printf("  ");
            }
        }
        printf("\n");
    }
    return 0;
}
```
##57.Write a C program to check whether the given number is a Harshad number (a number divisible by the sum of its digits).
```c
#include<stdio.h>
int main()
{
   int n,rem,sum=0,temp;
   printf("Enter a number:");
   scanf("%d",&n);
   temp=n;
   while(temp>0)
   {
       rem=temp%10;
       sum=sum+rem;
       temp=temp/10;
   }
   if(n%sum==0)
   {
       printf("Harshad Number.\n");
   }
   else
   {
       printf("Not Harshad Number.\n");
   }
    return 0;
}
```
##58.Write a C program to repeatedly calculate the sum of digits of a given number until a single-digit number is obtained, and print the final result.
```c
#include<stdio.h>
int main()
{
    int n,rem,sum;
    printf("Enter a number:");
    scanf("%d",&n);
    while(n>9)
    {
        sum=0;
        while(n>0)
        {
            rem=n%10;
            sum=sum+rem;
            n=n/10;
        }
        n=sum;
    }
    printf("%d",n);
    return 0;
}
```
##59.Take a number n. Print numbers from 1 to n using a loop with these conditions:
*If divisible by 3 → print "Fizz"
*If divisible by 5 → print "Buzz"
*If divisible by both 3 and 5 → print "FizzBuzz"
*Else → print the number itself.
*Implement it using a switch inside the loop with clever flags instead of many if-else.
```c
#include<stdio.h>
int main()
{
    int n,i,flag;
    printf("Enter a number:");
    scanf("%d",&n);
    for(i=1;i<=n;i++)
    {
        if(i%3==0&&i%5==0)
        {
            flag=0;
        }
        else if(i%3==0)
        {
            flag=1;
        }
        else if(i%5==0)
        {
            flag=-1;
        }
        else
        {
            flag=2;
        }
        switch (flag)
        {
            case -1:
            printf("FizzBuzz\n");
            break;
            case 0:
            printf("Fizz\n");
            break;
            case 1:
            printf("Buzz\n");
            break;
            case 2:
            printf("%d\n",i);
            break;
        }
    }
return 0;
}
```
##60.
