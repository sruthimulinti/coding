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


