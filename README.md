# halloween


Practical 8

Aim: Write a C program to open, read and write into a file.


Code:

#include <stdio.h>
#include <stdlib.h>

int main()
{
   char num[50];
   FILE *fptr;
   fptr = fopen("hi.txt","w");

   if(fptr == NULL)
   {
      printf("Error!");   
      exit(1);             
   }

   printf("Enter Your Text: ");
   scanf("%s",&num);

   fprintf(fptr,"%s",num);
   fclose(fptr);

   if ((fptr = fopen("hi.txt","r")) == NULL){
       printf("Error! opening file");

       exit(1);
   }

   fscanf(fptr,"%s", &num);

   printf("Value of n = %s", num);
   fclose(fptr); 
  

   return 0;
}
