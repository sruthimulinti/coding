## malloc
```c
#include<stdio.h>
main()
{
        int *ptr,n=15,i;
        ptr=(int*)malloc(n*sizeof(int));
        if(ptr==NULL)
        {
                printf("it contains null pointer");
        }
        for(i=0;i<n;i++)
        {
                ptr[i]=i+1;
        }
        for(i=0;i<n;i++)
        {
                printf("%d",ptr[i]);
        }
}
```
## calloc
```c
#include<stdio.h>
#include<stdlib.h>
main()
{
        //int *ptr,n=5,i;
        //ptr=(int*)calloc(n,sizeof(int));
        float n=10.5;
        int i;
        char *ptr;
        ptr=(float *)calloc(n,sizeof(float));
        if(ptr==NULL)
                printf("memory not allocated");
        for(i=0;i<n;i++)
                ptr[i]=i+1;
        for(i=0;i<n;i++)
                printf("%d",ptr[i]);
        free(ptr);
}
```
## realloc
```c
#include<stdio.h>
#include<stdlib.h>
main()
{
        int *ptr,*ptr1,i,n=5;
        ptr=(int*)malloc(n*sizeof(int));
        if(ptr==NULL)
                printf("memory is not alloacted");
        for(i=0;i<n;i++)
                ptr[i]=i+1;
        //for(i=0;i<n;i++)
                //printf("%d",ptr[i]);
        ptr1=(int*)realloc(ptr,10*sizeof(int));
        for(i=0;i<10;i++)
                ptr[i]=(i+1)*10;
        for(i=0;i<10;i++)
                printf("%d",ptr1[i]);
        free(ptr);
}
```
## pointer print
```c
#include<stdio.h>
main()
{
        char str[10]="viven";
        char *ptr=str;
        printf("%s",ptr+2);
}
```
## print pointer
```c
#include<stdio.h>
main()
{
        int val=25;
        int *ptr;
        ptr=&val;
        printf("%d\n",val);
        printf("%d\n",*ptr);
        printf("%p\n",&val);
        printf("%p\n",ptr);
}
```
## pointer array
```c
#include<stdio.h>
main()
{
        int i,arr[5]={10,20,30,40,50};
        int *ptr;
        ptr=&arr;
        for(i=0;i<5;i++)
                printf("%d\n",*(arr+i));
        for(i=0;i<5;i++)
                printf("%p\n",ptr++);
}
```
## print sizeof pointer
```c
#include<stdio.h>
main()
{
        int val=25;
        int *ptr;
        ptr=&val;
        printf("%lu",sizeof(*ptr));
}
```
## pointer array sum
```c
#include<stdio.h>
main()
{
        int arr[100],n,i,sum=0;
        int *ptr;
        printf("enter the size");
        scanf("%d",&n);
        for(i=0;i<n;i++)
        {
                scanf("%d",&arr[i]);
        }
        ptr=arr;
        for(i=0;i<n;i++)
        {
                sum+=i[ptr];
        }
        printf("%d",sum);
}
```
## pointer 2d array
```c
#include<stdio.h>
main()
{
        int arr[10][10],i,j,r,c;
        int (*ptr)[4];
        ptr=arr;
        printf("row and col");
        scanf("%d %d",&r,&c);
        for(i=0;i<r;i++)
        {
                for(j=0;j<c;j++)
                {
                        scanf("%d",&arr[i][j]);
                }
        }
        for(i=0;i<r;i++)
        {
                for(j=0;j<c;j++)
                {
                        printf("%d\n",*(*(arr+i)+j));
                        printf("%p\n",(*(arr+i)+j));
                        printf("%d\n",*(*(ptr+i)+j));
                        printf("%p\n",(*(ptr+i)+j));
                }
        }
}
## function pointer
```c
#include<stdio.h>
main()
{
        int a=10;
        modify(a);
        printf("%d",a);
}
int modify(int a)
{
        a=a+1;
}
```


