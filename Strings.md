## 1.Write a C program to count the number of vowels, consonants, digits, and spaces in a string entered by the user.
Sample Input:
Enter a string: Hello World 123
Sample Output:
Vowels: 3
Consonants: 7
Digits: 3
Spaces: 2
```c
#include <stdio.h>
#include <string.h>
#include <ctype.h>

int main() {
    char str[1000];
    int i, v = 0, c = 0, d = 0, sp = 0;

    printf("Enter string: ");
    fgets(str, sizeof(str), stdin);
    str[strcspn(str, "\n")] = '\0';

    for (i = 0; str[i] != '\0'; i++) {
        if (isalpha(str[i])) {
            char ch = tolower(str[i]);
            if (ch == 'a' || ch == 'e' || ch == 'i' || ch == 'o' || ch == 'u') {
                v++;
            } else {
                c++;
            }
        } else if (isdigit(str[i])) {
            d++;
        } else if (isspace(str[i])) {
            sp++;
        }
    }

    printf("Vowels: %d\nConsonants: %d\nDigits: %d\nSpaces: %d\n", v, c, d, sp);
    return 0;
}

```
##2.Write a program in C to input a string and print it.
```c
#include<stdio.h>
#include<string.h>
int main()
{
    char str[100];
    printf("Enter string:");
    fgets(str,sizeof(str),stdin);
    str[strcspn(str,"\n")]='\0';
    printf("\nyou entered string:%s",str);
    return 0;
}
```
##3.Write a program in C to find the length of a string without using library functions.
```c
#include<stdio.h>
#include<string.h>
int main()
{
    char str[100];
    int i,len=0;
    printf("Enter string:");
    fgets(str,sizeof(str),stdin);
    str[strcspn(str,"\n")]='\0';
    for(i=0;str[i]!='\0';i++)
    {
         len++;
    }
    printf("Length of the string:%d",len);
    return 0;
}
```
##4.Write a program in C to separate individual characters from a string.
```c#include<stdio.h>
#include<string.h>
int main()
{
    char str[100];
    int i,len=0;
    printf("Enter string:");
    fgets(str,sizeof(str),stdin);
    str[strcspn(str,"\n")]='\0';
    printf("\nCharacters are:");
    for(i=0;str[i]!='\0';i++)
    {
        printf("\n%c",str[i]);
    }
    return 0;
}
```
##5.Write a program in C to print individual characters of a string in reverse order.
```c
#include<stdio.h>
#include<string.h>
int main()
{
    char str[100];
    int i;
    printf("Enter string:");
    fgets(str,sizeof(str),stdin);
    str[strcspn(str,"\n")]='\0';
    int len=strlen(str);
    printf("\nCharacters in reverse order:");
    for(i=len-1;i>=0;i--)
    {
        printf("\n%c",str[i]);
    }
    return 0;
}
```
##6.Write a program in C to count the total number of words in a string.
```c
#include<stdio.h>
#include<string.h>
int main()
{
    char str[100];
    int i,word=0;
    printf("Enter string:");
    fgets(str,sizeof(str),stdin);
    str[strcspn(str,"\n")]='\0';
    for(i=0;str[i]!='\0';i++)
    {
    if((str[i]!='\n'&&str[i]!='\0')&&(i==0||str[i-1]==' '))
    {
        word++;
    }
    }
    printf("Total number of words=%d",word);
    return 0;
}
```
##7.Write a program in C to compare two strings without using string library functions. 
```c
#include<stdio.h>
#include<string.h>
int main()
{
    char str1[100],str2[100];
    int i,len1,len2;
    printf("Enter  first string:");
    fgets(str1,sizeof(str1),stdin);
    str1[strcspn(str1,"\n")]='\0';
    printf("Enter  second string:");
    fgets(str2,sizeof(str2),stdin);
    str2[strcspn(str2,"\n")]='\0';
    len1=strlen(str1);
    len2=strlen(str2);
    if(len1!=len2)
    {
        printf("Strings are not equal.");
        return 0;
    }
    for(i=0;i<len1;i++)
    {
    if(str1[i]!=str2[i])
    {
        printf("Strings are not equal.");
        return 0;
    }
    }
    
    printf("\nStrings are equal.");
    return 0;
}
```
##8.Write a program in C to copy one string to another string.
```c
#include<stdio.h>
#include<string.h>
int main()
{
    char str1[100],str2[100];
    int i;
    printf("Enter string:");
    fgets(str1,sizeof(str1),stdin);
    str1[strcspn(str1,"\n")]='\0';
    
    for(i=0;str1[i]!='\0';i++)
    {
    str2[i]=str1[i];
    }
    str2[i]='\0';
    printf("\ncopied string:%s",str2);
    return 0;
}
```
##9.Write a program in C to count the total number of vowels or consonants in a string.
```c
#include<stdio.h>
#include<string.h>
#include<ctype.h>
int main()
{
    char str[100];
    int i,v=0,c=0;
    printf("Enter string:");
    fgets(str,sizeof(str),stdin);
    str[strcspn(str,"\n")]='\0';
    
    for(i=0;str[i]!='\0';i++)
      {
    if(isalpha(str[i]))
    {
        str[i]=tolower(str[i]);
    if(str[i]=='a'||str[i]=='e'||str[i]=='i'||str[i]=='o'||str[i]=='u')
        {
            v++;
        }
        else
        {
            c++;
        }
    }
        }
    printf("Number of vowels=%d\nNumber of consonants=%d",v,c);
    return 0;
}
```
##10.Write a program in C to find the maximum number of characters in a string. 
```c
#include<stdio.h>
#include<string.h>
int main()
{
    char str[100];
    int i,max=0;
    printf("Enter string:");
    fgets(str,sizeof(str),stdin);
    str[strcspn(str,"\n")]='\0';
    
    for(i=0;str[i]!='\0';i++)
      {
    if(str[i]!='\n'&&str[i]!='\0')
    {
       max++;
        
    }
      }
    printf("maximum number of characters in the string:%d",max);
    return 0;
}
```
##11.Write a C program to sort a string array in ascending order.
```c
#include<stdio.h>
#include<stdio.h>
#include<string.h>
int main()
{
    char str[100][100],temp[100];
    int i,n,j;
    printf("Enter number of strings:");
    scanf("%d",&n);
    getchar();
    printf("Enter strings:\n");
    for(i=0;i<n;i++)
    {
        fgets(str[i],sizeof(str[i]),stdin);
        str[i][strcspn(str[i],"\n")]='\0';
    }
    for(i=0;i<n-1;i++)
    {
        for(j=i+1;j<n;j++)
        {
            if(strcmp(str[i],str[j])>0)
            {
                strcpy(temp,str[i]);
                strcpy(str[i],str[j]);
                strcpy(str[j],temp);
            }
        }
    }
    printf("\nStrings in ascending order:\n");
    for (i = 0; i < n; i++) {
        printf("%s\n", str[i]);
    }
    return 0;
}
```
##12.Write a program in C to read a string from the keyboard and sort it using bubble sort.
```c

