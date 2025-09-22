## Strings compare without predefined funtions
```c
#include<stdio.h>
main()
{
        char s1[100],s2[100];
        int i,flag=0;
        printf("enter the strings");
        gets(s1);
        gets(s2);
        while(s1[i]!= '\0' && s2[i]!= '\0')
        {
                if(s1[i]!=s2[i])
                {
                        flag=1;
                        break;
                }
                i++;
        }
        if(flag==0 && s1[i]== '\0' && s2[i]== '\0')
        {
                printf("both are equal");
        }
        else if(s1[i]<s2[i])
        {
         printf("s1 is small");
        }
        else
        {
                printf("s2 is small");
        }
```
