//Conctenation,Intersection,Union,Merge using linked list
#include<stdio.h>
#include<stdlib.h>
struct slist
{
    int data;
    struct slist *next;
};
typedef struct slist node;
node *create(node *first)
{
    node *new,*prev;
    int x;
    printf("Enter a value(enter -1 to stop)\n");
    scanf("%d",&x);
    while(x!=-1)
    {
        new=(node *)malloc(sizeof(node));
        new->data=x;
        new->next=NULL;
        if(first==NULL)
        {
            first=new;
            prev=new;
        }
        else
        {
            prev->next=new;
            prev=new;
        }
        printf("Enter a value(Enter -1 to stop)\n");
        scanf("%d",&x);
    }
    return first;
}
node *sort(node *l1)
{
    node *temp,*temp1;
    int t;
    for(temp=l1;temp->next!=NULL;temp=temp->next)
    {
        for(temp1=temp->next;temp1!=NULL;temp1=temp1->next)
        {
            if(temp->data>temp1->data)
            {
                t=temp->data;
                temp->data=temp1->data;
                temp1->data=t;
            }
        }
    }
    return l1;
}
node *con(node *l1,node *l2)
{
    node *temp;
    if(l1==NULL)
    {
        l1=l2;
    }
    else
    {
        temp=l1;
        while(temp->next!=NULL)
        {
            temp=temp->next;
        }
        temp->next=l2;
    }
    return l1;
}
node *addnode(node *l3,node *new)
{
    node *temp,*temp1;
    if(l3==NULL)
    {
        l3=new;
    }
    else if(l3->next==NULL)
    {
        l3->next=new;
    }
    else
    {
        temp=l3->next;
        temp1=l3;
        while(temp!=NULL)
        {
            temp1=temp;
            temp=temp->next;
        }
        temp1->next=new;
    }
    return l3;
}
node *uni(node *l1,node *l2)
{
    node *new,*l3=NULL;
    while(l1!=NULL && l2!=NULL)
    {
        new=(node *)malloc(sizeof(node));
        new->next=NULL;
        if(l1->data>l2->data)
        {
            new->data=l2->data;
            l3=addnode(l3,new);
            l2=l2->next;
        }
        else if(l1->data<l2->data)
        {
            new->data=l1->data;
            l3=addnode(l3,new);
            l1=l1->next;
        }
        else
        {
            new->data=l1->data;
            l3=addnode(l3,new);
            l1=l1->next;
            l2=l2->next;
        }
    }
    if(l1==NULL)
    {
        while(l2!=NULL)
        {
            new=(node *)malloc(sizeof(node));
            new->data=l2->data;
            new->next=NULL;
            l3=addnode(l3,new);
            l2=l2->next;
        }
    }
    if(l2==NULL)
    {
        while(l1!=NULL)
        {
            new=(node *)malloc(sizeof(node));
            new->data=l1->data;
            new->next=NULL;
            l3=addnode(l3,new);
            l1=l1->next;
        }
    }
    return l3;
}
node *intersection(node *l1,node *l2)
{
    node *new,*l3=NULL;
    while(l1!=NULL && l2!=NULL)
    {
        new=(node *)malloc(sizeof(node));
        new->next=NULL;
        if(l1->data>l2->data)
        {
            new->data=l2->data;
            l2=l2->next;
        }
        else if(l1->data<l2->data)
        {
            new->data=l1->data;
            l1=l1->next;
        }
        else
        {
            new->data=l1->data;
            l3=addnode(l3,new);
            l1=l1->next;
            l2=l2->next;
        }
    }
    return l3;
}
node *merge(node *l1,node *l2)
{
    node *new,*l3=NULL;
    while(l1!=NULL && l2!=NULL)
    {
        new=(node *)malloc(sizeof(node));
        new->next=NULL;
        if(l1->data>l2->data)
        {
            new->data=l2->data;
            l3=addnode(l3,new);
            l2=l2->next;
        }
        else if(l1->data<l2->data)
        {
            new->data=l1->data;
            l3=addnode(l3,new);
            l1=l1->next;
        }
        else
        {
            new->data=l1->data;
            l3=addnode(l3,new);
            new=(node *)malloc(sizeof(node));
            new->data=l1->data;
            new->next=NULL;
            l3=addnode(l3,new);
            l1=l1->next;
            l2=l2->next;
        }
    }
    if(l1==NULL)
    {
        while(l2!=NULL)
        {
            new=(node *)malloc(sizeof(node));
            new->data=l2->data;
            new->next=NULL;
            l3=addnode(l3,new);
            l2=l2->next;
        }
    }
    if(l2==NULL)
    {
        while(l1!=NULL)
        {
            new=(node *)malloc(sizeof(node));
            new->data=l1->data;
            new->next=NULL;
            l3=addnode(l3,new);
            l1=l1->next;
        }
    }
    return l3;
}
void display(node *first)
{
    node *temp=first;
    while(temp!=NULL)
    {
        printf("%d->",temp->data);
        temp=temp->next;
    }
    printf("NULL\n");
}
void main()
{
    node *l1,*l2,*l3;
    int ch;
    printf("Menu Driven\n1.Concatination\n2.Union\n3.Intersection\n4.Merge\n5.Exit");
    while(1)
    {
        printf("Enter your choice\n");
        scanf("%d",&ch);
        switch(ch)
        {
            case 1:l1=NULL;
                   l2=NULL;
                   printf("Enter first set\n");
                   l1=create(l1);
                   printf("Enter second set\n");
                   l2=create(l2);
                   printf("First set\n");
                   display(l1);
                   printf("Second set\n");
                   display(l2);
                   l3=con(l1,l2);
                   printf("Concatenation of two sets\n");
                   display(l3);
                   break;
            case 2:l1=NULL;
                   l2=NULL;
                   printf("Enter first set\n");
                   l1=create(l1);
                   printf("Enter second set\n");
                   l2=create(l2);
                   printf("First set\n");
                   display(l1);
                   printf("Second set\n");
                   display(l2);
                   l3=uni(sort(l1),sort(l2));
                   printf("Union of two sets\n");
                   display(l3);
                   break;
            case 3:l1=NULL;
                   l2=NULL;
                   printf("Enter first set\n");
                   l1=create(l1);
                   printf("Enter second set\n");
                   l2=create(l2);
                   printf("First set\n");
                   display(l1);
                   printf("Second set\n");
                   display(l2);
                   l3=intersection(sort(l1),sort(l2));
                   printf("Intersection of two sets\n");
                   display(l3);
                   break;
            case 4:l1=NULL;
                   l2=NULL;
                   printf("Enter first set\n");
                   l1=create(l1);
                   printf("Enter second set\n");
                   l2=create(l2);
                   printf("First set\n");
                   display(l1);
                   printf("Second set\n");
                   display(l2);
                   l3=merge(sort(l1),sort(l2));
                   printf("Merging of two sets\n");
                   display(l3);
                   break;
            case 5:exit(0);
                   break;
            default:printf("Check your choice\n");
        }
    }
    
}
