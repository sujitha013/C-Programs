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
