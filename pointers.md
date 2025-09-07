##1. Write a Program to print the address of variables using the address operator.
```c
#include<stdio.h>
 int main()
 {
 int a,b,c;
 printf("Enter values of a,b,c:");
 scanf("%d%d%d",&a,&b,&c);
 int*p=&a,*q=&b,*r=&c;
 printf("Address of a=%p\nAddress of b=%p\nAddress of c=%p",p,q,r);
 return 0;
 }
```
##2. Write a program to print size of pointer variables.
```c
#include<stdio.h>
int main()
{
    int a = 10;
    float b = 19.00;
    char ch = 'a';
    double d = 120.34;

    int *p = &a;
    float *q = &b;
    char *r = &ch;
    double *s = &d;

    printf("Size of int pointer: %ld bytes\n", sizeof(p));
    printf("Size of float pointer: %ld bytes\n", sizeof(q));
    printf("Size of char pointer: %ld bytes\n", sizeof(r));
    printf("Size of double pointer: %ld bytes\n", sizeof(s));

    return 0;
}
```
##3. Write a program to print size of pointer variables and size of values Dereferenced by them.
```c
#include <stdio.h>
int main()
{
    int a = 10;
    float b = 19.00;
    char ch = 'a';
    double d = 120.34;

    int *p = &a;
    float *q = &b;
    char *r = &ch;
    double *s = &d;

    printf("Size of int pointer: %zu bytes\n", sizeof(p));
    printf("Size of value pointed by int pointer: %zu bytes\n", sizeof(*p));

    printf("Size of float pointer: %zu bytes\n", sizeof(q));
    printf("Size of value pointed by float pointer: %zu bytes\n", sizeof(*q));

    printf("Size of char pointer: %zu bytes\n", sizeof(r));
    printf("Size of value pointed by char pointer: %zu bytes\n", sizeof(*r));

    printf("Size of double pointer: %zu bytes\n", sizeof(s));
    printf("Size of value pointed by double pointer: %zu bytes\n", sizeof(*s));

    return 0;
}
```
##4. Write a program to illustrate the dereferencing of pointers.
```c
#include<stdio.h>
 int main()
 {
int a=10,b=20,c=30;
 printf("Value of a=%d\n",a);
 printf("Value of b=%d\n",b);
 printf("Value of c=%d\n",c);
 int *p=&a,*q=&b,*r=&c;
 printf("Accessing values using pointers:\n");
 printf("*a=%d\n",*p);
 printf("*b=%d\n",*q); printf("*c=%d\n",*r);
 printf("Changing values using pointers...\n");
 *p=100; *q=200; *r=300;
 printf("Now a=%d\n",a);
 printf("Now b=%d\n",b);
 printf("Now c=%d\n",c);
return 0;
 }
```
##5. C program to illustrate pointer arithmetic.
```c
#include<stdio.h>
int main()
{
int a=10;
 int *p=&a;
 printf("Initially, address in p =%p\n",p);
 p=p+1; printf("After p+1, address =%p\n",p);
 p=p+2; printf("After p+2, address =%p\n",p);
 return 0;
}
```
##6. Write a program to declare an integer variable a, assign it a value, then declare a pointer variable, assign it the address of a, 
and finally print the value of a using the pointer variable.
```c
#include<stdio.h>
 int main()
 {
 int a=10;
 int *p;
 p=&a;
 printf("Value of a = %d\n",a);
printf("Value of a using pointer = %d\n",*p);
 return 0;
 }
```
##7. Write a program to print postfix/prefix increment/decrement in a pointer variable of base
```c
#include<stdio.h>
int main()
{
  int a=10, b=10;
  int *p, *q;
  p = &a;
  q = &b;

  printf("Initially, pointer p = %p\n", p);
  p++;   
  printf("After p++ (postfix increment), pointer p = %p\n", p);
  ++p;  
  printf("After ++p (prefix increment), pointer p = %p\n", p);

  printf("Initially, pointer q = %p\n", q);
  q--;  
  printf("After q-- (postfix decrement), pointer q = %p\n", q);
  --q;  
  printf("After --q (prefix decrement), pointer q = %p\n", q);

  return 0;
}
```
##8. Write a Program to print the value and address of elements of an array using pointers notation.
```c
#include<stdio.h>
int main()
{
    int a[5] = {10, 20, 30, 40, 50};
    int *p;
    printf("Array elements and their addresses:\n");
    
    for(p = a; p < a + 5; p++)   
    {
        printf("Value = %d, Address = %p\n", *p, p);
    }
    return 0;
}
```
##9.Write a program to print the value and address of array elements by subscripting  a pointer  
variable. 
```c
#include<stdio.h>
int main()
{
    int a[100],*ptr,size,i;
    printf("Enter size:");
    scanf("%d",&size);
    printf("Enter elements:");
    for(i=0;i<size;i++)
    {
        scanf("%d",&a[i]);
    }
    ptr=a;
    for(i=0;i<size;i++)
    {
    printf("Element %d:Value=%d:Address:%p\n",i,*(ptr+i),(ptr+i));
    }
    return 0;
}
```
##10.Create a function that swaps two numbers using   pointers. 
```c
#include<stdio.h>
int main()
{
    int a,b;
    printf("Enter two numbers:");
    scanf("%d%d",&a,&b);
    printf("\nBefore swapping: a=%d b=%d",a,b);
    int temp,*p,*q;
    p=&a;
    q=&b;
    temp=*p;
    *p=*q;
    *q=temp;
    printf("\nAfter swapping: a=%d b=%d",a,b);
    return 0;
}
```
##11.Implement a function that returns the length of a string using pointers
```c
#include<stdio.h>
#include<string.h>
int main()
{
    char str[100];
    int count=0;
    printf("Enter string:");
    fgets(str,sizeof(str),stdin);
    str[strcspn(str,"\n")]='\0';
    char *p;
    for(p=str;*p!='\0';p++)
    {
        count++;
    }
    printf("length of the string:%d",count);
    
    return 0;
}
```
##12.Develop a function to reverse a string in place using pointers.
```c



