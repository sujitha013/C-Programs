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
