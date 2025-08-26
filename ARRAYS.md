##1. Write a program in C to store elements in an array and print them.
```c
#include<stdio.h>
int main()
{
int a[100],i,size;
printf("Enter size:");
scanf("%d",&size);
printf("Enter elements:");
for(i=0;i<size;i++)
{
scanf("%d",&a[i]);
}
printf("Elements in the array:");
for(i=0;i<size;i++)
{
printf("%d ",a[i]);
}
return 0;
}
```
##2. Write a program in C to read n number of values in an array and display them in reverse order.
```c
/*#include<stdio.h>
int main()
{
int a[100],i,size;
printf("Enter size:");
scanf("%d",&size);
printf("Enter elements:");
for(i=0;i<size;i++)
{
scanf("%d",&a[i]);
}
printf("Elements in the array reverse order:");
for(i=size-1;i>=0;i--)
{
printf("%d ",a[i]);
}
return 0;
}```
