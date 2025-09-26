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

```c
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
#include<stdio.h>
#include<string.h>
#include<ctype.h>
int main()
{
    char str[100];
    int i,count=0;
    printf("Enter string:");
    fgets(str,sizeof(str),stdin);
    str[strcspn(str,"\n")]='\0';
    for(i=0;str[i]!='\0';i++)
    {
        str[i]=tolower(str[i]);
    }
    char *token=strtok(str," ,.!?;");
    while(token!=NULL)
    {
        if(strcmp(token,"the")==0)
        {
            count++;
        }
        token=strtok(NULL," ,.!?;");
    }
    printf("The word 'the' appears %d times in the string.\n", count);

    return 0;
}
```
##18.Write a program in C to remove characters from a string except alphabets. 
```c
#include<stdio.h>
#include<string.h>
#include<ctype.h>
int main()
{
    char str[100],str2[100];
    int i,j=0;
    printf("Enter string:");
    fgets(str,sizeof(str),stdin);
    str[strcspn(str,"\n")]='\0';
    for(i=0;str[i]!='\0';i++)
    {
       if(isalpha(str[i]))
       {
           str2[j++]=str[i];
       }
    }
    str2[j]='\0';
    printf("output string:%s\n",str2);
    

    return 0;
}
```
##19.Write a program in C to find the frequency of characters.
```c
#include<stdio.h>
#include<string.h>
#include<ctype.h>
int main()
{
    char str[100];
    int i,freq[256]={0};
    printf("Enter string:");
    fgets(str,sizeof(str),stdin);
    str[strcspn(str,"\n")]='\0';
    for(i=0;str[i]!='\0';i++)
    {
      freq[(int)str[i]]++;
    }
    for(i=0;str[i]!='\0';i++)
    {
       printf("%c->%d\n",str[i],freq[(int)str[i]]);
       freq[(int)str[i]]=0;
    }
    return 0;
}
```
##20.Write a program in C to combine two strings manually. 
```c
#include<stdio.h>
#include<string.h>
int main()
{
    char str[100],str1[100];
    int i;
    printf("Enter  frist string:");
    fgets(str,sizeof(str),stdin);
    str[strcspn(str,"\n")]='\0';
    int len=strlen(str);
    printf("Enter second string:");
    fgets(str1,sizeof(str1),stdin);
    str1[strcspn(str1,"\n")]='\0';
    int len1=strlen(str1);
    for(i=0;str[i]!='\0';i++)
    {
      str[len+i]=str1[i];
    }
    str[len+i]='\0';
    printf("\nCombined string:%s",str);
    
    return 0;
}
```
##21.Write a program in C to find the largest and smallest words in a string.
```c
#include<stdio.h>
#include<string.h>
#include<ctype.h>
#include<limits.h>
int main()
{
    char str[100],small[100],big[100];
    int i,len,min=INT_MAX,max=INT_MIN;
    printf("Enter string:");
    fgets(str,sizeof(str),stdin);
    str[strcspn(str,"\n")]='\0';
    for(i=0;str[i]!='\0';i++)
    {
        str[i]=tolower(str[i]);
    }
    char *token=strtok(str," ,.!?");
    while(token!=NULL)
    {
        len=strlen(token);
        if(len>max)
        {
            max=len;
            strcpy(big,token);
        }
        else if(len<min)
        {
            min=len;
            strcpy(small,token);
        }
       token=strtok(NULL," ,.!?");
    }
    printf("smallest word=%s\nlargest word=%s",small,big);
    return 0;
}
```
##22.Write a program in C to convert a string to uppercase.
```c
#include<stdio.h>
#include<string.h>
#include<ctype.h>
int main()
{
    char str[100];
    int i;
    printf("Enter string:");
    fgets(str,sizeof(str),stdin);
    str[strcspn(str,"\n")]='\0';
    for(i=0;str[i]!='\0';i++)
    {
        str[i]=toupper(str[i]);
    }
    printf("\nUppercase string:%s",str);
    
    return 0;
}
```
##23.Write a program in C to convert a string to lowercase.
```c
#include<stdio.h>
#include<string.h>
#include<ctype.h>
int main()
{
    char str[100];
    int i;
    printf("Enter string:");
    fgets(str,sizeof(str),stdin);
    str[strcspn(str,"\n")]='\0';
    for(i=0;str[i]!='\0';i++)
    {
        str[i]=tolower(str[i]);
    }
    printf("\nlowercase string:%s",str);
    
    return 0;
}
```
##24.Write a program in C to check whether a character is a Hexadecimal Digit or not.
```c
#include<stdio.h>
int main()
{
    char a;
    printf("Enter character:");
    scanf("%c",&a);
    
    if((a>='0')&&(a<=9)||(a>='a')&&(a<='f')||(a>='A')&&(a<='F'))
        {
            printf("%c is a hexadecimal character.",a);
        }
        else
        {
        printf("%c is  not a hexadecimal character.",a); 
        }
    
    return 0;
}
```
## 25.Write a program in C to check whether a letter is uppercase or not.
```c
#include<stdio.h>
#include<string.h>
#include<ctype.h>
int main()
{
    char str[100];
    int i,count=0;
    printf("Enter string:");
    fgets(str,sizeof(str),stdin);
    str[strcspn(str,"\n")]='\0';
    for(i=0;str[i]!='\0';i++)
    {
        if(ispunct(str[i]))
        {
            count++;
        }
    }
    printf("\nNumber of  punctuation characters:%d",count);
    return 0;
}
```
##26.Write a program in C to print only the string before the new line character.
```c
#include <stdio.h>
int main() {
    char str[100];
    int i;
    printf("Enter string: ");
    fgets(str, sizeof(str), stdin);
    for (i = 0; str[i] != '\n' && str[i] != '\0'; i++) {
        putchar(str[i]);
    }
    return 0;
}
```
##27.Write a C program to read a string and print the frequency of each character (ignore case, ignore spaces).
```c
#include<stdio.h>
#include<string.h>
#include<ctype.h>
int main()
{
    char str[100];
    int i,freq[256]={0};
    printf("Enter string:");
    fgets(str,sizeof(str),stdin);
    str[strcspn(str,"\n")]='\0';
    for(i=0;str[i]!='\0';i++)
    {
        str[i]=tolower(str[i]);
        freq[(int)str[i]]++;
    }
    printf("Output:");
    for(i=0;str[i]!='\0';i++)
    {
        if(str[i]!=' ' && freq[(int)str[i]]>0)
        printf("%c->%d\n",str[i],freq[(int)str[i]]);
        freq[(int)str[i]]=0;
    }
    
    return 0;
}
```
##28.Write a program in C to check whether a letter is lowercase or not.
```c
#include<stdio.h>
int main()
{
    char a;
    printf("Enter character:");
    scanf("%c",&a);
    if((a>='a')&&(a<='z'))
    {
        printf("The character %c is lowercase.",a);
    }
    else
    {
         printf("The character %c is not lowercase.",a);
    }
    return 0;
}
```
##29.Write a program in C to check whether a character is a digit or not.
```c
#include<stdio.h>
int main()
{
    char a;
    printf("Enter character:");
    scanf("%c",&a);
    if((a>='0')&&(a<='9'))
    {
        printf("The character %c is Digit.",a);
    }
    else
    {
         printf("The character %c is not digit.",a);
    }
    return 0;
}
```
##30.Write a program in C to split strings by space into words. 
```c
#include<stdio.h>
#include<string.h>
int main()
{
    char str[1000];
    int i=1;
    printf("Enter string:");
    fgets(str,sizeof(str),stdin);
    str[strcspn(str,"\n")]='\0';
    char*token=strtok(str," ,.!?");
    while(token!=NULL)
    {
        printf("word%d=%s\n",i,token);
        i++;
        token=strtok(NULL," ,.!?");
    }
    
    return 0;
}
```
##31.Write a C program to find the repeated character in a string.
```c
#include<string.h>
int main()
{
    char str[1000];
    int i,freq[256]={0};
    printf("Enter string:");
    fgets(str,sizeof(str),stdin);
    str[strcspn(str,"\n")]='\0';
    printf("\nRepeated characters are: ");
    for(i=0;str[i]!='\0';i++)
    {
        freq[(int)str[i]]++;
    }
    for(i=0;str[i]!='\0';i++)
    {
        if(str[i]!=' '&&freq[(int)str[i]]>1)
        {
           printf("%c ",str[i]); 
        }
        freq[(int)str[i]]=0;
    }
    
    return 0;
}
```
##32.Write a C program to convert vowels into uppercase characters in a string.
```c
#include<stdio.h>
#include<string.h>
#include<ctype.h>
int main()
{
    char str[1000];
    int i;
    printf("Enter string:");
    fgets(str,sizeof(str),stdin);
    str[strcspn(str,"\n")]='\0';
    for(i=0;str[i]!='\0';i++)
    {
        if(str[i]=='a'||str[i]=='e'||str[i]=='i'||str[i]=='o'||str[i]=='u')
        {
            str[i]=toupper(str[i]);
        }
    }
    printf("\nConverted string:%s",str);
    return 0;
}
```
##33.Write a C program to multiply two positive numbers as strings. Return a string 
representation of the product.
```c
#include<stdio.h>
#include<string.h>
#include<ctype.h>
int main()
{
    char str[1000],str1[1000];
    int i;
    long long sum=0,sum1=0;
    printf("Enter first number:");
    fgets(str,sizeof(str),stdin);
    str[strcspn(str,"\n")]='\0';
    printf("Enter second number:");
    fgets(str1,sizeof(str1),stdin);
    str1[strcspn(str1,"\n")]='\0';
    for(i=0;str[i]!='\0';i++)
    {
        if(isdigit(str[i]))
        {
            str[i]=str[i]-'0';
            sum=sum*10+str[i];
        }
    }
    for(i=0;str1[i]!='\0';i++)
    {
        if(isdigit(str1[i]))
        {
            str1[i]=str1[i]-'0';
            sum1=sum1*10+str1[i];
        }
    }
    printf("product=%lld",sum*sum1);
    return 0;
}
```
##34.Write a C program to check whether a string is palindrome or not.
```c
#include<stdio.h>
#include<string.h>
int main()
{
    char str[1000];
    int start=0,end;
    printf("Enter string:");
    fgets(str,sizeof(str),stdin);
    str[strcspn(str,"\n")]='\0';
    end=strlen(str)-1;
    while(start<end)
    {
        if(str[start]!=str[end])
        {
            printf("The string is not palindrome.\n");
            return 0;
        }
        start++;
        end--;
    }
    printf("The string is a palindrome.\n");
    return 0;
}
```
##35.Write a C program to check whether a given string is a palindrome or not, ignoring spaces, punctuation, and case.
```c
#include<stdio.h>
#include<string.h>
#include<ctype.h>
int main()
{
    char str[1000];
    int start=0,end;
    printf("Enter string:");
    fgets(str,sizeof(str),stdin);
    str[strcspn(str,"\n")]='\0';
    end=strlen(str)-1;
    while(start<end)
    {
        while((start<end)&&(!isalpha(str[start])))
        {
           start++; 
        }
        while((start<end)&&(!isalpha(str[end])))
        {
            end--;
        }
        if(tolower(str[start])!=tolower(str[end]))
        {
            printf("The string is not palindrome.");
            return 0;
        }
        start++;
        end--;
    }
    printf("The string is a palindrome.\n");
    return 0;
}
```
##36.Write a C program to reverse order of words in a given string.
```c
#include<stdio.h>
#include<string.h>
#include<ctype.h>
int main()
{
    char str[1000],str1[1000][100];
    int c=0,i;
    printf("Enter string:");
    fgets(str,sizeof(str),stdin);
    str[strcspn(str,"\n")]='\0';
    char*token=strtok(str," ,.!?");
    while(token!=NULL)
    {
       strcpy(str1[c++],token);
       token=strtok(NULL," ,.!?");
    }
    for(i=c-1;i>=0;i--)
    {
        printf("%s ",str1[i]);
    }
    
    return 0;
}
```
##37.Write a C program to find the first occurrence of a character in a given string.
```c
#include<stdio.h>
#include<string.h>
int main()
{
    char str[100],ch;
    int i;
    printf("Enter string:");
    fgets(str,sizeof(str),stdin);
    str[strcspn(str,"\n")]='\0';
    printf("Enter character to find:");
    scanf("%c",&ch);
    for(i=0;str[i]!='\0';i++)
    {
        if(str[i]==ch)
        {
     printf("First occurrence of %c is at position %d",str[i],i+1);
     return 0;
        }
    }
    printf("Character %c not found in the string",ch);
    return 0;
}
```
##38.Write a C program to find the last occurrence of a character in a given string. 
```c
#include<stdio.h>
#include<string.h>
int main()
{
    char str[100],ch;
    int i,lastpos=-1;
    printf("Enter string:");
    fgets(str,sizeof(str),stdin);
    str[strcspn(str,"\n")]='\0';
    printf("Enter character to find:");
    scanf("%c",&ch);
    for(i=0;str[i]!='\0';i++)
    {
        if(str[i]==ch)
        {
     lastpos=i;
        }
        
    }
    if(lastpos!=-1)
        {
            printf("Last occurrence of %c is at position %d",ch,lastpos+1);
        }
    else
    {
    printf("The character %c not found in the string.",ch);
    }
    return 0;
}
```
##39.Write a C program to search all occurrences of a character in a given string.
```c
#include<stdio.h>
#include<string.h>
int main()
{
    char str[100],ch;
    int i,found=0;
    printf("Enter string:");
    fgets(str,sizeof(str),stdin);
    str[strcspn(str,"\n")]='\0';
    printf("Enter character to find:");
    scanf("%c",&ch);
    printf("position of character %c in the string:",ch);
    for(i=0;str[i]!='\0';i++)
    {
        if(str[i]==ch)
        {
       printf("%d ",i+1);
       found=1;
        }
    }
    if(!found)
    printf("\nCharacter %c not found in the string.",ch);
    return 0;
}
```
##40.Write a C program to find the highest frequency character in a string.
```c
#include<stdio.h>
#include<string.h>
int main()
{
    char str[100];
    int i,freq[256]={0};
    printf("Enter string:");
    fgets(str,sizeof(str),stdin);
    str[strcspn(str,"\n")]='\0';
    for(i=0;str[i]!='\0';i++)
    {
        freq[(int)str[i]]++;
    }
    int max=freq[(int)str[0]];
    for(i=0;str[i]!='\0';i++)
    {
        if(freq[(int)str[i]]>max)
        {
            max=freq[(int)str[i]];
        }
    }
    for(i=0;str[i]!='\0';i++)
    {
        if(freq[(int)str[i]]==max)
        {
     printf("Highest frequency character: %c\n", str[i]);
            break; 
        }
    }
    return 0;
}
```
##41.Write a C program to find the lowest frequency character in a string.
```c
#include<string.h>
int main()
{
    char str[100];
    int i,freq[256]={0};
    printf("Enter string:");
    fgets(str,sizeof(str),stdin);
    str[strcspn(str,"\n")]='\0';
    for(i=0;str[i]!='\0';i++)
    {
        freq[(int)str[i]]++;
    }
    int min=strlen(str);
    for(i=0;str[i]!='\0';i++)
    {
        if(freq[(int)str[i]]<min&&freq[(int)str[i]]>0)
        {
            min=freq[(int)str[i]];
        }
    }
    for(i=0;str[i]!='\0';i++)
    {
        if(freq[(int)str[i]]==min)
        {
     printf("lowest frequency character: %c\n", str[i]);
            break; 
        }
    }
    return 0;
}
```
##42.Write a C program to remove all repeated characters from a given string.
```c
#include<stdio.h>
#include<string.h>
int main()
{
    char str[100];
    int i,freq[256]={0};
    printf("Enter string:");
    fgets(str,sizeof(str),stdin);
    str[strcspn(str,"\n")]='\0';
    for(i=0;str[i]!='\0';i++)
    {
        freq[(int)str[i]]++;
    }
    printf("\nString after removing duplicates: ");
    for(i=0;str[i]!='\0';i++)
    {
        if(freq[(int)str[i]]>0)
        {
            printf("%c",str[i]);
        }
        freq[(int)str[i]]=0;
    }
    
    return 0;
}
```
##43.Write a program to find the number of occurrences of a particular word in a string.
```c
#include<stdio.h>
#include<string.h>
#include<ctype.h>
int main()
{
    char str[100],word[100];
    int i,count=0;
    printf("Enter string:");
    fgets(str,sizeof(str),stdin);
    str[strcspn(str,"\n")]='\0';
    printf("Enter word to search:");
    fgets(word,sizeof(word),stdin);
    word[strcspn(word,"\n")]='\0';
    char*token=strtok(str," ,.!?");
    while(token!=NULL)
    {
        if(strcmp(token,word)==0)
        {
           count++; 
        }
        token=strtok(NULL," ,.!?");
    }
    printf("The word %s occurs %d times.",word,count);
    return 0;
}
```
##44.Write a C program to remove all vowels from a given string (using pointer notation).
```c
#include<stdio.h>
 #include<string.h>
 #include<ctype.h>
 int main()
 {
char str[100],*p;
 printf("Enter string:");
 fgets(str,sizeof(str),stdin);
 str[strcspn(str,"\n")]='\0';
 printf("\nstring without vowels:");
 for(p=str;*p!='\0';p++)
{
*p=tolower(*p);
 if((*p!='a')&&(*p!='e')&&(*p!='i')&&(*p!='o')&&(*p!='u')&&(*p!='A')&&(*p!='E')&&(*p!='I')&&(*p!='O')&&(*p!='U'))
 {
printf("%c",*p) ;
 }
}
return 0;
}
```
##45.Read a line (may include spaces). Print the first character that does not repeat. If none, print No unique character.
```c
#include<stdio.h>
 #include<string.h>
 #include<ctype.h>
int main()
 {
char str[1000];
 int i,j,flag;
 printf("Enter string:");
 fgets(str,sizeof(str),stdin);
str[strcspn(str,"\n")]='\0';
 for(i=0;str[i]!='\0';i++)
 {
str[i]=tolower(str[i]);
 }
for(i=0;str[i]!='\0';i++)
 {
flag=0;
 for(j=i+1;str[j]!='\0';j++)
 {
if(str[i]==str[j])
 {
flag=1;
 break;
 }
 }
 if(flag==0)
{
printf("\nThe first non repeating:%c",str[i]);
return 0;
 }
}
 printf("\nNot found such character.");
 return 0;
 }
```
##46.Read a line of text and print the number of words and number of characters (excluding spaces).
```c
#include<stdio.h>
 #include<string.h>
#include<ctype.h>
 int main()
 {
char str[100];
 int i,count=0,character=0;
printf("Enter string:");
 fgets(str,sizeof(str),stdin);
 str[strcspn(str,"\n")]='\0';
for(i=0;str[i]!=0;i++)
 {
if((str[i]!=' '&&str[i]!='\0')&&(i==0||str[i-1]==' '))
 {
count++;
 }
}
 for(i=0;str[i]!='\0';i++)
{
if(!isspace(str[i]))
{
character++;
 }
 }
printf("Number of words=%d\nNumber of characters=%d",count,character);
 return 0;
 }
```
##47.Read two strings and check if they are anagrams (i.e., contain the same characters in any order). Ignore case.
```c
 #include<stdio.h>
 #include<string.h>
 #include<ctype.h>
 int main()
 {
char str[1000],ch1,ch2,str1[1000];
 int freq1[26]={0},freq2[26]={0},i;
 printf("Enter first string:");
fgets(str,sizeof(str),stdin);
 str[strcspn(str,"\n")]='\0';
printf("\nEnter second string:");
fgets(str1,sizeof(str1),stdin);
str1[strcspn(str1,"\n")]='\0';
 for(i=0;str[i]!='\0';i++)
 {
 ch1=tolower(str[i]); freq1[ch1-'a']++;
 }
for(i=0;str1[i]!='\0';i++)
{
ch2=tolower(str1[i]);
freq2[ch2-'a']++;
 }
 for(i=0;i<26;i++)
 {
if(freq1[i]!=freq2[i])
 {
 printf("\nStrings are not Aanagrams");
 return 0;
 }
 }
 printf("\n String are anagrams");
 return 0;
 }
```
##48.Write a C program to reverse each word in a given string without changing the order of words.
```c
#include<stdio.h>
#include<string.h>
int main()
{
    char str[100],str1[100];
    int start,end,k=0,i;
    printf("Enter string:");
    fgets(str,sizeof(str),stdin);
    str[strcspn(str,"\n")]='\0';
    for(i=0;str[i]!='\0';i++)
    {
        if(str[i]!=' ')
        {
           str1[k++]=str[i]; 
        }
        else
        {
            str1[k]='\0';
            end=strlen(str1);
            start=0;
            while(start<end-1)
            {
                char temp=str1[start];
                str1[start]=str1[end-1];
                str1[end-1]=temp;
                start++;
                end--;
            }
            printf("%s ",str1);
            k=0;
        }
    }
    str1[k]='\0';
    end=strlen(str1);
    start=0;
    while(start<end-1)
            {
                char temp=str1[start];
                str1[start]=str1[end-1];
                str1[end-1]=temp;
                start++;
                end--;
            }
    
    printf("%s",str1);
    return 0;
}
```
##49.Write a program to input two strings and remove from the first string all characters that appear in the second string.
```c
#include<stdio.h>
#include<string.h>
int main()
{
    char str[100],str1[100];
    int i,freq1[256]={0};
    printf("Enter first string:");
    fgets(str,sizeof(str),stdin);
    str[strcspn(str,"\n")]='\0';
    printf("Enter second string:");
    fgets(str1,sizeof(str1),stdin);
    str1[strcspn(str1,"\n")]='\0';
    for(i=0;str1[i]!='\0';i++)
    {
        freq1[(unsigned char)str1[i]]=1;
    }
    for(i=0;str[i]!='\0';i++)
    {
        if(!freq1[(unsigned char)str[i]])
        {
            printf("%c",str[i]);
        }
    }
    
    
}
```
##50.Write a program to input a string and replace all vowels (a, e, i, o, u) with *.
```c
#include<stdio.h>
#include<string.h>
#include<ctype.h>
int main()
{
    char str[100];
    int i;
    printf("Enter string:");
    fgets(str,sizeof(str),stdin);
    str[strcspn(str,"\n")]='\0';
    for(i=0;str[i]!='\0';i++)
    {
        if(isalpha(str[i]))
        {
            str[i]=tolower(str[i]);
        }
        if(str[i]=='a'||str[i]=='e'||str[i]=='i'||str[i]=='u'||str[i]=='o')
        {
               str[i]='*';    
        }
    }
    printf("%s",str);
    return 0;
}
```
##51.Write a program to read a string (with multiple words) and print the length of the longest word.
```c
#include<stdio.h>
#include<string.h>
#include<limits.h>
int main()
{
    char str[100],str1[100][100],str2[100];
    int i,k=0,j=0,large=INT_MIN;
    printf("Enter the string:");
    fgets(str,sizeof(str),stdin);
    str[strcspn(str,"\n")]='\0';
    for(i=0;str[i]!='\0';i++)
    {
        if(str[i]!=' ')
        {
            str1[k][j++]=str[i];
        }
        else
        {
            str1[k][j]='\0';
            if(j>large)
            {
                large=j;
                strcpy(str2,str1[k]);
            }
            k++;
            j=0;
        }
    }
    str1[k][j]='\0';
            if(j>large)
            {
                large=j;
                strcpy(str2,str1[k]);
                
            }
           
            printf(" Length of the longest word=%d (%s)",large,str2);
            return 0;
}
```
##52.Write a program to input a string and reverse only the vowels in it.
```c
#include<stdio.h>
#include<string.h>
#include<ctype.h>
int main()
{
    char str[100];
    int i,start=0,end;
    printf("Enter string:");
    fgets(str,sizeof(str),stdin);
    str[strcspn(str,"\n")]='\0';
    end=strlen(str)-1;
    for(i=0;str[i]!='\0';i++)
    {
        str[i]=tolower(str[i]);
    }
    while(start<end)
    {
        if(str[start]!='a'&&str[start]!='e'&&str[start]!='i'&&str[start]!='o'&&str[start]!='u')
        {
            start++;
        }
        else if(str[end]!='a'&&str[end]!='e'&&str[end]!='i'&&str[end]!='o'&&str[end]!='u')
        {
            end--;
        }
        else
        {
            char temp=str[start];
            str[start]=str[end];
            str[end]=temp;
             start++;
             end--;
        }
    }
    printf("\nreverse only vowels in a given string:%s",str);
    return 0;
}
```
##53.Write a C program to implement basic string compression.
.The program should take a string as input.
.Consecutive repeating characters should be replaced by the character followed by the count of its repetition.
.If a character occurs only once, it should remain as it is without a number.
```c
#include<stdio.h>
#include<string.h>
int main()
{
    char str[1000];
    printf("Enter string:");
    fgets(str,sizeof(str),stdin);
    str[strcspn(str,"\n")]='\0';
    int i,count=1;
    for(i=0;str[i]!='\0';i++)
    {
        if(str[i]==str[i+1])
        {
            count++;
        }
        else
        {
            if(count>1)
                printf("%c%d",str[i],count);
            else
                printf("%c",str[i]);
                count=1;
        }
    }
    return 0;
    
}
```
##54.Find the longest substring without repeating characters in a given string.
```c
#include<stdio.h>
#include<string.h>
int main()
{
    char str[100];
    printf("Enter string:");
    fgets(str,sizeof(str),stdin);
    str[strcspn(str,"\n")]='\0';
    int i,j,len,maxlen=0,startindex=0;
    for(i=0;str[i]!='\0';i++)
    {
        len=0;
        int freq[256]={0};
        for(j=i;str[j]!='\0';j++)
        {
           if(freq[(unsigned)str[j]]==0)
           {
               freq[(unsigned char)str[j]]++;
               len++;
           }
           else
           {
               break;
           }
           if(len>maxlen)
           {
               maxlen=len;
               startindex=i;
           }
            
        }
    }
     printf("Length of the largest substring without reapeting characters:%d\n",maxlen);
     printf("Larest substrig without repeating characters:");
    for(i=startindex;i<startindex+maxlen;i++)
    {
        printf("%c",str[i]);
    }
    return 0;
    
}
```
##55.Write a program to check if the given string’s characters can be rearranged to form a palindrome.
```c
#include<stdio.h>
#include<string.h>
#include<ctype.h>
int main()
{
    char str[1000];
    printf("Enter string:");
    fgets(str,sizeof(str),stdin);
    str[strcspn(str,"\n")]='\0';
    int i,freq[256]={0},odd=0;
    for(i=0;str[i]!='\0';i++)
    {
        if(isalpha(str[i]))
        {
            freq[tolower(str[i])]++;
        }
    }
    for(i=0;i<256;i++)
    {
        if(freq[i]%2!=0)
        {
            odd++;
        }
    }
    if(odd<=1)
    {
        printf("Yes, it can be rearranged into a palindrome.\n");
    }
    else
    {
        printf("No, it cannot be rearranged into a palindrome.\n");
    }
    return 0;
    
    
}
```
##56.A string is a Pangram if it contains every letter of the English alphabet at least once.
```c
#include<stdio.h>
#include<string.h>
#include<ctype.h>
int main()
{
    char str[100],str2[100];
    printf("Enter string:");
    fgets(str,sizeof(str),stdin);
    str[strcspn(str,"\n")]='\0';
    strcpy(str2,str);
    int i,freq[26]={0};
    for(i=0;str[i]!='\0';i++)
    {
        if(isalpha(str[i]))
        {
            str[i]=tolower(str[i]);
            freq[str[i]-'a']++;
        }
    }
    for(i=0;i<26;i++)
    {
        if(freq[i]==0)
        {
            printf("The string  \"%s\"  is not a panagram.\n",str2);
            return 0;
        }
    }
    printf("The string  \"%s\"   is a panagram.\n",str2);
    return 0;
}
```
##57.Write a C program to expand a compressed string where each letter is followed by a number that represents how many times the letter should be repeated.
```
#include<stdio.h>
#include<string.h>
#include<ctype.h>
int main()
{
    char str[100],ch;
    printf("Enter string:");
    fgets(str,sizeof(str),stdin);
    str[strcspn(str,"\n")]='\0';
    int i=0,count,j;
    while(str[i]!='\0')
    {
        if(isalpha(str[i]))
        {
            ch=str[i];
            i++;
            if(!isdigit(str[i]))
            {
                printf("%c",ch);
            }
        }
      else if(isdigit(str[i]))
      {
          int count=0;
          while(isdigit(str[i]))
          {
              count=count*10+(str[i]-'0');
              i++;
          }
          for(j=0;j<count;j++)
          {
              printf("%c",ch);
          }
       }
    }
    return 0;
}
```
##58.Check if a given string is a pangrammatic lipogram (all letters except one are present).
```c
#include<stdio.h>
#include<string.h>
#include<ctype.h>
int main()
{
    char str[100];
    printf("Enter string:");
    fgets(str,sizeof(str),stdin);
    str[strcspn(str,"\n")]='\0';
    int i,freq[26]={0},count=0,j;
    for(i=0;str[i]!='\0';i++)
    {
        if(isalpha(str[i]))
        {
        str[i]=tolower(str[i]);
        freq[str[i]-'a']++;
        }
    }
    for(i=0;i<26;i++)
    {
        if(freq[i]!=0)
        {
            count++;
        }
        else
        {
          j=i;  
        }
    }
    if(count==26)
    {
        printf("Pangram!\n");
    }
    else if(count==25)
    {
    printf("Pangrammatic Lipogram! Missing letter: %c\n", j + 'a');
    }
    else
    {
        printf("Not Pangrammatic Lipogram!\n");
    }
    return 0;
}
```
##59.Take a string containing letters and digits. Rearrange it so that alphabets and digits appear alternately.If impossible, print “Rearrangement impossible”.
```c
#include<stdio.h>
#include<string.h>
#include<math.h>
#include<ctype.h>
#include<stdlib.h>
int main()
{
    char str[100],alp[100],dig[100],result[100];
    printf("Enter string:");
    fgets(str,sizeof(str),stdin);
    str[strcspn(str,"\n")]='\0';
    int i,a=0,d=0,k=0,j=0;
    for(i=0;str[i]!='\0';i++)
    {
        if(isalpha(str[i]))
        {
            alp[k++]=str[i];
            a++;
        }
        else if(isdigit(str[i]))
        {
            dig[j++]=str[i];
            d++;
        }
    }
    if(abs(a-d)>1)
    {
        printf("Rearrange is impossibile.\n");
        return 0;
    }
    int ai=0,di=0,ri=0;
    int startalp=(a>=d)?1:0;
    while((ai<a)||(di<d))
    {
        if(startalp&&ai<a)
        {
            result[ri++]=alp[ai++];
        }
        else if(!startalp&&di<d)
        {
            result[ri++]=dig[di++];
        }
        startalp=!startalp;
    }
    result[ri]='\0';
    printf("Rearranged string %s\n",result);
    return 0;
    
}
```


