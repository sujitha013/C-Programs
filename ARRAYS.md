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
printf("Elements in the array reverse order:");
for(i=size-1;i>=0;i--)
{
printf("%d ",a[i]);
}
return 0;
}
```
##3.Write a program in C to find the sum of all elements of the array
```c
#include<stdio.h>
int main()
{
int a[100],i,size,sum=0;
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
sum=sum+a[i];
}
printf("\nsum of all elements of the array=%d",sum);
return 0;
```
##4.Write a program in C to copy the elements of one array into another array.
```c
#include<stdio.h>
int main()
{
int a[100],i,size,b[i];
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
b[i]=a[i];
}
printf("\nElements that are copied  form other array:");
for(i=0;i<size;i++)
{
printf("%d ",b[i]);
}
return 0;
}
```
##5.Write a program in C to count the total number of duplicate elements in an array.
```c
#include<stdio.h>
int main()
{
    int a[100],i,j,size,count,freq[100],dupcount=0;
    printf("Enter size:");
    scanf("%d",&size);
    printf("Enter elements:");
    for(i=0;i<size;i++)
    {
        scanf("%d",&a[i]);
        freq[i]=-1;
    }
    printf("Elements in the array:");
    for(i=0;i<size;i++)
    {
        printf("%d ",a[i]);
    }
    for(i=0;i<size;i++)
    {
        count=1;
        for(j=i+1;j<size;j++)
        {
           if(a[i]==a[j])
           {
               count++;
               freq[j]=0;
           }
        }
        if(freq[i]!=0)
        {
            freq[i]=count;
        }
    }
    for(i=0;i<size;i++)
    {
        if(freq[i]>1)
        {
            dupcount++;
     dupcount++;
        }
    }
    printf("\nCount of duplicat elements in the array:%d",dupcount);
    return 0;
}
```
##6.Write a program in C to print all unique elements in an array.
```c
#include<stdio.h>
int main()
{
    int a[100],i,j,size,flag;
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
    printf("\nUnique elements in the array:");
    for(i=0;i<size;i++)
    {
        flag=0;
        for(j=i+1;j<size;j++)
        {
           if(a[i]==a[j])
           {
               flag=1;
           }
        }
        if(flag==0)
        {
            printf("%d ",a[i]);
        }
    }

    return 0;
}
```
##7.Write a program in C to merge two arrays of the same size sorted in descending order.
```c
#include<stdio.h>
int main()
{
    int a[100], b[100], c[200];
    int size, i, j, k;

    printf("Enter size of arrays (same size for both): ");
    scanf("%d", &size);

    printf("Enter elements of first array (in descending order): ");
    for(i = 0; i < size; i++)
        scanf("%d", &a[i]);

    printf("Enter elements of second array (in descending order): ");
    for(i = 0; i < size; i++)
        scanf("%d", &b[i]);

    // Merge process (like merge sort, but descending order)
    i = j = k = 0;
    while(i < size && j < size)
    {
        if(a[i] >= b[j])
            c[k++] = a[i++];
        else
            c[k++] = b[j++];
    }

    // Copy remaining elements
    while(i < size)
        c[k++] = a[i++];
    while(j < size)
        c[k++] = b[j++];

    printf("\nMerged array in descending order: ");
    for(i = 0; i < 2*size; i++)
        printf("%d ", c[i]);

    return 0;
}
```
##8.Write a  program in C to count the frequency of each element of an array.
```c
#include<stdio.h>
int main()
{
    int a[100],i,j,size,count,freq[100];
    printf("Enter size :");
    scanf("%d",&size);
    printf("Enter elements :");
    for(i=0;i<size;i++)
    {
        scanf("%d",&a[i]);
        freq[i]=-1;

    }
    for(i=0;i<size;i++)
    {
        count=1;
        for(j=i+1;j<size;j++)
        {
            if(a[j]==a[i])
            {
                count++;
                freq[j]=0;
            }
        }
        if(freq[i]!=0)
        {
            freq[i]=count;
        }
    }
    for(i=0;i<size;i++)
    {
        if(freq[i]!=0)
        {
        printf("%d occurs %d time(s)\n",a[i],freq[i]);
        }

    }

    return 0;
}
```
##9.Write a program in C to find the maximum and minimum elements in an array
```c
#include<stdio.h>
int main()
{
    int a[100],size,min,max,i;
    printf("Enter size:");
    scanf("%d",&size);
    printf("Array elements:");
    for(i=0;i<size;i++)
    {
        scanf("%d",&a[i]);
    }
    min=max=a[0];
    for(i=1;i<size;i++)
    {
      if(a[i]>max)
      {
          max=a[i];
      }
      if(a[i]<min)
      {
          min=a[i];
      }
    }
    printf("Maximum element=%d\nMinimum element=%d",max,min);
    return 0;
}
```
##10.Write a program in C to separate odd and even integers into separate arrays.
```c
#include<stdio.h>
int main()
{
    int a[100],i,odd[100],even[100],size;
    printf("Enter size :");
    scanf("%d",&size);
    printf("Enter elements :");
    for(i=0;i<size;i++)
    {
        scanf("%d",&a[i]);
    }
    int k=0,p=0;
    for(i=0;i<size;i++)
    {
        if(a[i]%2==0)
        {
            even[k++]=a[i];
        }
        else
        {
            odd[p++]=a[i];
        }
    }
    printf("odd elements array:");
    for(i=0;i<p;i++)
    {
        printf("%d ",odd[i]);
    }
    printf("\neven elements array:");
    for(i=0;i<k;i++)
    {
        printf("%d ",even[i]);
    }

    return 0;
}
```
##11.Write a program in C to sort elements of an array in ascending order.
```c
#include<stdio.h>
int main()
{
    int a[100],i,j,temp,size;
    printf("Enter size:");
    scanf("%d",&size);
    printf("Enter elements:");
    for(i=0;i<size;i++)
    {
        scanf("%d",&a[i]);
    }
    for(i=0;i<size;i++)
    {
        for(j=i+1;j<size;j++)
        {
            if(a[j]<a[i])
            {
                temp=a[i];
                a[i]=a[j];
                a[j]=temp;
            }
        }
    }
    printf("\nArray in Ascending Order:");
    for(i=0;i<size;i++)
    {
        printf("%d ",a[i]);
    }
return 0;
}
```
##12.Write a program in C to sort the elements of the array in descending order.
```c
#include<stdio.h>
int main()
{
    int a[100],i,j,temp,size;
    printf("Enter size:");
    scanf("%d",&size);
    printf("Enter elements:");
    for(i=0;i<size;i++)
    {
        scanf("%d",&a[i]);
    }
    for(i=0;i<size;i++)
    {
        for(j=i+1;j<size;j++)
        {
            if(a[j]>a[i])
            {
                temp=a[i];
                a[i]=a[j];
                a[j]=temp;
            }
        }
    }
    printf("\nArray in descending Order:");
    for(i=0;i<size;i++)
    {
        printf("%d ",a[i]);
    }
return 0;
}
```
##13.Write a program in C to delete an element at a desired position from an array.
```c
#include<stdio.h>
int main()
{
    int a[100],i,pos,size;
    printf("Enter size:");
    scanf("%d",&size);
    printf("Enter elements:");
    for(i=0;i<size;i++)
    {
        scanf("%d",&a[i]);
    }
    printf("\nElements in the array:");
    for(i=0;i<size;i++)
    {
        printf("%d ",a[i]);
    }
    printf("\nEnter position to delete:");
    scanf("%d",&pos);
    if(pos<=0||pos>size)
    {
        printf("Invalid postion.");
        return 0;
    }
    for(i=pos-1;i<size;i++)
    {
        a[i]=a[i+1];
    }
    size--;
    printf("\nArray after deletion: ");
    for(i=0;i<size;i++)
    {
        printf("%d ",a[i]);
    }
    return 0;
}
```
##14.Write a program in C to find the second largest element in an array.
```c
#include<stdio.h>
#include<limits.h>
int main()
{
    int a[100],i,max=INT_MIN,secondmax=INT_MIN,size;
    printf("Enter size:");
    scanf("%d",&size);
    printf("Enter elements:");
    for(i=0;i<size;i++)
    {
        scanf("%d",&a[i]);
    }
    printf("\nElements in the array:");
    for(i=0;i<size;i++)
    {
        printf("%d ",a[i]);
    }
    for(i=0;i<size;i++)
    {
        if(a[i]>max)
        {
            secondmax=max;
            max=a[i];
        }
        else if((a[i]>secondmax)&&(a[i]<max))
        {
            secondmax=a[i];
        }
    }
    if(secondmax==INT_MIN)
    {
        printf("\nnot found such element.");
    }
    else
    {
        printf("\nsecond largest element=%d",secondmax);
    }
return 0;
}
```
##15.Write a program in C to find the second smallest element in an array.
```c
#include<stdio.h>
#include<limits.h>
int main()
{
int a[100],i,size,min=INT_MAX,secondmin=INT_MAX;
printf("Enter size:");
scanf("%d",&size);
printf("Enter elements:");
for(i=0;i<size;i++)
{
scanf("%d",&a[i]);
}
for(i=0;i<size;i++)
{
if(a[i]<min)
{
secondmin=min;
min=a[i];
}
else if(a[i]<secondmin&&a[i]>min)
{
secondmin=a[i];
}
}
if(secondmin==INT_MAX)
{
printf("\nNot found such element");
}
else
{
printf("second smallest element=%d",secondmin);
}
return 0;
}
```
##16.Write a program in C for a 2D array of size 3x3 and print the matrix.
```c
#include<stdio.h>
int main()
{
    int a[3][3],i,j;
    printf("Enter elements of 3X3 matrix:");
    for(i=0;i<3;i++)
    {
        for(j=0;j<3;j++)
        {
            scanf("%d",&a[i][j]);
        }
    }
    printf("Elements in 3X3 matrix:\n");
    for(i=0;i<3;i++)
    {
        for(j=0;j<3;j++)
        {
            printf("%d ",a[i][j]);
        }
        printf("\n");
    }
    return 0;
}
```
##17.Write a program in C for adding two matrices of the same size.
```c
#include<stdio.h>
int main()
{
    int rows,cols;
    printf("Enter rows and cols:");
    scanf("%d%d",&rows,&cols);
    int a[rows][cols],i,j,b[rows][cols],c[rows][cols];
    printf("Enter elements of first matrix:");
    for(i=0;i<rows;i++)
    {
        for(j=0;j<cols;j++)
        {
            scanf("%d",&a[i][j]);
        }
    }
    printf("\nEnter elements of second matrix:");
    for(i=0;i<rows;i++)
    {
        for(j=0;j<cols;j++)
        {
            scanf("%d",&b[i][j]);
        }
    }
    for(i=0;i<rows;i++)
    {
        for(j=0;j<cols;j++)
        {
            c[i][j]=a[i][j]+b[i][j];
        }
    }
    printf("Sum of two matrices:\n");
    for(i=0;i<rows;i++)
    {
        for(j=0;j<cols;j++)
        {
            printf("%d ",c[i][j]);
        }
    printf("\n");
    }
    return 0;
}
```
##18.Write a program in C for the subtraction of two matrices.
```c
#include<stdio.h>
int main()
{
    int rows,cols;
    printf("Enter rows and cols:");
    scanf("%d%d",&rows,&cols);
    int a[rows][cols],i,j,b[rows][cols],c[rows][cols];
    printf("Enter elements of first matrix:");
    for(i=0;i<rows;i++)
    {
        for(j=0;j<cols;j++)
        {
            scanf("%d",&a[i][j]);
        }
    }
    printf("\nEnter elements of second matrix:");
    for(i=0;i<rows;i++)
    {
        for(j=0;j<cols;j++)
        {
            scanf("%d",&b[i][j]);
        }
    }
    for(i=0;i<rows;i++)
    {
        for(j=0;j<cols;j++)
        {
            c[i][j]=a[i][j]-b[i][j];
        }
    }
    printf("Subtraction of two matrices:\n");
    for(i=0;i<rows;i++)
    {
        for(j=0;j<cols;j++)
        {
            printf("%d ",c[i][j]);
        }
        printf("\n");
    }
return 0;
}
```
##19.Write a program in C for the multiplication of two square matrices.
```c
#include<stdio.h>
int main()
{
    int rows,cols;
    printf("Enter rows and cols:");
    scanf("%d%d",&rows,&cols);
    int a[rows][cols],i,j,b[rows][cols],c[rows][cols],k;
    printf("Enter elements of first matrix:");
    for(i=0;i<rows;i++)
    {
        for(j=0;j<cols;j++)
        {
            scanf("%d",&a[i][j]);
        }
    }
    printf("\nEnter elements of second matrix:");
    for(i=0;i<rows;i++)
    {
        for(j=0;j<cols;j++)
        {
            scanf("%d",&b[i][j]);
        }
    }
    for(i = 0; i < n; i++)
    {
        for(j = 0; j < n; j++)
        {
            c[i][j] = 0;
            for(k = 0; k < n; k++)
            {
                c[i][j] += a[i][k] * b[k][j];
            }
        }
    }


    printf("Multiplication of two matrices:\n");
    for(i=0;i<rows;i++)
 for(i=0;i<rows;i++)
    {
        for(j=0;j<cols;j++)
        {
            printf("%d ",c[i][j]);
        }
        printf("\n");
    }
    return 0;
}
```
##20.Write a program in C to find the transpose of a given matrix.
```c
#include<stdio.h>
int main()
{
    int rows,cols;
    printf("Enter rows and cols:");
    scanf("%d%d",&rows,&cols);
    int a[rows][cols],i,j;
    printf("Enter elements of  matrix:");
    for(i=0;i<rows;i++)
    {
        for(j=0;j<cols;j++)
        {
            scanf("%d",&a[i][j]);
        }
    }
    printf("Transopse of the  matrix:\n");
    for(i=0;i<cols;i++)
    {
        for(j=0;j<rows;j++)
        {
            printf("%d ",a[j][i]);
        }
        printf("\n");
    }


    return 0;
}
```
##21.Write a program in C to find the sum of the right diagonals of a matrix.
```c
#include<stdio.h>
int main()
{
    int rows,cols;
    printf("Enter rows and cols:");
    scanf("%d%d",&rows,&cols);
    int a[rows][cols],i,j,sum=0;
    printf("Enter elements of %dX%d matrix:",rows,cols);
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
            if(i+j==cols-1)
            {
                sum=sum+a[i][j];
            }
        }
    }
    printf("\nSum of right diagonal=%d",sum);
    return 0;
}
```
##22.Write a program in C to find the sum of the left diagonals of a matrix.
```c
#include<stdio.h>
int main()
{
    int rows,cols;
    printf("Enter rows and cols:");
    scanf("%d%d",&rows,&cols);
    int a[rows][cols],i,j,sum=0;
    printf("Enter elements of %dX%d matrix:",rows,cols);
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
            if(i==j)
            {
                sum=sum+a[i][j];
            }
        }
    }
    printf("\nSum of left diagonal=%d",sum);
    return 0;
}
```
##23.Write a program in C to find the sum of rows and columns of a matrix.
```c
#include<stdio.h>
int main()
{
    int rows,cols;
    printf("Enter rows and cols:");
    scanf("%d%d",&rows,&cols);
    int a[rows][cols],i,j,rowsum,colsum;
    printf("Enter elements of %dX%d matrix:",rows,cols);
    for(i=0;i<rows;i++)
    {
        for(j=0;j<cols;j++)
        {
            scanf("%d",&a[i][j]);
        }
    }
    for(i=0;i<rows;i++)
    {
        rowsum=0;
        for(j=0;j<cols;j++)
        {
           rowsum=rowsum+a[i][j];
        }
        printf("Sum of row %d = %d\n", i+1, rowsum);
    }
    for(j=0;j<cols;j++)
    {
        colsum=0;
        for(i=0;i<rows;i++)
        {
           colsum=colsum+a[i][j];
        }
        printf("Sum of column %d = %d\n", j+1, colsum);
    }

    return 0;
}
```
##24.Write a program in C to print or display the lower triangular of a given matrix.
```c
#include<stdio.h>
int main()
{
    int n,i,j;
    printf("Enter order of square matrix: ");
    scanf("%d",&n);

    int a[n][n];
    printf("Enter elements of %dX%d matrix:\n",n,n);
    for(i=0;i<n;i++)
    {
        for(j=0;j<n;j++)
        {
            scanf("%d",&a[i][j]);
        }
    }

    printf("\nLower Triangular Matrix:\n");
    for(i=0;i<n;i++)
    {
        for(j=0;j<n;j++)
        {
            if(i >= j)
                printf("%d ", a[i][j]);
            else
                printf("0 ");   // or leave space
        }
        printf("\n");
    }

    return 0;
}
```
##25.Write a program in C to print or display an upper triangular matrix.
```c
#include<stdio.h>
int main()
{
    int n,i,j;
    printf("Enter order of square matrix: ");
    scanf("%d",&n);

    int a[n][n];
    printf("Enter elements of %dX%d matrix:\n",n,n);
    for(i=0;i<n;i++)
    {
        for(j=0;j<n;j++)
        {
            scanf("%d",&a[i][j]);
        }
    }

    printf("\nupper Triangular Matrix:\n");
    for(i=0;i<n;i++)
    {
        for(j=0;j<n;j++)
        {
            if(i <= j)
                printf("%d ", a[i][j]);
            else
                printf("0 ");   // or leave space
        }
        printf("\n");
    }

    return 0;
}
```
##26.Write a C program to rotate an N x N matrix 90° clockwise.
```c
#include<stdio.h>
int main()
{
    int rows,cols;
    printf("Enter rows and cols:");
    scanf("%d%d",&rows,&cols);
    int a[rows][cols],i,j,b[cols][rows];
    printf("Enter elements:");
    for(i=0;i<rows;i++)
    {
        for(j=0;j<cols;j++)
        {
            scanf("%d",&a[i][j]);
        }
    }
    for(j=0;j<cols;j++)
    {
        for(i=0;i<rows;i++)
        {
           b[j][i]=a[i][j];
        }
        printf("\n");
    }
    for(i=0;i<cols;i++)
    {
         int start=0;
        int end=rows-1;
        while(start<end)
            {
                int temp=b[i][start];
                b[i][start]=b[i][end];
                b[i][end]=temp;
        start++;
        end--;
         }
    }
    for(i=0;i<cols;i++)
    {
        for(j=0;j<rows;j++)
        {
            printf("%d ",b[i][j]);
        }
        printf("\n");
    }
    return 0;
}
```
##27.Write a program in C to accept two matrices and check whether they are equal.
```c
#include<stdio.h>
int main()
{
    int rows,cols;
    printf("Enter rows and cols:");
    scanf("%d%d",&rows,&cols);
    int a[rows][cols],b[rows][cols],i,j;
    printf("Enter elements of first %dX%d matrix:",rows,cols);
    for(i=0;i<rows;i++)
    {
        for(j=0;j<cols;j++)
        {
            scanf("%d",&a[i][j]);
        }
    }
    printf("Enter elements of second %dX%d matrix:",rows,cols);
    for(i=0;i<rows;i++)
    {
        for(j=0;j<cols;j++)
        {
            scanf("%d",&b[i][j]);
        }
    }
    for(i=0;i<rows;i++)
    {
        for(j=0;j<cols;j++)
        {
            if(a[i][j]!=b[i][j])
            {
                printf("both matrices are not equal.");
                return 0;
            }
        }
    }
    printf("both matrices are equal.");
    return 0;
}
```
##28.Write a program in C to find the majority element of an array.
```c
#include<stdio.h>
int main()
{
    int a[100],i,j,freq[100],count,size;
    printf("Enter size:");
    scanf("%d",&size);
    int arr=size/2;
    printf("Enter elements:");
    for(i=0;i<size;i++)
    {
        scanf("%d",&a[i]);
        freq[i]=-1;
    }
    for(i=0;i<size;i++)
    {
        count=1;
        for(j=i+1;j<size;j++)
        {
            if(a[j]==a[i])
            {
                count++;
                freq[j]=0;
            }
        }
        if(freq[i]!=0)
        {
            freq[i]=count;
        }
    }
    for(i=0;i<size;i++)
    {
        if(freq[i]>arr)
        {
            printf("Majority element = %d",a[i]);
            return 0;
        }
    }
    printf("\nNot found such element.");
    return 0;
}
```
##29.Write a program in C to find the missing number in a given array. There are no duplicates in the list.
```c
#include<stdio.h>
int main()
{
    int a[100],size,i,total,miss,sum=0;
    printf("Enter size:");
    scanf("%d",&size);
    total=size*(size+1)/2;
    printf("Enter elements:");
    for(i=0;i<size;i++)
    {
        scanf("%d",&a[i]);
    }
    for(i=0;i<size-1;i++)
    {
        sum=sum+a[i];
    }
    miss=total-sum;
    printf("The missing number:%d",miss);
    return 0;
}
```
##30.Write a program in C to find the two repeating elements in a given array.
```c
#include<stdio.h>
int main()
{
    int a[100],size,i,j,freq[100],count,found=0;
    printf("Enter size:");
    scanf("%d",&size);
    printf("Enter elements:");
    for(i=0;i<size;i++)
    {
        scanf("%d",&a[i]);
        freq[i]=-1;
    }
    for(i=0;i<size;i++)
    {
       count=1;
       for(j=i+1;j<size;j++)
       {
           if(a[j]==a[i])
           {
           count++;
           freq[j]=0;
           }
       }
       if(freq[i]!=0)
       {
           freq[i]=count;
       }
    }
      printf("\nThe repeating elements are:");
    for(i=0;i<size;i++)
    {
        if(freq[i]>1)
        {
          printf("%d ",a[i]);
          found++;
          if(found==2)
          break;
        }
    }
return 0;
}
```
##31.Write a program to check if a given element is present in an array.
```c
#include<stdio.h>
int main()
{
    int a[100],size,i,j,search;
    printf("Enter size:");
    scanf("%d",&size);
    printf("Enter elements:");
    for(i=0;i<size;i++)
    {
        scanf("%d",&a[i]);
    }
    printf("Enter element to search:");
    scanf("%d",&search);
    for(i=0;i<size;i++)
    {
        if(a[i]==search)
        {
            printf("Element %d is present in the array.",search);
            return 0;
        }
    }
    printf("Element %d is not present in the array.",search);
    return 0;
}
```
##32.Create a function to calculate the average of elements in an array
```c
#include<stdio.h>
float avg_of_the_array(int[],int);
int main()
{
    int a[100],size,i;
    float average;
    printf("Enter size:");
    scanf("%d",&size);
    printf("Enter elements:");
    for(i=0;i<size;i++)
    {
        scanf("%d",&a[i]);
    }
    average=avg_of_the_array(a,size);
    printf("Average of array elements =%.2f",average);
    return 0;
}
float avg_of_the_array(int a[],int size)
{
    int i;
    float av,sum=0.0;
    for(i=0;i<size;i++)
    {
        sum=sum+a[i];
    }
    av=sum/(float)size;
    return av;
}
```
##33.Write a program to count the number of even and odd elements in an array.
```c
#include<stdio.h>
int main()
{
    int a[100],size,i,evencount=0,oddcount=0;
    printf("Enter size:");
    scanf("%d",&size);
    printf("Enter elements:");
    for(i=0;i<size;i++)
    {
        scanf("%d",&a[i]);
    }
    for(i=0;i<size;i++)
    {
        if(a[i]%2==0)
        {
            evencount++;
        }
        else
        {
            oddcount++;
        }
    }
    printf("\nNumber of even elements:%d",evencount);
    printf("\nNumber of odd elements:%d",oddcount);
    return 0;
}
```
##34.Implement a function to reverse the elements of an array.
```c
#include<stdio.h>
int reversearray(int[],int);
int main()
{
    int a[100],size,i;
    printf("Enter size:");
    scanf("%d",&size);
    printf("Enter elements:");
    for(i=0;i<size;i++)
    {
        scanf("%d",&a[i]);
    }
    reversearray(a,size);
    return 0;
}
int reversearray(int a[],int size)
{
    int i,temp;
    for(i=0;i<size/2;i++)
    {
       temp=a[i];
       a[i]=a[size-i-1];
       a[size-i-1]=temp;
    }
    printf("\nReversed array:");
    for(i=0;i<size;i++)
    {
        printf("%d ",a[i]);
    }
}
```
##35.Implement a function to delete an element at a specific position in an array.
```c
#include<stdio.h>
int deleteposition(int[],int);
int main()
{
    int a[100],size,i;
    printf("Enter size:");
    scanf("%d",&size);
    printf("Enter elements:");
    for(i=0;i<size;i++)
    {
        scanf("%d",&a[i]);
    }
    deleteposition(a,size);
    return 0;
}
int deleteposition(int a[],int size)
{
    int i,pos;
    printf("Enter position to delete:");
    scanf("%d",&pos);
    if(pos<1||pos>size)
    {
        printf("Invalid position!");
        return 0;
    }
    for(i=pos-1;i<size-1;i++)
    {
       a[i]=a[i+1];
    }
    size--;
    printf("\nReversed array:");
    for(i=0;i<size;i++)
    {
        printf("%d ",a[i]);
    }
}
```
## 36.Write a function to find the product of all elements in an array.
```c
#include<stdio.h>
long long productarray(int[],int);
int main()
{
    int a[100],i,size;
    long long p;
    printf("Enter size:");
    scanf("%d",&size);
    printf("Enter elements:");
    for(i=0;i<size;i++)
    {
        scanf("%d",&a[i]);
    }
    p=productarray(a,size);
    printf("Product of array elements=%lld",p);
    return 0;
}
long long productarray(int a[],int size)
{
    int i;long long pod=1;
    for(i=0;i<size;i++)
    {
        pod*=a[i];
    }
    return pod;
}
```
##37.Print Square of Array Elements in C.
```c
#include<stdio.h>
#include<math.h>
int main()
{
    int a[100],i,size,b[100];
    printf("Enter size:");
    scanf("%d",&size);
    printf("Enter elements:");
    for(i=0;i<size;i++)
    {
        scanf("%d",&a[i]);
    }
    for(i=0;i<size;i++)
    {
        b[i]=pow(a[i],2);
    }
    printf("\nSquares of array elements:");
    for(i=0;i<size;i++)
    {
        printf("%d ",b[i]);
    }
    return 0;
}
```
##38.Print Ascii Values using Array in C
```c
#include<stdio.h>
int main()
{
    char a[100];
    int i,size;
    printf("Enter size:");
    scanf(" %d",&size);
    printf("Enter elements:");
    for(i=0;i<size;i++)
    {
        scanf(" %c",&a[i]);
    }
    printf("ASCII values:");
    for(i=0;i<size;i++)
    {
        printf("%d ",a[i]);
    }
    return 0;
}
```
##39.write C Program To Find Two Elements whose Sum is Closest to Zero.
```c
#include<stdio.h>
#include<stdlib.h>
int main()
{
      int i,j,size,a[100],sum=0,minsum,e1,e2;
    printf("Enter size:");
    scanf(" %d",&size);
    printf("Enter elements:");
    for(i=0;i<size;i++)
    {
        scanf("%d",&a[i]);
    }
    minsum=a[0]+a[1];
    e1=a[0];
    e2=a[1];

    for(i=0;i<size;i++)
    {
       for(j=i+1;j<size;j++)
       {
           sum=a[i]+a[j];
           if(abs(sum)<abs(minsum))
           {
             minsum=sum;
             e1=a[i];
             e2=a[j];
           }
       }
    }
    printf("Two elements whose sum is closest to zero:%d and %d\nsum=%d",e1,e2,minsum);
    return 0;
}
```
##40.C Program to Find Union and Intersection of Two Arrays
```c
#include<stdio.h>

