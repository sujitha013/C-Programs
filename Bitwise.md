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
