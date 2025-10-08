##1.Write a program in C to create and store information in a text file.
Test Data :
Input a sentence for the file : This is the content of the file test.txt.
Expected Output :
The file test.txt created successfully...!!
```c
#include<stdio.h>
#include<string.h>
#include<stdlib.h>
int main()
{
    FILE *fp=NULL;
    char str[1000];
    fp=fopen("test.txt","w");
    if(fp==NULL)
    {
        printf("File could not be created\n");
        exit(1);
    }
    printf("Enter string:");
    fgets(str,sizeof(str),stdin);
    str[strcspn(str,"\n")]='\0';
   fputs(str,fp);
    printf("The file test.txt created successfully...!!\n ");
    fclose(fp);
    
}
```
##2. Read Existing File
Write a program in C to read an existing file.
Test Data :
Input the file name to be opened : test.txt
Expected Output :
The content of the file test.txt is  :                                                                       
This is the content of the file test.txt.
```c
#include<stdio.h>
#include<string.h>
#include<stdlib.h>
int main()
{
    FILE *fp=NULL;
    char str[1000];
    fp=fopen("test.txt","r");
    if(fp==NULL)
    {
        printf("File could not be opened\n");
        exit(1);
    }
   
    printf("The content of the file test.txt is :\n");
    while(fgets(str,sizeof(str),fp)!=NULL)
    {
    printf("%s",str);
    }
    fclose(fp);
    
}
```
##3.Write a program in C to write multiple lines to a text file.
```c
#include<stdio.h>
#include<string.h>
#include<stdlib.h>
int main()
{
    FILE*fp=NULL;
    char str[1000];
    int i,n;
    fp=fopen("test.txt","w");
    if(fp==NULL)
    {
        printf("File could not be created\n");
        exit(1);
    }
    printf("Input the number of lines to be written:");
    scanf("%d",&n);
    getchar();
    printf("The lines are:\n");
    for(i=0;i<n;i++)
    {
        fgets(str,sizeof(str),stdin);
        fputs(str,fp);
    }
    fclose(fp);
    fp=fopen("test.txt","r");
    if(fp==NULL)
    {
        printf("File could not be opened.\n");
        exit(1);
    }
     printf("\nThe content of the file test.txt is:\n");
    while(fgets(str,sizeof(str),fp)!=NULL)
    {
        printf("%s",str);
    }
   
    
    fclose(fp);
    
}
```
##4.Write a C program to read a file and count:Total number of charactersTotal number of wordsTotal number of lines
```c
#include<stdio.h>
#include<string.h>
#include<ctype.h>
#include<stdlib.h>
int main()
{
    FILE*fp=NULL;
    char ch;
    int character=0,line=0,words=0;
    int inword=0;
    fp=fopen("sample.txt","r");
    if(fp==NULL)
    {
        printf("File could not be created.\n");
        exit(1);
    }
    while((ch=getc(fp))!=EOF)
    {
       character++;
       if(ch=='\n')
       {
           line++;
       }
       if(isspace(ch))
       {
           inword=0;
       }
       else if(inword==0)
       {
           inword=1;
           words++;
       }
       
    }
    if(character>0&&ch!='\n')
    {
        line++;
    }
    printf("Characters=%d\nwords=%d\nlines=%d",character,words,line);
    fclose(fp);
}
```
##5.Write a C program to copy the content of one file into another file.
```c
#include<stdio.h>
#include<stdlib.h>
int main()
{
    FILE*src=NULL,*dst=NULL;
    int ch;
    src=fopen("sujitha.txt","r");
    if(src==NULL)
    {
        printf(" Source File can not be opened.\n");
        exit(1);
    }
    dst=fopen("geetha.txt","w");
    if(dst==NULL)
    {
       printf("Destination File could not be created.\n"); 
       fclose(src);
       exit(1);
    }
   while ((ch = fgetc(src)) != EOF)
    {
        fputc(ch,dst);
    }
    printf("File copied successfully.\n");
    fclose(src);
    fclose(dst);
    return 0;
}
```
##6.Read a file words.txt.Count frequency of each word in the file.Print words and their count in descending order of frequency.
```c
#include<stdio.h>
#include<string.h>
#include<ctype.h>
#include<stdlib.h>
int main()
{
    FILE*fp=NULL;
    char str[1000],str1[100][100];
    int k=0,ch,j=0,i,l,count;
    fp=fopen("sample.txt","r");
    if(fp==NULL)
    {
        printf("File can not be opened.\n");
        exit(1);
    }
    while((ch=fgetc(fp))!=EOF&&k<sizeof(str)-1)
    {
        
        str[k++]=tolower((char)ch);
    }
    str[k]='\0';
    
    char *token=strtok(str," ,.!?\n\t");
    while(token!=NULL)
    {
        strcpy(str1[j],token);
        j++;
        token=strtok(NULL," ,.!?\n\t");
    }
    for(i=0;i<j;i++)
    {
        count=1;
        if(strcmp(str1[i],"0")==0)
        {
            continue;
        }
        for(l=i+1;l<j;l++)
        {
            if(strcmp(str1[i],str1[l])==0)
            {
                count++;
                strcpy(str1[l],"0");
            }
        }
        printf("%s->%d\n",str1[i],count);
    }
    fclose(fp);
    return 0;
}
```
##7.Read a file input.txt and print the word that occurs most frequently. Ignore case and punctuation.
```c
#include<stdio.h>
#include<string.h>
#include<ctype.h>
#include<stdlib.h>
int main()
{
    FILE*fp=NULL;
    char str[1000],str1[1000][1000];
    int k=0,i,j,count,max=0,index=-1,freq[100];
    fp=fopen("sample2.txt","r");
    if(fp==NULL)
    {
        printf("File could not be opend.\n");
        exit(1);
    }
    while(fgets(str,sizeof(str),fp)!=NULL)
    {
        for(i=0;str[i]!='\0';i++)
        {
            str[i]=tolower(str[i]);
        }
    }
    char *token=strtok(str," ,.!?\n\t");
    while(token!=NULL)
    {
      strcpy(str1[k],token);
      freq[k]=-1;
      k++;
      token=strtok(NULL," ,.!?\n\t");
    }
    for(i=0;i<k;i++)
    {
        count=1;
        for(j=i+1;j<k;j++)
        {
          if(strcmp(str1[i],str1[j])==0)
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
    for(i=0;i<k;i++)
    {
        if(freq[i]>max)
        {
        max=freq[i];
        index=i;
        }
    }
    if(index!=-1)
    {
    printf("Most Frequent Word=%s\n",str1[index]);
    printf("Frequency of word=%d\n",max);
    }
    else
    {
        printf("No words are found.\n");
    }
    fclose(fp);
    return 0;
}
```
##8.Count vowels, consonants, digits, and special characters from a file
```c
#include<stdio.h>
#include<string.h>
#include<stdlib.h>
#include<ctype.h>
int main()
{
    FILE*fp=NULL;
    char ch;
    int v=0,c=0,d=0,sp=0;
    fp=fopen("input.txt","r");
    if(fp==NULL)
    {
        printf("File could not be created.\n");
        exit(1);
    }
    while(!feof(fp))
    {
        ch=fgetc(fp);
        if(isalpha(ch))
        {
            ch=tolower(ch);
            if(ch=='a'||ch=='e'||ch=='i'||ch=='o'||ch=='u')
            {
                v++;
            }
            else
            {
                c++;
            }
        }
        else if(isdigit(ch))
        {
            d++;
        }
        else if(ch!='\n'&&!isspace(ch))
        {
            sp++;
        }
    }
    printf("Vowels=%d\nConsonants=%d\nDigits=%d\nSpecial character=%d",v,c,d,sp);
    fclose(fp);
    return 0;
}
```
##9.Write a C program that reads a file input.txt and replaces every vowel with * and every digit with #. Save the modified content into a new file output.txt.
```c
#include<stdio.h>
#include<stdlib.h>
#include<string.h>
#include<ctype.h>
int main()
{
    FILE*fp=NULL;
    char str[1000],ch;
    int k=0,i;
    fp=fopen("input1.txt","r");
    if(fp==NULL)
    {
        printf("File could not be opened.\n");
        exit(1);
    }
    while((ch=fgetc(fp))!=EOF)
    {
       str[k++]=ch;
    }
    str[k]='\0';
    for(i=0;str[i]!='\0';i++)
    {
        if(isalpha(str[i]))
        {
            str[i]=tolower(str[i]);
        }
        if(str[i]=='a'||str[i]=='e'||str[i]=='i'||str[i]=='o'||str[i]=='u')
        {
            str[i]='*';
        }
        else if(isdigit(str[i]))
        {
            str[i]='#';
        }
    }
    fclose(fp);
    fp=fopen("input2.txt","w");
    if(fp==NULL)
    {
        printf("File could not be created.\n");
        exit(1);
    }
    fputs(str,fp);
    fclose(fp);
    return 0;
}
```
##10.Write a C program to merge two files (file1.txt and file2.txt) into a new file (merged.txt) in alternate line order — i.e., first line from file1, then first line from file2, then second line from file1, etc.
If one file has more lines than the other, append the remaining lines at the end.
```c
#include<stdio.h>
#include<stdlib.h>
#include<string.h>
void write_with_newline(FILE *out, char *line) {
    fputs(line, out);
    int len = strlen(line);
    if (len == 0 || line[len - 1] != '\n') {
        fputc('\n', out); // Add newline if missing
    }
}
int main()
{
    FILE *fp1=NULL, *fp2=NULL, *fp3=NULL;
    char str1[1000],str2[1000];
    fp1=fopen("File1.txt","r");
    if(fp1==NULL)
    {
        printf("File can not be opened.\n");
        exit(1);
    }
    fp2=fopen("File2.txt","r");
    if(fp2==NULL)
    {
        printf("File can not be opened.\n");
        exit(1);
    }
    fp3=fopen("merge.txt","w");
    if(fp3==NULL)
    {
        printf("File could not be created.\n");
        
        exit(1);
    }
    while(1)
    {
        if(fgets(str1,sizeof(str1),fp1)!=NULL)
        {
            write_with_newline(fp3,str1);
        }
        if(fgets(str2,sizeof(str2),fp2)!=NULL)
        {
           write_with_newline(fp3,str2); 
        }
        if(feof(fp1)&&feof(fp2))
        {
            break;
        }
    }
    while (fgets(str1, sizeof(str1), fp1) != NULL)
        write_with_newline(fp3,str1);

    while (fgets(str2, sizeof(str2), fp2) != NULL)
        write_with_newline(fp3,str2);
    fclose(fp1);
    fclose(fp2);
    fclose(fp3);
    return 0;
}
```