int main()
{
    int i, j, size1, size2, a[100], b[100], flag;

    // Input first array
    printf("Enter size of first array: ");
    scanf("%d", &size1);
    printf("Enter elements of first array: ");
    for(i = 0; i < size1; i++)
        scanf("%d", &a[i]);

    // Input second array
    printf("Enter size of second array: ");
    scanf("%d", &size2);
    printf("Enter elements of second array: ");
    for(i = 0; i < size2; i++)
        scanf("%d", &b[i]);

    // UNION
    printf("\nUnion of two arrays: ");
    for(i = 0; i < size1; i++)
        printf("%d ", a[i]);

    for(i = 0; i < size2; i++) {
        flag = 0;
        for(j = 0; j < size1; j++) {
            if(b[i] == a[j]) {
                flag = 1;
                break;
            }
        }
        if(flag == 0)
            printf("%d ", b[i]);
    }

    // INTERSECTION
    printf("\nIntersection of two arrays: ");
 printf("\nIntersection of two arrays: ");
    for(i = 0; i < size2; i++) {
        for(j = 0; j < size1; j++) {
            if(b[i] == a[j]) {
                printf("%d ", b[i]);
                break; // avoid duplicate prints
            }
        }
    }

    return 0;
}
```
##41.C Program to Print all Non Repeated Elements in an Array
```c
#include<stdio.h>
int main()
{
    int a[100],i,j,count,size,freq[100];
    printf("Enter size:");
    scanf("%d",&size);
    printf("Enter elements:");
    for(i=0;i<size;i++)
    {
        scanf("%d",&a[i]);
        freq[i]=-1;
    }
    for(i=0;i<size;i++)
    {
       count=1;
        for(j=i+1;j<size;j++)
        {
            if(a[j]==a[i])
            {
                count++;
                freq[j]=0;
            }
        }
        if(freq[i]!=0)
        {
            freq[i]=count;
        }
    }
    printf("\nNon-repeated elements are:");
    for(i=0;i<size;i++)
    {
        if(freq[i]==1)
        {
            printf("%d ",a[i]);
        }
    }
    return 0;
}
```
##42.Write a program to write all the elements of 2-D Array into !-D Array in row wise.
```c
#include<stdio.h>
int main()
{
    int rows,cols;
    printf("Enter rows and cols:");
    scanf("%d%d",&rows,&cols);
    int a[rows][cols],i,j,size,b[100],k=0;
    printf("Enter elements of %d-D matrix:",rows);
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
        b[k++]=a[i][j];
        }
    }
    printf("\n1-D array in row-wise order:");
    for(i=0;i<k;i++)
    {
        printf("%d ",b[i]);
    }


    return 0;
}
```
##43.Write a program to write whether a matrix is symmetric or not
```c
#include<stdio.h>
int main()
{
    int rows,cols;
    printf("Enter rows and cols:");
    scanf("%d%d",&rows,&cols);
    if(rows != cols)
    {
    printf("Matrix must be square to check symmetry.\n");
    return 0;
    }

    int a[rows][cols],b[rows][cols],i,j;
    printf("Enter elements of %dX%d matrix:",rows,cols);
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
            b[j][i]=a[i][j];
        }
    }
    for(i=0;i<rows;i++)
    {
        for(j=0;j<cols;j++)
        {
           if(a[i][j]!=b[i][j])
           {
               printf("The matrix is not symmetric.");
               return 0;
           }
 }
    }
    printf("\nThe matrix is symmetric.");
    return 0;
}
```
##44.Write a program to check if elements of an array are distinct or not.
```c
#include<stdio.h>
int main()
{
    int a[100],freq[100],count,i,j,size;
    printf("Enter size:");
    scanf("%d",&size);
    printf("Enter elements:");
    for(i=0;i<size;i++)
    {
    scanf("%d",&a[i]);
    freq[i]=-1;
    }
    for(i=0;i<size;i++)
    {
        count=1;
        for(j=i+1;j<size;j++)
        {
            if(a[j]==a[i])
            {
            count++;
            freq[j]=0;
            }
        }
       if(freq[i]!=0)
       {
           freq[i]=count;
       }
    }
    for(i=0;i<size;i++)
    {
        if(freq[i]!=1)
        {
            printf("Array has duplicate elements.");
            return 0;
        }
    }
    printf("\nAll elements are distinct.");
    return 0;
}
```
##45.Write a program to remove duplicate elements from a sorted array.
```c
#include<stdio.h>
int main()
{
    int a[100],i,size,j=0;
    printf("Enter size:");
    scanf("%d",&size);
    printf("Enter elements:");
    for(i=0;i<size;i++)
    {
        scanf("%d",&a[i]);
    }
    for(i=0;i<size-1;i++)
    {
        if(a[i]!=a[i+1])
        {
            a[j++]=a[i];
        }
    }
    a[j++]=a[size-1];
    printf("\nArray after removing duplicates: ");
    for(i=0;i<j;i++)
    {
        printf("%d ",a[i]);
    }
    return 0;
}
```
##46.Write a program to find out whether a square matrix is symmetric or not. A square matrixis symmetric if the transpose of the matrix is equal to the matrix.
```c
#include <stdio.h>
int main() {
    int n, i, j;
    printf("Enter order of square matrix: ");
    scanf("%d", &n);

    int a[n][n];
    printf("Enter elements of %dx%d matrix:\n", n, n);
    for (i = 0; i < n; i++) {
        for (j = 0; j < n; j++) {
            scanf("%d", &a[i][j]);
        }
    }

    // Check symmetry
    for (i = 0; i < n; i++) {
        for (j = i + 1; j < n; j++) { // Only check elements above diagonal
            if (a[i][j] != a[j][i]) {
                printf("The matrix is not symmetric.\n");
                return 0;
            }
        }
    }

    printf("The matrix is symmetric.\n");
    return 0;
}
```
##47.Write a C program to rotate an array of integers to the right by k positions.
```c
#include<stdio.h>
int main()
{
    int a[100],i,j,n,k,temp;
    printf("Enter n:");
    scanf("%d",&n);
    printf("Enter elements:");
    for(i=0;i<n;i++)
    {
        scanf("%d",&a[i]);
    }
    printf("Enter k:");
    scanf("%d",&k);
    k=k%n;
    for(i=0;i<n/2;i++)
    {
       temp=a[i];
       a[i]=a[n-i-1];
       a[n-i-1]=temp;
    }
    for(i=0;i<k/2;i++)
    {
        temp=a[i];
        a[i]=a[k-i-1];
        a[k-i-1]=temp;
    }
    for(i=0;i<(n-k)/2;i++)
    {
        temp=a[k+i];
        a[k+i]=a[n-(k-i)-1];
        a[n-(k-i)-1]=temp;
    }
    printf("\nOutput:");
    for(i=0;i<n;i++)
    {
        printf("%d ",a[i]);
    }
    
}
```
##48.Write a C program to perform binary search on an array.
```c
#include<stdio.h>
int main()
{
    int n;
    printf("Enter size:");
    scanf("%d",&n);
    int a[n],left=0,right=n-1,mid,search,i,found=0;
    printf("\nEnter elements:");
    for(i=0;i<n;i++)
    {
        scanf("%d",&a[i]);
    }
    printf("\nEnter element to search:");
    scanf("%d",&search);
    while(left<=right)
    {
        mid=(left+right)/2;
        if(search==a[mid])
        {
            printf("\nElement Found at index %d",mid);
            found=1;
            break;
        }
        else if(search<a[mid])
        {
            right=mid-1;
        }
        else if(search>a[mid])
        {
            left=mid+1;
        }
    }
    if(found==0)
    {
        printf("\nElement not found.");
    }
    return 0;
}
```
##49.Read two sorted arrays and merge them into a single sorted array.
```c
#include<stdio.h>
 int main()
 {
int a[100],b[100],c[100],size1,size2,i,j,temp;
 printf("Enter size of first array:");
scanf("%d",&size1);
printf("\nEnter first array elements:");
for(i=0;i<size1;i++)
 {
scanf("%d",&a[i]);
 c[i]=a[i];
 }
printf("\nEnter size of second array:");
 scanf("%d",&size2);
printf("\nEnter second array elements:");
 for(i=0;i<size2;i++)
 {
scanf("%d",&b[i]);
 c[size1+i]=b[i];
 }
for(i=0;i<size1+size2;i++)
 {
for(j=i+1;j<size1+size2;j++)
{
if(c[j]<c[i])
{
temp=c[i];
 c[i]=c[j];
c[j]=temp;
  }
   }
     }
 printf("\nmerged array:");
 for(i=0;i<size1+size2;i++)
 {
printf("%d ",c[i]);
 }
return 0;
 }
