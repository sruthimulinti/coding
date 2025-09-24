## structure declaring
```c
#include<stdio.h>
struct stu{
        char name[10];
        int age;
        float marks;
}s={"sri",23,2.5};
main()
{
        //struct stu s={"sri",20,2.6};
        printf("%s\n",s.name);
        printf("%d\n",s.age);
        printf("%f\n",s.marks);
}
```
## maximum marks in the structure
```c
#include<stdio.h>
struct stu{
        char name[10];
        int age;
        int marks;
}b[3];
main()
{
        int n,i,max;
        printf("enter the numbers");
        scanf("%d",&n);
        for(i=0;i<n;i++)
        {
                scanf("%s",&b[i].name);
                scanf("%d",&b[i].age);
                scanf("%d",&b[i].marks);
        }
        max=0;
        for(i=0;i<n;i++)
        {
                if(b[max].marks<b[i].marks)
                {
                        max=i;
 }
        }
        printf("%d",b[max].marks);
}
```
## structure copy
```c
#include<stdio.h>
struct stu{
        char name[10];
        int age;
        float marks;
}s,s1;
main()
{
        struct stu s={"sri",20,25};
        s1=s;
        printf("%s",s1.name);
        printf("%d",s1.age);
        printf("%f",s1.marks);
}
```
## 
