## creating a node
```c
#include<stdio.h>
#include<stdlib.h>
struct node{
        int data;
        struct node *link;
}
main()
{
struct node *head,*one,*two;
head=(struct node*)malloc(sizeof(struct node));
head->data=10;
head->link="NULL";
one=(struct node*)malloc(sizeof(struct node));
one->data=20;
head->link=one;
two=(struct node*)malloc(sizeof(struct node));
two->data=30;
head->link=two;
if(head==NULL)
        printf("it is empty");
while(head!="NULL")
{
        printf("%d %d",head->data,head->link);
}
}
```
## insering at begining
```c
#include<stdio.h>
#include<stdlib.h>
struct node{
        int data;
        struct node*next;
}
main()
{
        struct node*head=NULL;
        struct node*first=NULL;
        struct node*second=NULL;
        head=(struct node*)malloc(sizeof(struct node));
        first=(struct node*)malloc(sizeof(struct node));
        second=(struct node*)malloc(sizeof(struct node));
        head->data=10;
        head->next=first;
        first->data=20;
        first->next=second;
        second->data=30;
        second->next=NULL;
        struct node*temp=head;
        while(temp!=NULL)
        {
                printf("%d->",temp->data);
                temp=temp->next;
        }
        printf("NULL\n");
        struct node*new=NULL;
        new=(struct node*)malloc(sizeof(struct node));
        new->data=60;
        new->next=head;
        head=new;
        struct node*link=head;
        while(link!=NULL)
        {
                printf("%d->",link->data);
                link=link->next;
       }
        printf("NULL\n");
}
```
## insering at end
```c
#include<stdio.h>
#include<stdlib.h>
struct node{
        int data;
        struct node* next;
};
main()
{
        struct node* head=NULL;
        struct node* first=NULL;
        struct node* second=NULL;
        head=(struct node*)malloc(sizeof(struct node));
        first=(struct node*)malloc(sizeof(struct node));
        second=(struct node*)malloc(sizeof(struct node));
        head->data=10;
        head->next=first;
        first->data=20;
        first->next=second;
        second->data=30;
        second->next=NULL;
        struct node* temp=head;
        while(temp!=NULL)
        {
                printf("%d->",temp->data);
                temp=temp->next;
        }
        struct node* new=NULL;
        new=(struct node*)malloc(sizeof(struct node));
        second->next=new;
        new->data=55;
        new->next=NULL;
        struct node* link=NULL;
        while(link!=NULL)
        {
                printf("%d->",link->data);
                link=link->next;
       }
}
```
## deleting first node
```c
#include<stdio.h>
#include<stdlib.h>
struct node{
        int data;
        struct node *next;
}
main()
{
        struct node* head=NULL;
        struct node* first=NULL;
        struct node* second=NULL;
        head=(struct node*)malloc(sizeof(struct node));
        first=(struct node*)malloc(sizeof(struct node));
        second=(struct node*)malloc(sizeof(struct node));
        head->data=10;
        head->next=first;
        first->data=20;
        first->next=second;
        second->data=30;
        second->next=NULL;
        struct node* temp=head;
        while(temp!=NULL)
        {
                if(temp->next==NULL)
                {
                        printf("%d",temp->data);
                }
                else
                {
                printf("%d->",temp->data);
                }
                temp=temp->next;
        }
        first->next=NULL;
        struct node* link=head;
         while(link!=NULL)
        {
                printf("%d->",link->data);
                link=link->next;
        }
        printf("NULL\n");

}
```
## finding the middle node in the linkedlist
```c
#include<stdio.h>
#include<stdlib.h>
struct node
{
        int data;
        struct node* next;
}
struct node* head;
void createnode(int val)
{
        struct node* newnode=(struct node*)malloc(sizeof(struct node));
        newnode->data=val;
        newnode->next=NULL;
        if(head==NULL)
        {
                head=newnode;
        }
        else
        {
                struct node* temp=head;
                while(temp->next!=NULL)
                {
                        temp=temp->next;
                }
                temp->next=newnode;
        }
}
void display()
{
        struct node* temp=head;
        while(temp!=NULL)
        {
                printf("%d->",temp->data);
                temp=temp->next;
        }
        printf("NULL\n");
}
main()
{
        createnode(10);
        createnode(20);
        createnode(30);
        display();
}
```
## insering at begining,end,middle and particular position using functions
```c
#include<stdio.h>
#include<stdlib.h>
struct node{
        int data;
        struct node* next;
};
struct node* head=NULL;
void createnode(int val)
{

      struct node* newnode=(struct node*)malloc(sizeof(struct node*));
      newnode->data=val;
      newnode->next=NULL;
      if(head==NULL)
      {
              head=newnode;
      }
      else{
              struct node* temp=head;
              while(temp->next!=NULL){
                      temp=temp->next;
              }
              temp->next=newnode;
         }
}
void insertnodeend(int val)
{
        struct node* temp=head;
        struct node* newnode=(struct node*)malloc(sizeof(struct node));
        newnode->data=val;
        newnode->next=NULL;
        while(temp->next!=NULL)
        {
                temp=temp->next;
        }
        temp->next=newnode;
}
}
void insertnodeend(int val)
{
        struct node* temp=head;
        struct node* newnode=(struct node*)malloc(sizeof(struct node));
        newnode->data=val;
        newnode->next=NULL;
        while(temp->next!=NULL)
        {
                temp=temp->next;
        }
        temp->next=newnode;
}
void insertnodebeg(int val)
{
        struct node* temp=head;
        struct node* newnode=(struct node*)malloc(sizeof(struct node));
        newnode->data=val;
        newnode->next=head;
        head=newnode;
}
void insertnodemiddle(int val)
{
        struct node* temp=head;
int count=0;
        int mid;
        while(temp!=NULL)
        {
                count++;
                temp=temp->next;
        }
        mid=(count/2);
        temp=head;
        for(int i=1;i<mid;i++)
        {
                temp=temp->next;
        }
        struct node* newnode=(struct node*)malloc(sizeof(struct node));
        newnode->data=val;
        newnode->next=temp->next;
        temp->next=newnode;
}
void insertnodepos(int val,int pos)
{
        struct node* newnode=(struct node*)malloc(sizeof(struct node));
        newnode->data=val;
        newnode->next=NULL;
        if(pos==1)
        {
                newnode->next=head;
                head=newnode;
        }
 struct node* temp=head;
        for(int i=0;i<pos-1 && temp!=NULL;i++)
        {
                temp=temp->next;
        }
        if(temp==NULL)
        {
                printf("it is out of range");
        }
        newnode->next=temp->next;
        temp->next=newnode;
}
void display()
{
     struct node* temp=head;
     while(temp!=NULL)
     {
          printf("%d->",temp->data);
          temp=temp->next;
     }
     printf("NULL\n");
}
main()
{
        struct node *head=NULL;
    createnode(10);
    createnode(20);
    createnode(30);
    display();
    insertnodeend(60);
    display();
    insertnodebeg(40);
    display();
    insertnodemiddle(55);
    display();
    insertnodepos(88,3);
    display();
}
```
## deleting the nodes
```c
#include<stdio.h>
#include<stdlib.h>
struct node
{
        int data;
        struct node* next;
};
struct node* head=NULL;
void createnode(int val)
{
        struct node* newnode=(struct node*)malloc(sizeof(struct node));
        newnode->data=val;
        newnode->next=NULL;
        if(head==NULL)
        {
                head=newnode;
        }
        else
        {
             struct node* temp=head;
             while(temp->next!=NULL)
             {
                     temp=temp->next;
             }
             temp->next=newnode;
        }
}
void delnodebeg()
{
        if(head==NULL)
        {
             printf("list is empty");
        }
        struct node* temp=head;
        head=head->next;
        free(temp);
}
void delnodeend()
{
        if(head==NULL)
        {
                printf("list is empty");
        }
        if(head->next==NULL)
        {
                free(head);
                head=NULL;
        }
        struct node* temp=head;
        while(temp->next->next!=NULL)
        {
                temp=temp->next;
        }
        free(temp->next);
        temp->next=NULL;
}
void display()
{
        struct node* temp=head;
        while(temp!=NULL)
        {
                printf("%d->",temp->data);
                temp=temp->next;
        }
        printf("NULL\n");
}
main()
{
     createnode(10);
     createnode(20);
     createnode(30);
     display();
     delnodebeg();
     display();
     delnodeend();
     display();
}




