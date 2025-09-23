## function sum
```c
#include<stdio.h>
main()
{
        int a,b,s;
        scanf("%d %d",&a,&b);
        s=sum(a,b);
        printf("%d",s);
}
int sum(int x,int y)
{
        int s=x+y;
        return s;
}
```
## number reverse using funtions
```c
#include<stdio.h>
int reverse(int n);
main()
{
      int n,k;
      printf("enter the number");
      scanf("%d",&n);
      k=reverse(n);
      printf("%d",k);
}
int reverse(int n)
{
        int rem=0,sum=0,rev=0;
        while(n!=0)
        {
                rem=n%10;
                sum+=rem;
                rev=rev*10+rem;
                n/=10;
        }
        return rev;
}
```
## prime number using function
```c
#include<stdio.h>
main()
{
        int n;
        printf("enter the number");
        scanf("%d",&n);
        prime(n);
}
int prime(int n)
{
        int i,flag=1;
        for(i=2;i<=n/2;i++)
        {
                if(n%i==0)
                {
                     flag=0;
                     break;
                }
                else
                        flag=1;
        }
        if(flag==1 && n>2)
                printf("prime");
 else
                printf("Not prime");
}
```
## multiplication table
```c
#include<stdio.h>
main()
{
        int n;
        printf("enter the number:");
        scanf("%d",&n);
        mul(n);
}
int mul(int n)
{
     int i;
     for(i=1;i<=10;i++)
     printf("%d x %d=%d\n",n,i,n*i);
}
```
## factorial using functions
```c
#include<stdio.h>
main()
{
        int k,n=5;
        k=factorial(n);
        printf("%d",k);
}
int factorial(int n)
{
        int fact=1,i;
        for(i=1;i<=n;i++)
        {
                fact=fact*i;
        }
        return fact;
}
```
## function even or odd
```c
#include<stdio.h>
main()
{
        int n,k;
        printf("enter the number");
        scanf("%d",&n);
        k=even(n);
        if(k==1)
                printf("even");
        else
                printf("odd");
}
int even(int n)
{
        if(n%2==0)
                return 1;
        else
                return 0;
}
```
## funtion armstrong
```c
include<stdio.h>
main()
{
        int n,k;
        printf("enter the number");
        scanf("%d",&n);
        k=armstrong(n);
        if(k==1)
                printf("armstrong");
        else
                printf("not armstrong");
}
int armstrong(int n)
{
        int rem=0,sum=0,count,n1;
        while(n!=0)
        {
                n/=10;
                count++;
        }
        sum=0;
        n1=n;
        while(n!=0)
        {
                rem=n%10;
                sum+=rem;
                n/=10;
        }
        if(n1==sum)
                return 1;
        else
                return 0;
}
```
## call by reference
```c
#include<stdio.h>
main()
{
      int a,b,c,tot;
      scanf("%d %d %d",&a,&b,&c);
      add(&a,&b,&c,&tot);
      printf("%d",tot);
}
add(int *aptr,int *bptr,int *cptr,int *tot)
{
        *tot=*aptr+*bptr+*cptr;
}
```
## swaping
```c
#include<stdio.h>
main()
{
        int a,b;
        scanf("%d %d",&a,&b);
        swap(&a,&b);
        printf("%d %d",a,b);
}
int swap(int *aptr,int *bptr)
{
        int temp;
        temp=*aptr;
        *aptr=*bptr;
        *bptr=temp;
}
```
## array element delete using functions
```c
#include<stdio.h>
int arrdel(int arr[],int pos,int num);
main()
{
        int arr[5],pos,num,i;
        printf("enter the number");
        scanf("%d",&num);
        printf("enter the del pos");
        scanf("%d",&pos);
        for(i=0;i<num;i++)
            scanf("%d",&arr[i]);
        arrdel(arr,pos,num);
}
int arrdel(int arr[],int pos,int num)
{
        int temp,i;
        for(i=pos+1;i<num;i++)
        {
                temp=arr[i];
                arr[i]=arr[i-1];
                arr[i-1]=temp;
        }
        for(i=0;i<num-1;i++)
printf("%d",arr[i]);
}
```
## recursion fibnocci series
```c
#include<stdio.h>
int fib(int num);
main()
{
        int num,k;
        printf("enter the number");
        scanf("%d",&num);
        fib(num);
}
int fib(int a)
{
        int f;
        if(a==1)
            return 0;
        if(a==2)
            return 1;
        f=fib(a-1)+fib(a-2);
        printf("%d",f);
}
```
## factorial 
```c
#include<stdio.h>
int factorial(int num);
main()
{
        int num,k;
        printf("enter the number");
        scanf("%d",&num);
        k=factorial(num);
        printf("%d",k);
}
int factorial(int a)
{
        int fact;
        if(a==1)
           return 1;
        fact=a*factorial(a-1);
        return fact;
}
```
## recursion sum
```c
#include<stdio.h>
int sum(int n);
main()
{
        int n,k;
        printf("enter the number");
        scanf("%d",&n);
        k=sum(n);
        printf("%d",k);
}
int sum(int n)
{
        int s=0;
        if(n==0)
            return 0;
        s=n+sum(n-1);
        return s;
}
```
## 
