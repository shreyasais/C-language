#include<stdio.h>
main()
{
int d1,d2,m1,m2,y1,y2,i,j,f1,f2,h1,h2,fh1,fh2,d,m,y;
clrscr();
printf("Enter the day,month and year for first date:(dd/mm/yyyy):");
scanf("%d/%d/%d",&d1,&m1,&y1);//07/07/2022
printf("Enter the day,month and year for second date:(dd/mm/yyyy):");
scanf("%d/%d/%d",&d2,&m2,&y2);//06/07/2022
i=d1;
switch(m1-1)
{
  case 11:i=i+30;
  case 10:i=i+31;
  case 9:i=i+30;
  case 8:i=i+31;
  case 7:i=i+31;
  case 6:i=i+30;
  case 5:i=i+31;
  case 4:i=i+30;
  case 3:i=i+31;
  case 2:i=i+28;
  case 1:i=i+31;
}
if(y1%4==0&&y1%100!=0||y1%400==0)
   if(m1>2)
   i=i+1;
f1=(y1-1)/4;
h1=(y1-1)/100;
fh1=(y1-1)/400;

j=d2;
switch(m2-1)
{
  case 11:j=j+30;
  case 10:j=j+31;
  case 9:j=j+30;
  case 8:j=j+31;
  case 7:j=j+31;
  case 6:j=j+30;
  case 5:j=j+31;
  case 4:j=j+30;
  case 3:j=j+31;
  case 2:j=j+28;
  case 1:j=j+31;
}
if(y2%4==0&&y2%100!=0||y2%400==0)
   if(m2>2)
   j=j+1;
f2=(y2-1)/4;
h2=(y2-1)/100;
fh2=(y2-1)/400;

    d=(i-j);
    printf("Difference in days:%d\n",d);
    m=(m1-m2);
    printf("Difference in months:%d\n",m);
    y=(y1-y2);
    printf("Difference in years:%d",y);
    
getch(); 
    
}

