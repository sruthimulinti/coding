## 
```c
1
22
333
4444
55555
```
##
```c
#include<stdio.h>
main()
{
int num,i,j;
printf("enter the number:");
scanf("%d",&num);
for(i=1;i<=num;i++)
{
        for(j=1;j<=i;j++)
        {
                printf("%d",i);
        }
        printf("\n");
}
}
```
##
```c
1
12
123
1234
12345
```
##
```c
#include<stdio.h>
main()
{
int num,i,j;
printf("enter the number");
scanf("%d",&num);
for(i=1;i<=num;i++)
{
        for(j=1;j<=i;j++)
        {
                printf("%d",j);
        }
        printf("\n");
}
}
```
## 
```c
1
23
456
78910
1112131415
flodys triangle
```
##
```c
#include<stdio.h>
main()
{
        int num,i,m=1,j;
        printf("enter the number:");
        scanf("%d",&num);
        for(i=1;i<=num;i++)
        {
                for(j=1;j<=i;j++)
                {
                        printf("%d",m);
                        m++;
                }
                printf("\n");
        }
}
```
##
```c
2
34
456
5678
678910
```
##
```c
#include<stdio.h>
main()
{
int num,m,i,j;
printf("enter the number");
scanf("%d",&num);
for(i=2;i<=num;i++)
{
        m=i;
        for(j=1;j<=i-1;j++)
        {
                printf("%d",m);
                m++;
        }
        printf("\n");
}
}
```
##
```c
5
54
543
5432
54321
```
##
```c
#include<stdio.h>
main()
{
        int num,i,j;
        printf("enter the number:");
        scanf("%d",&num);
        for(i=num;i>=1;i--)
        {
                for(j=num;j>=i;j--)
                {
                        printf("%d",j);
                }
                printf("\n");
        }
}
```
##
```c
5
44
333
2222
11111
```
##
```c
#include<stdio.h>
main()
{
        int num,i,j;
        printf("enter the number");
        scanf("%d",&num);
        for(i=num;i>=1;i--)
        {
                for(j=num;j>=i;j--)
                {
                        printf("%d",i);
                }
                printf("\n");
        }
}
```
##
```c
1
01
101
0101
10101
```
##
```c
#include<stdio.h>
main()
{
        int num,i,j;
        printf("ente the number:");
        scanf("%d",&num);
        for(i=1;i<=num;i++)
        {
                for(j=1;j<=i;j++)
                {
                     if((i+j)%2==0)
                             printf("1");
                     else
                             printf("0");
                }
                printf("\n");
        }
}
```
## 
```c
  *  *  *  *  *
  *  *  *  *
  *  *  *
  *  *
  *
```
##
##
```c
#include<stdio.h>
main()
{
        int num,i,j;
        printf("enter the number:");
        scanf("%d",&num);
        for(i=num;i>=1;i--)
        {
                for(j=1;j<=i;j++)
                {
                        printf("  *",i);
                }
                printf("\n");
        }
}
```
##
```c
55555
4444
333
22
1
```
##
```c
#include<stdio.h>
main()
{
        int num,i,j;
        printf("Enter the number");
        scanf("%d",&num);
        for(i=num;i>=1;i--)
        {
                for(j=1;j<=i;j++)
                {
                        printf("%d",i);
                }
               printf("\n");
        }
}
```
##
```c
12345
1234
123
12
1
```
##
```c
#include<stdio.h>
main()
{
    int num,i,j;
    printf("enter the number:");
    scanf("%d",&num);
    for(i=num;i>=1;i--)
    {
            for(j=1;j<=i;j++)
            {
                    printf("%d",j);
            }
            printf("\n");
     }
}
```
##
```c
54321
5432
543
54
5
```
##
```c
#include<stdio.h>
main()
{
        int num,i,j;
        printf("enter the number:");
        scanf("%d",&num);
        for(i=1;i<=num;i++)
        {
                for(j=num;j>=i;j--)
                {
                        printf("%d",j);
                }
                printf("\n");
        }
}
```
## 
```c
11111
2222
333
22
1
```
##
```c
#include<stdio.h>
main()
{
        int num,i,j;
        printf("enter the number");
        scanf("%d",&num);
        for(i=1;i<=num;i++)
        {
                for(j=num;j>=i;j--)
                {
                           if(i%2==0)
                                   printf("2");
                           else
                           {
                                   if(i==3)
                                        printf("3");
                                   else
                                        printf("1");
                           }
                }
                printf("\n");
        }
}
```
##
```c
    *
   **
  ***
 ****
*****
```
##
```c
#include<stdio.h>
main()
{
        int num,i,j,k;
        printf("enter the number:");
        scanf("%d",&num);
        for(i=1;i<=num;i++)
        {
                for(k=1;k<=num-i;k++)
                {
                        printf(" ");
                }
                for(j=1;j<=i;j++)
                {
                        printf("*",j);
                }
        printf("\n");
       }
}
```
## 
```c
      *
     *  *
    *  *  *
   *  *  *  *
  *  *  *  *  *
```
##
```c
#include<stdio.h>
main()
{
int num,k,i,j;
printf("enter the number");
scanf("%d",&num);
for(i=1;i<=num;i++)
{
        for(k=1;k<=num-i;k++)
              printf(" ");
        for(j=1;j<=i;j++)
              printf("  *",i);
        printf("\n");
}
}
```
##
```c
    *
   ***
  *****
 *******
*********
```
##
```c
#include<stdio.h>
main()
{
        int num,i,j,k;
        printf("enter the number:");
        scanf("%d",&num);
        for(i=1;i<=num;i++)
        {
                for(k=1;k<=num-i;k++)
                     printf(" ");
                for(j=1;j<=i;j++)
                     printf("*");
                for(j=1;j<i;j++)
                    printf("*");
              printf("\n");
        }
}
```
##
```c
    1
   123
  12345
 1234567
123456789
```
```c
#include<stdio.h>
main()
{
        int i,j,k,f,num,p;
        printf("enter the number:");
        scanf("%d",&num);
        for(i=1;i<=5;i++)
        {
                for(k=1;k<=num-i;k++)
                       printf(" ");
                for(j=1;j<=i;j++)
                       printf("%d",j);
                p=j;
                for(j=1;j<i;j++)
                {
                       printf("%d",p);
                       p++;
                }
        printf("\n");
        }
}
```
##
```c
    1
   232
  34543
 4567654
567898765
```
```c
#include<stdio.h>
main()
{
        int num,m,i,j,k,p;
        printf("enter the number:");
        scanf("%d",&num);
        for(i=1;i<=num;i++)
        {
                for(k=1;k<=num-i;k++)
                     printf(" ");
                m=i;
                for(j=1;j<=i;j++)
                {
                        printf("%d",m);
                        m++;
                }
                p=m-2;
                for(j=1;j<i;j++)
                {
                        printf("%d",p);
                        p--;
                }
               printf("\n");
}
}
```






