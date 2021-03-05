#include <stdio.h>
struct node
{
    int data;
    struct node *link;
};

typedef struct node ll;
ll *first, *temp, *temp2,*newnode; int ch;
int pos=0;
int size=0;
int main()
{
    do
    {
        menu();
        printf("Enter your choice \n");
        scanf("%d",&ch);
        switch(ch)
        {
            case 1: insertAtEnd(); break;
            case 2: insertAtPos(); break;
            case 3: print(); break;
            case 4: printsize(); break;
            default: printf("Wrong choice choice 1 to 4");
        }
    }while(ch!=4);
    return 0;
}

void insertAtEnd()
{
    if(first==NULL)
    {
        first = (ll*)malloc(sizeof(ll));
        printf("Enter Data ");
        scanf("%d",&first->data);

        first->link = NULL;
        ++size;
        
        printf("inserted At End");
        return;
    }
    temp = first ;
    while(temp->link != NULL)
    {
        temp=temp->link;
    }
    temp2 = (ll*)malloc(sizeof(ll)); // New Last Node
    printf("Enter Data ");
    scanf("%d",&temp2->data);

    temp2->link = NULL; // NULL because it is going to be Last Node
    temp->link=temp2;
    ++size;

}

void print()
{
    temp = first;
    while(temp!=NULL)
    {
        printf("[%d %u]",temp->data,temp->link);
        temp = temp ->link;
    }
}
void printsize()
{
    printf("size is %d ",size);
}
void insertAtPos()
{
    if(first == NULL)
    {
        insertAtEnd();
    }
    
        printf("enter the position to insert\n");
        scanf("%d",&pos);
        if((pos<=0) || (pos>=size+2))  //check for valid position
        {
            printf("invalid position\n");
            return;
        }
        
        if(pos==1)
        {
            insertBeg();
            return;
        }
        temp=first;
        for(int i=0;i<pos-2;i++)
        {
            	temp = temp->link; // at the end of this loop pointer will be at pos -1 position
            }	// create  a new Node
             newnode = (ll*)malloc(sizeof(ll));
             printf("enter  data\n");
             scanf("%d",&newnode->data);
             newnode->link=temp->link;
             temp->link=newnode;
             printf("inserted node at %d",pos);
             ++size;
        
}
void insertBeg()
{
    if(first==NULL)
    {
        first = (ll *)malloc(sizeof(ll));
        printf("enter the data\n");
        scanf("%d",&first->data);
        first->link=NULL;
        printf("first node cerated\n");
    }
    else
    {
        newnode = (ll *)malloc(sizeof(ll));
        printf("enter data\n");
        scanf("%d",&newnode->data);
        newnode->link=first;
        first = newnode;
        printf("inserted node at beginning\n");
    }
}
void menu()
{ 
    printf("\n1 Insert \n2 insertAtPos \n3 Print \n4 size \n");
}
