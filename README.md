#include<stdio.h>

#include<conio.h>
int tower(int n,char beg,char aux,char end)
 {
 if(n==1)
 {
 printf("thed disk 1 is move from %c to %c\n",beg,end);
 return;
 }
 tower(n-1,beg,end,aux);
 printf("the disk %d is moved from %c to %c\n",n,beg,end);
 tower(n-1,aux,beg,end);
}
void main()
 {
int num;
printf("enter the number of disk \n");
scanf("%d",&num);
tower(num,'A','B','C');
getch();
 }
