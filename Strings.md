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
#include<stdio.h>
#include<string.h>
int main()
{
    char str[100],temp;
    int i,j,n;
    printf("Enter string:");
    fgets(str,sizeof(str),stdin);
    str[strcspn(str,"\n")]='\0';
    n=strlen(str);
    for(i=0;i<n-1;i++)
    {
        for(j=i+1;j<n;j++)
        {
            if(str[j]>str[i])
            {
                temp=str[i];
                str[i]=str[j];
                str[j]=temp;
            }
        }
    }
    printf("\nSorted string:%s",str);
    return 0;
    
}
```
##13.Write a program in C to extract a substring from a given string. 
```c
#include<stdio.h>
#include<string.h>
int main()
{
    char str[00],substr[100];
    int i,length,start;
    printf("Enter string:");
    fgets(str,sizeof(str),stdin);
    str[strcspn(str,"\n")]='\0';
    printf("Enter start positio (0-Based index): ");
    scanf("%d",&start);
    printf("Enter the length of substring:");
    scanf("%d",&length);
    for(i=0;(i<length)&&(str[start+i]!='\0');i++)
    {
        substr[i]=str[start+i];
    }
    substr[i]='\0';
    printf("\nExtracted substring:%s",substr);
    return 0;
}
```
##14.Write a C program to generate and print all possible substrings of a given string.
```c
#include<string.h>
int main()
{
    char str[100];
    int i,j,k,length;
    printf("Enter string:");
    fgets(str,sizeof(str),stdin);
    str[strcspn(str,"\n")]='\0';
    length=strlen(str);
    printf("\nAll possible substrings in a string:");
    for(i=0;i<length;i++)
    {
        for(j=i;j<length;j++)
        {
            for(k=i;k<=j;k++)
            {
                printf("%c",str[k]);
            }
            printf("\n");
        }
    }
    return 0;
}
```
##15.Write a C program to check whether a substring is present in a string. 
#include<stdio.h>
#include<string.h>
int main()
{
    char str[100],substr[100];
    int i,j,len1,len2,found;
    printf("Enter string:");
    fgets(str,sizeof(str),stdin);
    str[strcspn(str,"\n")]='\0';
    printf("Enter substring:");
    fgets(substr,sizeof(substr),stdin);
    substr[strcspn(substr,"\n")]='\0';
    len1=strlen(str);
    len2=strlen(substr);
    found=0;
    for(i=0;i<len1-len2;i++)
    {
        for(j=0;j<len2;j++)
        {
            if(str[i+j]!=substr[j])
            {
            break;
            }
        }
        if(j==len2)
        {
            found=1;
            break;
        }
    }
     if (found)
        printf("Substring found!\n");
    else
        printf("Substring not found!\n");
    
    return 0;
}
```
##16.Write a program in C to read a sentence and replace lowercase characters with uppercase and vice versa.
```c
#include<stdio.h>
#include<string.h>
#include<ctype.h>
int main()
{
    char str[100];
    int i;
    printf("Enter sentence:");
    fgets(str,sizeof(str),stdin);
    str[strcspn(str,"\n")]='\0';
    for(i=0;str[i]!='\0';i++)
    {
        if(isalpha(str[i]))
        {
            if(isupper(str[i]))
            {
                str[i]=tolower(str[i]);
            }
            else if(islower(str[i]))
            {
                str[i]=toupper(str[i]);
            }
        }
    }
    printf("\nConverted sentence:%s",str);
    
    return 0;
}
```
##17.Write a program in C to find the number of times a given word 'the' appears in the given string
```c



