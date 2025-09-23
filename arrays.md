## array printing
```c
#include<stdio.h>
main()
{
int arr[100],i,n;
printf("enter the array size:");
scanf("%d",&n);
printf("enter the array elements:");
for(i=0;i<n;i++)
{
        scanf("%d",&arr[i]);
}
printf("peinting the array elements:");
printf("{ ");
for(i=0;i<n;i++)
{
        printf("%d, ",arr[i]);
}
printf(" }");
}
```
## array sum
```c
#include<stdio.h>
main()
{

printf("enter the array size:");
scanf("%d",&size);
printf("enter the array elements");
for(i=0;i<size;i++)
{
        scanf("%d",&arr[i]);
}
for(i=0;i<size;i++)
{
        printf("%d",arr[i]);
        sum=sum+arr[i];
}
printf("%d",sum);
}
```
## array reverse
```c
#include<stdio.h>
main()
{
        int arr[100],i,temp,j,n;
        printf("enter the size");
        scanf("%d",&n);
        for(i=0;i<n;i++)
        {
                scanf("%d",&arr[i]);
        }
        for(i=0,j=n-1;i<j;i++,j--)
        {
                temp=arr[i];
                arr[i]=arr[j];
                arr[j]=temp;
        }
        for(i=0;i<n;i++)
                printf("%d",arr[i]);
}
```
## array transpose
```c
#include<stdio.h>
main()
{
    int a[100][100],i,j,arr[100][100],r,c,temp;
    printf("enter the size");
    scanf("%d %d",&r,&c);
    printf("enter the matrix");
    for(i=0;i<r;i++)
    {
            for(j=0;j<c;j++)
                   scanf("%d",&a[i][j]);
    }
    for(i=0;i<r;i++)
    {
            for(j=0;j<c;j++)
            {
                    arr[j][i]=a[i][j];
            }
    }
    for(i=0;i<r;i++)
    {
            for(j=0;j<c;j++)
            {
                 printf("%d ",arr[i][j]);
            }
            printf("\n");
    }
 }
```
## array copy
```c
#include<stdio.h>
main()
{
int a[100],b[100],i,n;
printf("enter the size of array:");
scanf("%d",&n);
printf("enter the array elements:");
for(i=0;i<n;i++)
{
        scanf("%d",&a[i]);
}
for(i=0;i<n;i++)
{
        printf("%d",a[i]);
}
b[i]=a[i];
for(i=0;i<n;i++)
{
        printf("%d",b[i]);
}
}
```
## array square
```c
#include<stdio.h>
main()
{
    int a[100],i,res;
    printf("enter the array elements:");
    for(i=0;i<5;i++)
    {
            scanf("%d",&a[i]);
    }
    for(i=0;i<5;i++)
    {
            printf("%d\n",a[i]*a[i]);
    }
}
```
## array max and min element
```c
#include<stdio.h>
main()
{
        int arr[5]={1,2,3,4,5};
        int i,large,small;
        large=small=arr[0];
        for(i=1;i<5;i++)
        {
                if(arr[i]<small)
                     small=arr[i];
                if(arr[i]>large)
                      large=arr[i];
        }
        printf("%d %d ",small,large);
}
```
## array sort
```c
#include<stdio.h>
main()
{
        int a[100],i,n,j,temp;
        printf("enter the size");
        scanf("%d",&n);
        printf("enter the array elements");
        for(i=0;i<n;i++)
              scanf("%d",&a[i]);
        for(i=0;i<n-1;i++)
        {
                for(j=0;j<n-i-1;j++)
                {
                        if(a[j]>a[j+1])
                        {
                                temp=a[j];
                                a[j]=a[j+1];
                                a[j+1]=temp;
                        }
                }
        }
 printf("enter the sorted");
        for(i=0;i<n;i++)
             printf("%d",a[i]);
}
```
## array upper triangle
```c
#include<stdio.h>
main()
{
        int a[10][10],i,j,r,c;
        printf("enter the rows and cols");
        scanf("%d %d",&r,&c);
        printf("enter the matrix");
        for(i=0;i<r;i++)
        {
                for(j=0;j<c;j++)
                        scanf("%d",&a[i][j]);
        }
        for(i=0;i<r;i++)
        {
                for(j=i;j<r;j++)
                {
                        printf("%d",a[i][j]);
                }
                printf("\n");
        }
}
```
## array second max number
```c
#include<stdio.h>
main()
{
        int arr[100],num,i,j,max,max1;
        printf("enter the number");
        scanf("%d",&num);
        max=arr[0];
        printf("enter the array elements");
        for(i=0;i<num;i++)
                scanf("%d",&arr[i]);
        for(i=0;i<num;i++)
        {
                if(arr[i]>max)
                {
                        max=arr[i];
                }
        }
        max1=arr[1];
        for(i=1;i<num;i++)
        {
                if(arr[i]>max1 && arr[i]<max)
                {
                        max1=arr[i];
                }
        }
        printf("%d",max1);
}
```
## array second minimum number
```c
#include<stdio.h>
main()
{
        int arr[100],num,i,min,min1;
        printf("enter the number");
        scanf("%d",&num);
        printf("enter the array elemnets");
        for(i=0;i<num;i++)
                scanf("%d",&arr[i]);
        min=arr[0];
        for(i=0;i<num;i++)
        {
                if(arr[i]<min)
                      min=arr[i];
        }
        min1=arr[1];
        for(i=1;i<num;i++)
        {
                if(arr[i]<min1 && arr[i]>min)
                       min1=arr[i];
        }
        printf("%d",min);
        printf("%d",min1);
}
```
## array even and odd numbers sort
```c
#include<stdio.h>
main()
{
        int a[100],i,j,temp,n;
        printf("enter the number");
        scanf("%d",&n);
        printf("enter the array elements");
        for(i=0;i<n;i++)
            scanf("%d",&a[i]);
        for(i=0;i<n-1;i++)
        {
                for(j=0;j<n-i-1;j++)
                {
                if(a[j]%2==0)
                {
                        temp=a[j];
                        a[j]=a[j+1];
                        a[j+1]=temp;
                }
                }
        }
        for(i=0;i<n;i++)
                printf("%d",a[i]);
}
```
## missing number in array
```c
#include<stdio.h>
main()
{
        int arr[10],i,n,sum=0,m=0,t_sum=0;
        printf("enter the number");
        scanf("%d",&n);
        for(i=0;i<n;i++)
        {
                scanf("%d",&arr[i]);
        }
        for(i=0;i<n-1;i++)
        {
                t_sum+=arr[i];
        }
        sum=(n*(n+1))/2;
        m=sum-t_sum;
        printf("%d",m);
}
```
## sphere matrix
```c
#include<stdio.h>
main()
{
        int arr[10][10],i,j,r,c,count=0;
        printf("enter the row and col");
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
                for(j=0;j<r;j++)
                {
                        if(arr[i][j]==0)
                        {
                             count++;
                        }
                }
        }
             printf("count %d",count);
        if(count>=5)
        {
            printf("sphare matrix");
        }
        else
        {
                printf("not sphare matrix");
        }
}
```
## max value in row
```c
#include<stdio.h>
main()
{
        int arr[10][10],i,j,r,c,max,sum=0;
        scanf("%d %d",&r,&c);
        for(i=0;i<r;i++)
        {
                for(j=0;j<c;j++)
                {
                        scanf("%d",&arr[i][j]);
                }
        }
        max=0;
        for(i=0;i<r;i++)
        {
                sum=0;
                for(j=0;j<c;j++)
                {
                        sum+=arr[i][j];
                        if(sum>max)
                        {
                                max=sum;
                        }
                 }
        }
        printf("%d",max);
}
```
## array unique element
```c
#include<stdio.h>
main()
{
        int a[6],count=0,i,j;
        printf("enter the elements");
        for(i=0;i<6;i++)
        {
                scanf("%d",&a[i]);
        }
        for(i=0;i<6;i++)
        {
                count=0;
             for(j=i+1;j<6;)
             {
                if(a[i]==a[j] && i!=j){
                    count++;
                    break;
                }
             j++;
             }
             if(count==0)
                 printf("%d",a[i]);
        }
}
```
## array left diagonal sum
```c
#include<stdio.h>
main()
{
        int a[10][10],i,j,r,c,sum=0;
        printf("enter the row and cols");
        scanf("%d %d",&r,&c);
        printf("enter the matrix");
        for(i=0;i<r;i++)
        {
                for(j=0;j<c;j++)
                     scanf("%d",&a[i][j]);
        }
        int n=r;
        for(i=0;i<r;i++)
        {
                        sum+=a[i][n-i-1];
        }
        printf("%d",sum);
}
```
## array duplicate elements
```c
#include<stdio.h>
main()
{
        int a[100],i,count,j,n,temp;
        printf("enter the size of array");
        scanf("%d",&n);
        printf("enter the array elements");
        for(i=0;i<n;i++)
             scanf("%d",&a[i]);
        for(i=0;i<n-1;i++)
        {
                for(j=0;j<n-i-1;j++)
                {
                        if(a[j]>a[j+1])
                        {
                                temp=a[j];
                                a[j]=a[j+1];
                                a[j+1]=temp;
                        }
                }
        }
        for(i=0;i<n;i++)
        {
                count=1;
                for(j=i+1;j<n;j++)
                {
                  if(a[i]==a[j])
                        count++;
                }
                if(count>0)
                        printf("%d %d",a[i],count);
        }
}
```
## printing the 2d array
```c
#include<stdio.h>
main()
{
        int a[100][100],b[100][100],i,j;
        printf("enter the array elements:");
        for(i=0;i<3;i++)
        {
                for(j=0;j<3;j++)
                {
                        scanf("%d",&a[i][j]);
                }
        }
        printf("enter the 2nd array elements:");
        for(i=0;i<3;i++)
        {
                for(j=0;j<3;j++)
                {
                        scanf("%d",&b[i][j]);
                }
        }
        printf("print the array elements");
        for(i=0;i<3;i++)
        {
               for(j=0;j<3;j++)
                {
                        printf("%d",a[i][j]);
                        printf("%d",b[i][j]);
                }
        }

}
```
## macro array
```c
#include<stdio.h>
main()
{
#define SIZE 5
        int i,arr[SIZE];
        for(i=0;i<SIZE;i++)
             scanf("%d",&arr[i]);
        for(i=0;i<SIZE;i++)
             scanf("%d",arr[i]);
}
```
## column sum
```c
#include<stdio.h>
main()
{
        int arr[10][10],i,j,r,c,max,sum=0;
        printf("enter the row and col");
        scanf("%d %d",&r,&c);
        for(i=0;i<r;i++)
        {
                for(j=0;j<c;j++)
                {
                        scanf("%d",&arr[i][j]);
                }
        }
        sum=0;
        for(i=0;i<r;i++)
        {
                for(j=0;j<c;j++)
                {
                        max=0;
                        sum+=arr[j][i];
                        if(sum>max)
                        {
                                max=sum;
                        }
                        sum=0;
                }
        }
        printf("%d",max);
}
```
## array delete
```c
#include<stdio.h>
main()
{
        int a[100],i,j,temp,d,n;
        printf("enter the size");
        scanf("%d",&n);
        printf("enter the array elements");
        for(i=0;i<n;i++)
                scanf("%d",&a[i]);
        printf("enter the deleting position");
        scanf("%d",&d);
        for(i=d+1;i<n;i++)
        {

                                temp=a[i];
                                a[i]=a[i-1];
                                a[i-1]=temp;
        }
        for(i=0;i<n-1;i++)
             printf("%d",a[i]);
}
```
## upper and lower triangle matrix print
```c
#include<stdio.h>
main()
{
        int arr[10][10],i,j,m,n;
        printf("enter the m and n");
        scanf("%d %d",&m,&n);
        for(i=0;i<n;i++)
        {
                for(j=0;j<m;j++)
                {
                        scanf("%d",&arr[i][j]);
                }
        }
        printf("lower");
        for(i=0;i<n;i++)
        {
                for(j=0;j<m;j++)
                {
                        if(i>=j)
                        {
                                printf("%d",arr[i][j]);
                        }
                        else
                        {
                                printf("\n");
                        }
                }
        }
        printf("uper");
        for(i=0;i<n;i++)
        {
                for(j=0;j<m;j++)
                {
                        if(i<=j)
                        {
                                printf("%d",arr[i][j]);
                        }
                        else
                                printf("\n ");
                }
        }
}
```
## number inserting in array at particular position
```c
#include<stdio.h>
main()
{
        int arr[10],i,j,n,p,temp,val;
        printf("enter the num");
        scanf("%d",&n);
        for(i=0;i<n;i++)
                scanf("%d",&arr[i]);
        printf("enter the insert position");
        scanf("%d",&p);
        printf("insert value");
        scanf("%d",&val);
        //for(i=0;i<n;i++)
            // scanf("%d",&arr[i]);
        for(i=n;i>=p;i--)
               arr[i]=arr[i-1];
        arr[p]=val;
        for(i=0;i<n+1;i++)
        {
                printf("%d",arr[i]);
        }
}
```