```
50.Write a C program to reverse an array using a function.
```c
#include<stdio.h>
 int reversearray(int[],int);
 int main()
{
 int a[100],size,i;
 printf("Enter size:");
scanf("%d",&size);
 printf("\nEnter elements:");
 for(i=0;i<size;i++)
 {
scanf("%d",&a[i]);
}
 reversearray(a,size); return 0;
 }
int reversearray(int a[],int size)
{
int temp,i;
 for(i=0;i<size/2;i++)
 {
temp=a[i];
 a[i]=a[size-i-1];
 a[size-i-1]=temp;
 }
printf("\nReversed array:");
 for(i=0;i<size;i++)
 {
 printf("%d ",a[i]);
}
 }
 ```
##51.Given an array where every number occurs twice except one, find that single number using bitwise XOR.
```c
#include<stdio.h>
int main()
{
    int a[100],i,result=0,size;
    printf("Enter size:");
    scanf("%d",&size);
    printf("Enter elements:");
    for(i=0;i<size;i++)
    {
        scanf("%d",&a[i]);
    }
    for(i=0;i<size;i++)
    {
        result=result^a[i];
    }
    printf("\nSingle element=%d",result);
    return 0;
}
```
##52.Write a program to input a matrix and print only the boundary elements (first row, last row, first column, last column).
```c
#include<stdio.h>
int main()
{
    int rows,cols;
    printf("Enter rows and cols:");
    scanf("%d%d",&rows,&cols);
    int i,j,a[rows][cols];
    printf("Enter elements:");
    for(i=0;i<rows;i++)
    {
        for(j=0;j<cols;j++)
        {
            scanf("%d",&a[i][j]);
        }
    }
    for(j=0;j<cols;j++)
     printf("%d ",a[0][j]);
     for(i=1;i<rows;i++)
     printf("%d ",a[i][cols-1]);
     if(rows>1)
     {
     for(j=cols-2;j>=0;j--)
     printf("%d ",a[rows-1][j]);
     }
     if(cols>1)
     {
         for(i=rows-2;i>0;i--)
         printf("%d ",a[i][0]);
     }
            
            
   return 0;
}
```
##53.Read an array of size n and an integer sum. Count the number of pairs in the array whose sum equals the given value.
```c
#include<stdio.h>
int main()
{
    int a[100],i,j,size,sum,count=0;
    printf("Enter size:");
    scanf("%d",&size);
    printf("Enter elements:");
    for(i=0;i<size;i++)
    {
        scanf("%d",&a[i]);
    }
    printf("Enter sum:");
    scanf("%d",&sum);
    for(i=0;i<size;i++)
    {
        for(j=i+1;j<size;j++)
        {
            if(a[i]+a[j]==sum)
            {
                count++;
            }
        }
    }
    printf("Number of pairs=%d",count);
    return 0;
}
```
##54.Write a C program to generate and print all subarrays of a given array.
```c
#include<stdio.h>
int main()
{
int a[100],i,n,j,k;
printf("Enter size:");
scanf("%d",&n);
printf("Enter elements:");
for(i=0;i<n;i++)
{
scanf("%d",&a[i]);
}
printf("Subarrays of given array:\n");
for(i=0;i<n;i++)
{
for(j=i;j<n;j++)
{
for(k=i;k<=j;k++)
{
printf("%d ",a[k]);
}
printf("\n");
}
}
return 0;
}
```
##55.Write a program to input an array and find the product of all elements except self for each position.
```c
#include<stdio.h>
int main()
{
    int a[100],i,size,pod,b[100],k=0,j;
    printf("Enter size:");
    scanf("%d",&size);
    printf("Enter elements:");
    for(i=0;i<size;i++)
    {
        scanf("%d",&a[i]);
    }
    for(i=0;i<size;i++)
    {
        pod=1;
        for(j=0;j<size;j++)
        {
            if(i!=j)
            {
                pod=pod*a[j];
            }
        }
         b[k++]=pod;
    }
    for(i=0;i<k;i++)
    {
        printf("%d ",b[i]);
    }
    return 0;
}
```
##56.Write a program to print all leaders in an array.
```c
#include<stdio.h>
 int main()
 {
int a[100],i,j,size,flag;
 printf("Enter size:");
 scanf("%d",&size);
 printf("Enter elements:");
 for(i=0;i<size;i++)
 {
scanf("%d",&a[i]);
 }
for(i=0;i<size;i++)
 {
 flag=1;
 for(j=i+1;j<size;j++)
 {
if(a[j]>a[i])
 {
flag=0;
break;
 }
 }
if(flag)
{
printf("%d ",a[i]);
 }
 }
return 0;
 }
