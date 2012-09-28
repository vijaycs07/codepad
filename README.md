#include<stdio.h>
#include<stdlib.h>

struct node
{
int num;
struct node* next;
};

void  push(struct node** head,int num)
{
struct node* tmp;
tmp=(struct node*)malloc(sizeof(struct node));
tmp->num=num;
tmp=(*head);
(*head)=tmp;
}

void display(struct node* head)
{
printf("%u",head);
while(head !=NULL)
{
printf("%d",head->num);
head=head->next;
}
}

int main()
{
struct node* p=NULL;
push(&p,12);
push(&p,21);
display(p);
return (0);
}
