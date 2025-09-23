##  Strings compare without predefined funtions
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
}
```
## string copy without predefined functions
```c
#include<stdio.h>
main()
{
        char s1[10],s2[10];
        int i;
        printf("enter the string");
        gets(s1);
        while(s1[i]!='\0')
        {
                s2[i]=s1[i];
        i++;
        }
        s2[i]='\0';
        printf("%s",s1);
        printf("%s",s2);
}
```
## string frequency
```c
#include<stdio.h>
#include<string.h>
main()
{
        char str[100];
        int i,freq[256]={0};
        printf("enter the string");
        scanf("%s",str);
        for(i=0;str[i]!='\0';i++)
        {
                freq[(unsigned char)str[i]]++;
        }
        for(i=0;i<256;i++)
        {
                   if(freq[i]>0)
                   {
                    printf("%c= %d\n",i,freq[i]);
                   }
        }
}
```
## string swap
```c
#include<stdio.h>
main()
{
        char str1[10],str2[10],temp[10];
        int i,j;
        printf("enter the string");
        scanf("%s %s",str1,str2);
        for(i=0;str1[i]!='\0'|| str2[i]!='\0';i++)
        {
                    temp[i]=str1[i];
                    str1[i]=str2[i];
                    str2[i]=temp[i];
        }
        printf("%s\n",str1);
        printf("%s\n",str2);
}
```
## string replace with the character in poisition 
```c
#include<stdio.h>
main()
{
        char str[20];
        int i;
        printf("enter the string");
        gets(str);
        while(str[i]!='\0')
        {
                if(str[i]==' ')
                     str[i]='u';
        i++;
        }
        /*while(str[i]!='\0')
        {
            printf("%c",str[i]);
            i++;
        }*/
        printf("%s",str);
}
```
## string anagram
```c
#include<stdio.h>
main()
{
        char str1[100],str2[100];
        int i,j,f1[256]={0},f2[256]={0},count=0;
        scanf("%s %s",str1,str2);
        for(i=0;str1[i]!='\0';i++)
        {
                f1[(unsigned char)str1[i]]++;
        }
        for(i=0;i<256;i++)
        {
                if(f1[i]>0)
                {
                        printf("%c %d",i,f1[i]);
                }
        }
        for(j=0;str2[j]!='\0';j++)
        {
                f2[(unsigned char)str2[i]]++;
        }
        for(j=0;j<256;j++)
        {
                           if(f2[j]>0)
                {
                        printf("%c %d",i,f2[j]);
                }
        }
        for(i=0;str1[i]!='\0';i++)
        {
                for(j=0;str2[j]!='\0';j++)
                {
                if(f1[i]==f2[j])
                {
                        count++;
                }
                }
        }
        if(count>1)
                printf("anagram");
        else
              printf(" not anagram");
}
```
## string word count
```c
#include<stdio.h>
main()
{
        char str[10];
        int i,count=0;
        printf("enter the string");
        scanf("%s",str);
        while(str[i]!='\0')
        {
                if(str[i]!='\0' && str[i]!='\t')
                {
                      count++;
                }
                i++;
        }
        printf("%d",count);
}
```
## string alphabets , digits ,symbols count
```c
#include<stdio.h>
main()
{
        char str[20];
        int i,alp=0,num=0,sym=0;
        printf("enter the string");
        scanf("%s",str);
        while(str[i]!='\0')
        {
                if((str[i]>='a' && str[i]<='z')||(str[i]>='A' && str[i]<='Z'))
                        alp++;
                else if(str[i]>='0' && str[i]<='9')
                        num++;
                else
                        sym++;
        i++;
        }
        printf("alp=%d",alp);
        printf("num=%d",num);
        printf("sym=%d",sym);
}
```
## string pointer
```c
#include<stdio.h>
main()
{
        char str[10];
        char *ptr;
        ptr=str;
        printf("enter the string");
        scanf("%s",str);
        while(*ptr!='\0')
        {
                printf("%c\n",*ptr);
                printf("%p\n",&ptr);
                ptr++;
        }
}
```
## string converting upper to lower and lower to upper
```c
#include<stdio.h>
main()
{
        char str[100];
        int i;
        printf("enter the string");
        gets(str);
        while(str[i]!='\0')
        {
                if(str[i]>='a' && str[i]<='z')
                      str[i]= str[i]-32;
                else
                      str[i]= str[i]+32;
        i++;
        }
        for(i=0;str[i]!='\0';i++)
                printf("%c",str[i]);
}
```
## substring found
```c
#include<stdio.h>
main()
{
        char str[100],sub[100];
        int i,j,k,found=0;
        printf("enter the string");
        fgets(str,sizeof(str),stdin);
        printf("enter the substring");
        scanf("%s",sub);
        for(i=0;str[i]!='\0';i++)
        {
                j=0;
                k=i;
                while(str[k]!='\0' && sub[j]!='\0' && str[k]==sub[j])
                {
                        k++;
                        j++;
                }
                if(sub[j]=='\0')
                {
                        found=1;
                        break;
                }
        }
                if(found)
                {
                        printf("substring found");
                }
                else
                        printf("substring notfound");
}
```
## string vowel or consonent
```c
#include<stdio.h>
main()
{
        char str[10];
        int i,vow=0,con=0;
        printf("enter the string");
        scanf("%s",str);
        while(str[i]!='\0')
        {
                if(str[i]=='a'||str[i]=='e'||str[i]=='o'||str[i]=='i'||str[i]=='u')
               {
                       vow++;
               }
                else
                        con++;
        i++;
        }
        printf("vow=%d\n",vow);
        printf("con=%d\n",con);
}
```
## string sort
```c
#include<stdio.h>
main()
{
        char str[100];
        int i,len=0,temp=0,j;
        printf("enter the string");
        gets(str);
        for(i=0;str[i]!='\0';i++)
        {
                len++;
        }
        for(i=0;i<len-1;i++)
        {
                for(j=i+1;j<len;j++)
                {
                        if(str[i]>str[j])
                        {
                                temp=str[i];
                                str[i]=str[j];
                                str[j]=temp;
                        }
                }
        }
 printf("%s",str);
}
```
## string from start to end index
```c
#include<stdio.h>
main()
{
        char str[10];
        int s,e,i;
        printf("enter the string");
        scanf("%s",str);
        printf("start end");
        scanf("%d%d",&s,&e);
        for(i=s ;i<=e;i++)
        {
                printf("%c",str[i]);
        }
}
```
## string reverse
```c
#include<stdio.h>
main()
{
        char str[10];
        int i,len=0;
        printf("enter the string");
        scanf("%s",str);
        for(i=0;str[i]!='\0';i++)
        {
                len++;
        }
        for(i=len;i>=0;i--)
        {
                printf("%c",str[i]);
        }
}
```
## string before new line 
```c
#include<stdio.h>
main()
{
        char str[20];
        //="sruthi\nclass";
        int i,n=3;
        printf("enter the string");
        for(i=0;i<n;i++)
        {
            fgets(str,sizeof(str),stdin);
            if(i==0)
                    printf("%s",str);
        }
        i=0;
        while(str[i]!='\0')
        {
                        printf("%c",str[i]);
                        if(str[i]=='\n')
                                break;
        i++;
        }
```
## smallest word and largest word
```c
include<stdio.h>
main()
{
        char str;
        int min,max,word;
        printf("enter the string");
        gets(str);
        len=strlen(str);
        min=len;
        max=0;
        word='\0';
        for(i=0;i<=len;i++)
        {
             if(strlen(word)>min)
             {
                    min=word;
                    strcpy(word,min);
             }
             else if(strlen(word)<max)
             {
                    max=word;
                    strcpy(word,max);
             }
 }
        printf("%s",min);
        printf("%s",max);
}
```
## string decompress
```c
#include<stdio.h>
#include<string.h>
main()
{
        char str[100],s[100];
        int i,k,count=0;
        printf("enter the string");
        scanf("%s",str);
        int j=0;
        for(i=0;str[i]!='\0';i++)
        {
                if(str[i]>'0' && str[i]<='9')
                {
                       k=str[i]-'0';
                       for(int l=0;l<k-1;l++)
                       {
                          s[j++]=str[i-1];
                       }
                }
                else
                        s[j++]=str[i];
        }
        s[j]='\0';
printf("%s",s);
}
```


                                                                              
                                                                              

                                                                                                                                                                                                 
