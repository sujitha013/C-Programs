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
##8.Toggle all bits of a given number (within 8 bits).
```c
#include<stdio.h>
int main()
{
    int n,i,bit;
    printf("Enter a number:");
    scanf("%d",&n);
    bit=n^0xFF;
    for(i=7;i>=0;i--)
    {
        printf("%d",(n>>i)&1);
    }
    printf("->%d",n);
    printf("\n");
    for(i=7;i>=0;i--)
    {
        printf("%d",(bit>>i)&1);
    }
    printf("->%d",bit);
    return 0;
}
```
##9.Write a C program to find the position of the lowest set bit (rightmost 1) in the binary representation of a given integer.
```c
#include<stdio.h>
int main()
{
    int n,bit,j,i;
    printf("Enter a number:");
    scanf("%d",&n);
    printf("Binary from of a number:");
    for(i=31;i>=0;i--)
    {
        printf("%d",(n>>i)&1);
    }
    for(i=0;i<32;i++)
    {
      bit=(n>>i)&1;
      if(bit==1)
      {
          j=i;
          break;
      }
      
    }
    printf("\nthe lowestbit position set bit=%d",j);
}
```
##10.Take an array of integers.For each element, print the number of 1’s in its binary representation.Also, find the integer with maximum set bits.
```c
#include<stdio.h>
int main()
{
    int a[100],i,size,count,j,freq[100],k=0,max=0,p;
    printf("Enter size:");
    scanf("%d",&size);
    printf("Enter elements:");
    for(i=0;i<size;i++)
    {
        scanf("%d",&a[i]);
    }
    for(i=0;i<size;i++)
    {
        count=0;
        for(j=31;j>=0;j--)
        {
            if(((a[i]>>j)&1)==1)
            {
                count++;
            }
        }
        freq[k++]=count;
    }
    for(i=0;i<size;i++)
    {
        if(freq[i]>max)
        {
            max=freq[i];
            p=a[i];
            
        }
        printf("%d->%d set bits\n",a[i],freq[i]);
    }
    printf("Number with maximum set bits=%d",p);
}
```
##11.Given an array of integers, print all numbers that have an even number of set bits in their binary representation.
```c
#include<stdio.h>
int main()
{
    int size,a[100],i,count,bit,j;
    printf("Enter size:");
    scanf("%d",&size);
    printf("Enter elements:");
    for(i=0;i<size;i++)
    {
        scanf("%d",&a[i]);
    }
    printf("Number with Even set bits:");
    for(i=0;i<size;i++)
    {
        count=0;
        for(j=31;j>=0;j--)
        {
            bit=((a[i]>>j)&1);
            if(bit==1)
            {
                count++;
            }
        }
        if(count%2==0)
        {
            printf("%d ",a[i]);
        }
    }
  return 0;  
}
```




