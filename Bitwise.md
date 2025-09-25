##1.Write a program using bitwise operators to count the number of 1 bits in the binary representation of a number.
```c
#include<stdio.h>
int main()
{
    int n,temp,rem,a[100],i=0,j,count=0;
    printf("Enter a number:");
    scanf("%d",&n);
    if(n == 0)
    {
    printf("0");
    printf("\nset bits in a given number=0");
    return 0;
  }

    printf("\nBinary repersentation:");
    temp=n;
    while(temp>0)
    {
     rem=temp%2;
     a[i++]=rem;
     temp=temp/2;
    }
    for(j=0;j<i/2;j++)
    {
        int temp=a[j];
        a[j]=a[i-j-1];
        a[i-j-1]=temp;
    }
    for(j=0;j<i;j++)
    {
        printf("%d",a[j]);
    }
    for(j=0;j<i;j++)
    {
        if(a[j]==1)
        {
            count++;
        }
    }
    printf("\nset bits in a given number=%d",count);
    return 0;
}
```
##2.Find whether the number is odd or even 
```c
#include<stdio.h>
int main()
{
    int n;
    printf("Enter a number:");
    scanf("%d",&n);
    if((n&1)==0)
    {
     printf("The number %d is even\n",n);   
    }
    else
    {
        printf("The number %d is odd\n",n);
    }
    return 0;
}
```
##3.Check if the number is a power of 2
```c
#include<stdio.h>
int main()
{
    int n;
    printf("Enter a number:");
    scanf("%d",&n);
    if((n&(n-1))==0&&(n!=0))
    {
     printf("The number %d is powe of 2",n);   
    }
    else
    {
        printf("The number %d is not power of 2\n",n);
    }
    return 0;
}
```
##4.Can you swap two variables without using a temporary variable? Show the code.
```c
#include<stdio.h>
int main()
{
   int a,b;
   printf("Enter a and b:");
   scanf("%d%d",&a,&b);
   printf("Before swapping:a=%d b=%d\n",a,b);
   a=a^b;
   b=a^b;
   a=a^b;
   printf("After swapping:a=%d b=%d",a,b);
    return 0;
}
```
##5.Swap even-positioned bits with odd-positioned bits of a given number.
```c
#include<stdio.h>
int main()
{
    int n,i,even,odd;
    printf("Enter a number:");
    scanf("%d",&n);
    printf("Before swapped:");
    for(i=31;i>=0;i--)
    {
        printf("%d",(n>>i)&1);
    }
    printf("\n");
    even=(n&0xAAAAAAAA);
    odd=(n&0x55555555);
    int result=(even>>1)|(odd<<1);
    printf("After swapped:");
    for(i=31;i>=0;i--)
    {
        printf("%d",(result>>i)&1);
    }
    return 0;
}
```
##6.Given a number, clear all even-positioned bits.
```c
#include<stdio.h>
int main()
{
    int n,i,bit;
    printf("Enter a number:");
    scanf("%d",&n);
    bit=n;
    for(i=31;i>=0;i--)
    {
        printf("%d",(n>>i)&1);
    }
    printf("->%d",n);
    for(i=31;i>=0;i--)
    {
        if(i%2==0)
        {
           bit=bit&(~(1<<i)); 
        }
    }
    printf("\n");
    for(i=31;i>=0;i--)
    {
        printf("%d",(bit>>i)&1);
    }
    printf("->%d",bit);
    return 0;
}
```
##7.Given a number, set all odd-positioned bits.
```c
#include<stdio.h>
int main()
{
    int n,i,bit;
    printf("Enter a number:");
    scanf("%d",&n);
    bit=n;
    for(i=31;i>=0;i--)
    {
        printf("%d",(n>>i)&1);
    }
    printf("->%d",n);
    for(i=31;i>=0;i--)
    {
        if(i%2==0)
        {
           bit=bit|(1<<i); 
        }
    }
    printf("\n");
    for(i=31;i>=0;i--)
    {
        printf("%d",(bit>>i)&1);
    }
    printf("->%d",bit);
    return 0;
}
```



