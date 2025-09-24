## minimum and maximum number
```c
#include<stdio.h>
main()
{
        int a,b;
        scanf("%d %d",&a,&b);
        if(a>b)
        {
            printf("a is max");
            printf("b is min");
        }
        else
        {
            printf("a is min");
            printf("b is max");
        }
}
```
## weeknumber gives week day
```c
#include<stdio.h>
main()
{
int num;
printf("enter the number");
scanf("%d",&num);
if(num==0)
     printf("sunday");
else if(num==1)
     printf("monday");
else if(num==2)
     printf("tuesday");
else if(num==3)
     printf("wednesday");
else if(num==4)
     printf("thursday");
else if(num==5)
     printf("friday");
else
     printf("saturday");
}
```
## finding the character is upper or lower case
```c
#include<stdio.h>
main()
{
char ch;
printf("enter the character");
scanf("%c",&ch);
if(ch>'A'&&ch<'Z')
{
        printf("Uppercase");
}
else
{
       printf("lowercase");
}
}
```
## finding the number of days in the month
```c
#include<stdio.h>
main()
{
int year,mon;
printf("enter the month");
scanf("%d",&mon);
if(mon==1||mon==3||mon==5||mon==7||mon==8||mon==10||mon==12)
        printf("31");
else if(mon==4||mon==6||mon==9||mon==11)
        printf("30");
else
{
        if(mon==2)
        {
                if(year%4==0&&year%100!=0||year%400==0)
                     printf("28");
                else
                     printf("29");
        }
}
}
```
## maximum and minimum number using swith case
```c
#include<stdio.h>
main()
{
int a,b,res;
printf("enter the number");
scanf("%d %d",&a,&b);
res=a>b;
switch(res)
{
        case 1:
                printf("max is %d",a);
                break;
        case 0:
                printf("max is %d",b);
                break;
}
}
```
## even numbers from 1 to 20
```c
#include<stdio.h>
main()
{
int num,i;
printf("enter the number");
scanf("%d",&num);
for(i=1;i<=num;i++)
{
        if(i%2==0)
        {
                printf("%d\n",i);
        }
}
}
```
##  sum of numbers from 1 to 1000
```c
#include<stdio.h>
main()
{
int num,i,sum;
sum=0,i=1;
printf("enter the number");
scanf("%d",&num);
while(i<=num)
{
        sum=sum+i;
        i++;
}
printf("%d",sum);
}
```
## factorial of the given number
```c
#include<stdio.h>
main()
{
int num,i,fact=1;
printf("enter the number");
scanf("%d",&num);
for(i=1;i<=num;i++)
{
        fact=fact*i;
}
printf("%d",fact);
}
```
## prime number program
```c
#include<stdio.h>
main()
{
int num,flag=0,i;
printf("enter the number");
scanf("%d",&num);
for(i=2;i<=(num/2);i++)
{
        if(num%i==0)
        {
             flag=0;
             break;
        }
        else
                flag=1;
}
if(flag==1 && num>2)
        printf("prime number");
else
        printf("not prime number");
}
```
## sum of the digits of given number
```c
#include<stdio.h>
main()
{
int num,rem=0,sum=0;
printf("enter the number");
scanf("%d",&num);
while(num!=0)
{
        rem=num%10;
        sum=sum+rem;
        num=num/10;
}
printf("%d",sum);
}
```
## fibonnic series
```c
#include<stdio.h>
main()
{
int i,num,f,s,t;
f=0,s=1,t=0;
printf("enter the number");
scanf("%d",&num);
for(i=0;i<=num;i++)
{
        printf("%d\n",t);
        f=s;
        s=t;
        t=f+s;
}
}
```
## reverse the number
```c
#include<stdio.h>
main()
{
int num,rev=0,rem=0;
printf("enter the number");
scanf("%d",&num);
while(num!=0)
{
        rem=num%10;
        rev=rev*10+rem;
        num=num/10;
}
printf("%d",rev);
}
```
## largest number in the array
```c
#include<stdio.h>
main()
{
int num,i;
printf("enter the size of the array");
scanf("%d",&num);
int arr[num];
printf("enter the array elements");
for(i=0;i<num;i++)
{
        scanf("%d",&arr[i]);
}
int max=arr[0];
for(i=1;i<num;i++)
{
        if(max<arr[i])
        {
                max=arr[i];
        }
}
printf("%d",max);
}
```
## smallest number in the array
```c
#include<stdio.h>
main()
{
int num,i,a[100];
printf("enter the number");
scanf("%d",&num);
printf("enter the array elemnts");
for(i=0;i<num;i++)
     scanf("%d",&a[i]);
printf("print array elemnets");
for(i=0;i<num;i++)
     printf("%d",a[i]);
i=1;
int min=a[0];
while(i<num)
{
     if(a[i]<min)
     {
             min=a[i];
     }
i++;
}
printf("%d\n",min);
}
```
## printing array elements using for loop
```c
#include<stdio.h>
main()
{
int num,i,a[100];
printf("enter the size of array");
scanf("%d",&num);
printf("enter the array elements");
for(i=0;i<num;i++)
{
     scanf("%d",&a[i]);
}
printf("print the all elements");
for(i=0;i<num;i++)
{
        printf("%d ",a[i]);
}
}
```
## sum of the array elements using while loop
```c
#include<stdio.h>
main()
{
int num,i,a[100],sum;
sum=0;
printf("enter the size of array");
scanf("%d",&num);
printf("enter the array elements");
for(i=0;i<num;i++)
{
     scanf("%d",&a[i]);
}
i=0;
while(i<num)
{
     sum=sum+a[i];
     i++;
}
printf("sum = %d",sum);
}
```
## count the number of vowels in the string
```c
#include<stdio.h>
main()
{
char s[30];
int l,i,count=0;
printf("enter the string");
scanf("%s",&s);
for(i=0;s[i]!='\0';i++)
{
        char ch=s[i];
        if(ch=='a'||ch=='e'||ch=='i'||ch=='o'||ch=='u')
        {
             count++;
        }
}
printf("count = %d",count);
}
```
## count the number of words in the string
```c
#include<stdio.h>
main()
{
int i,count=0;
char str[100];
printf("enter the string");
fgets(str,sizeof(str),stdin);
i=0;
while(str[i]!='\0')
{
        if(str[i]==' ' || str[i]=='\t'|| str[i]=='\n')
                count++;
i++;
}
printf("count=%d",count);
}
```
## string palindrome
```c
#include<stdio.h>
main()
{
char str[100];
int i,j,n,len,flag=1;
printf("enter the string");
scanf("%s",&str);
for(i=0;str[i]!='\0';i++)
        len=len+1;
for(i=0,j=len-1;i<len/2;i++,j--)
{
        if(str[i]==str[j])
        {
                flag=1;
        }
        else
        {
                flag=0;
                break;
        }
}
if(flag==1)
        printf("string palindrome");
else
        printf("not string palindrome");
}
```
## concatinate 2 strings without predefined libraries
```c
#include<stdio.h>
main()
{
char s1[100],s2[100];
int i,j,len;
printf("enter the two strings: ");
scanf("%s %s",s1,s2);
i=0;
while(s1[i]!='\0')
{
     i++;
}
j=0;
while(s2[j]!='\0')
{
        s1[i]=s2[j];
        i++;
        j++;

}
s1[i]='\0';
printf("%s",s1);
}
```
## length of the string using for loop
```c
#include<stdio.h>
main()
{
char str[100];
int i,length;
length=0;
printf("enter the string");
scanf("%s",&str);
for(i=0;str[i]!='\0';i++)
{
        length++;
}
printf("%d",length);
}
```
## power of the number using for loop
```c
#include<stdio.h>
main()
{
int num,i,res,p;
res=1;
printf("enter the number");
scanf("%d %d",&num,&p);
for(i=1;i<=p;i++)
{
        res*=num;
}
printf("%d",res);
}
```
## gcd of the given numbers
```c
#include<stdio.h>
main()
{
int a,b,temp;
printf("enter the numbers");
scanf("%d %d",&a,&b);
while(b!=0)
{
        temp=b;
        b=a%b;
        a=temp;
}
printf("%d",a);
}
```
## lcm of the given numbers
```c
#include<stdio.h>
main()
{
int a,b,i,lcm;
printf("enter the numbers");
scanf("%d %d",&a,&b);
for(i=1;i<a*b;i++)
{
        if(i%a==0&&i%b==0)
        {
                lcm=i;
                break;
        }
}
printf("lcm=%d",lcm);
 }
```
## multiplication table
```c
#include<stdio.h>
main()
{
int num,i;
printf("enter the number");
scanf("%d",&num);
for(i=1;i<=10;i++)
{
        printf("%dx%d=%d\n",num,i,num*i);
}
}
```
## armstrong number using while loop
```c
#include<stdio.h>
#include<math.h>
int main()
{
int num,i,count,rem=0,sum=0,tarm=0;
for(i=1;i<=1000;i++)
{
    count=0;
    sum=0;
    num=i;
    while(num!=0)
    {
        num=num/10;
        count++;
    }
    num=i;
    while(num!=0)
    {
        rem=num%10;
        sum+=pow(rem,count);
        num=num/10;
    }
   if(sum==i)
  {
    printf("%d\n",i);
   }
}
}
```
## number palindrome
```c
#include<stdio.h>
main()
{
int k,num,rem,sum,rev;
sum=0,rev=0,rem=0;
printf("enter the number :");
scanf("%d",&num);
k=num;
while(num!=0)
{
        rem=num%10;
        sum=sum+rem;
        rev=rev*10+rem;
        num=num/10;
}
printf("sum=%d",sum);
printf("rev=%d\n",rev);
if(k==rev)
        printf("number palindrome");
else
        printf("not number palindrome");
}
```
## lower triangle matrix
```c
#include<stdio.h>
main()
{
int i,j,row,col,sum=0;
printf("enter the size of row and col:");
scanf("%d %d",&row,&col);
int m[row][col];
printf("Enter the matrix elements:");
for(i=0;i<row;i++)
{
        for(j=0;j<col;j++)
        {
                scanf("%d",&m[i][j]);
        }
}
printf("sum for the lower triangle matrix");
for(i=0;i<row;i++)
{
        for(j=0;j<=i;j++)
        {
                sum+=m[i][j];
        }
}
for(i=0;i<row;i++)
{
        for(j=0;j<=i;j++)
        {
                printf("%d",m[i][j]);
        }
        printf("\n");
}
printf("sum is %d:",sum);
}
```