```
##57.Given an array of integers, find the first missing positive number.
```c
#include<stdio.h>
int main()
{
    int a[100],i,n,j,temp,found;
    printf("Enter n:");
    scanf("%d",&n);
    printf("Enter elements:");
    for(i=0;i<n;i++)
    {
        scanf("%d",&a[i]);
    }
    for(i=0;i<n;i++)
    {
        for(j=i+1;j<n;j++)
        {
            if(a[j]<a[i])
            {
                temp=a[i];
                a[i]=a[j];
                a[j]=temp;
            }
        }
    }
    for(i=a[0];i<=a[n-1];i++)
    {
        found=0;
        for(j=0;j<n;j++)
        {
            if(a[j]==i)
            {
               found=1;
                break;
            }
        }
        if(!found)
        {
            if(i>0)
            {
            printf("%d ",i);
            break;
            }
        }
    }
   return 0; 
}
```
##58.Given an array of size n, rearrange the array in such a way that:
.The first element is the maximum,
.The second element is the minimum,
.The third is the second maximum,
.The fourth is the second minimum, and so on…
```c
#include<stdio.h>
int main()
{
    int a[100],i,j,size,start=0,res[100],k=0;
    printf("Enter size:");
    scanf("%d",&size);
    int end=size-1;
    printf("Enter elements:");
    for(i=0;i<size;i++)
    {
        scanf("%d",&a[i]);
    }
    for(i=0;i<size;i++)
    {
        for(j=i+1;j<size;j++)
        {
            if(a[j]<a[i])
            {
                int temp=a[i];
                a[i]=a[j];
                a[j]=temp;
            }
        }
    }
    while(start<=end)
    {
        res[k++]=a[end--];
        if(start<=end)
        {
            res[k++]=a[start++];
            
        }
       
    }
    for(i=0;i<k;i++)
    {
        printf("%d ",res[i]);
    }
    return 0;
}
```
##59.Find the first element in the array that repeats.
```c
#include<stdio.h>
int main()
{
    int a[100],i,j,size,flag;
    printf("Enter size:");
    scanf("%d",&size);
    printf("Enter elements:");
    for(i=0;i<size;i++)
    {
        scanf("%d",&a[i]);
    }
    for(i=0;i<size;i++)
    {
        flag=0;
        for(j=i+1;j<size;j++)
        {
            if(a[j]==a[i])
            {
               flag=1;
               break;
            }
        }
        if(flag)
        {
            printf("First repeating element= %d",a[i]);
            return 0;
        }
    }
    printf("No repeating element.\n");
    return 0;
}
```
##60.Write a C program that takes an unsorted array of integers and finds the longest consecutive subsequence.
```c
#include<stdio.h>
int main()
{
    int a[100], size, temp, i, j, count=1, max=1, start=0, bestStart=0;
    printf("Enter size: ");
    scanf("%d",&size);

    printf("Enter elements: ");
    for(i=0;i<size;i++)
        scanf("%d",&a[i]);

    // Sort the array
    for(i=0;i<size;i++)
    {
        for(j=i+1;j<size;j++)
        {
            if(a[j]<a[i])
            {
                temp=a[i];
                a[i]=a[j];
                a[j]=temp;
            }
        }
    }

    for(i=1;i<size;i++)
    {
        if(a[i]==a[i-1]+1)
        {
            count++;
            if(count>max)
            {
                max=count;
                bestStart=i-count+1;  // update starting index
            }
        }
        else if(a[i]!=a[i-1])
        {
            count=1; // reset
        }
    }

    printf("\nLongest consecutive sequence length = %d",max);
    printf("\nLongest consecutive sequence: ");
    for(i=bestStart;i<bestStart+max;i++)
        printf("%d ",a[i]);

    return 0;
}
```
##61.Write a C program that finds the equilibrium index of an array.
```c
#include<stdio.h>
int main()
{
    int a[100],i,size,total=0,right_sum=0,left_sum=0;
    printf("Enter size:");
    scanf("%d",&size);
    printf("Enter elements:");
    for(i=0;i<size;i++)
    {
        scanf("%d",&a[i]);
    }
    for(i=0;i<size;i++)
    {
        total=total+a[i];
    }
    for(i=0;i<size;i++)
    {
        right_sum=total-left_sum-a[i];
        if(right_sum==left_ sum)
        {
            printf("Equilibrium index:%d\n",i);
            break;
        }
        left_sum=left_sum+a[i];
    }
 return 0;   
}
```
##62.Write a C program to read an array of integers and store all positive elements along with their original indices in a 2D array.
```c
#include<stdio.h>
int main()
{
    int a[100],i,size,rows=0,cols=2,j,k;
    printf("Enter size:");
    scanf("%d",&size);
    printf("Enter elements:");
    for(i=0;i<size;i++)
    {
        scanf("%d",&a[i]);
    }
    for(i=0;i<size;i++)
    {
        if(a[i]>0)
        {
            rows++;
        }
    }
    int b[rows][cols],r=0;
    for(i=0;i<size;i++)
    {
        if(a[i]>0)
        {
            b[r][0]=i;
            b[r][1]=a[i];
            r++;
        }
    }
    for(i=0;i<rows;i++)
    {
        printf("%d\t%d\n",b[i][0],b[i][1]);
    }
    
    
    
   return 0; 
}
```

