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
##4.Write a C program to read a file and count:
    Total number of characters
    Total number of words
    Total number of lines
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

