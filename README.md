EXP NO:16 C PROGRAM TO SEARCH A GIVEN ELEMENT IN THE GIVEN LINKED LIST.

Aim: 

To write a C program to search a given element in the given linked list.

Algorithm:

Define the structure for a node in a linked list.
Define the search function to find a specific character in the linked list.
Initialize the head of the linked list as needed.
Call the search function and perform other linked list operations as needed.

Program:

    struct Node{
    struct Node *next; 
    char data;
    }*head;
    void search(char data)
    {
    struct Node *ptr;
    char item=data; 
    int i=0,flag;
    ptr = head; 
    if(ptr == NULL)
    {
        printf("Empty List\n");  
    }
    else
    {
        while (ptr!=NULL)
        {
            if(ptr->data == item)
            {
                printf("item %c found at location %d ",item,i+1); 
                flag=0;    
            }
            i++;
            ptr = ptr -> next;   
        }
        if(flag!=0)
        {
            printf("Item not found\n");
        }
    }
    }
Output:

<img width="879" height="607" alt="image" src="https://github.com/user-attachments/assets/27baec10-ba84-49c3-bbb9-70e3e04e97d2" />

Result: 

Thus, the program to search a given element in the given linked list is verified successfully.

EXP NO:17 PROGRAM TO INSERT A NODE IN A LINKED LIST.
Aim: 

To write a C program to insert a node in a linked list.

Algorithm:

Define the structure for a node in a linked list
Define the insert function to insert a new node with character data at the end of the linked list.
Initialize the head of the linked list as needed.
Call the insert function and perform other linked list operations as needed.

Program:

    struct Node{ 
    char data;
    struct Node *next;
    }*head;
    void insert(char data)
    {
    struct Node *n=(struct Node*)malloc(sizeof(struct Node));
    struct Node *temp;
    if(head==NULL)
    {
        head=n;
        n->data=data; 
        n->next=NULL; 
        temp=head; 
        return;
    }
    while(temp->next!=NULL)
    {
    temp=temp->next;
    }
    n->data=data; 
    n->next=NULL;
    temp->next=n;
    }
    
Output: 

<img width="584" height="519" alt="image" src="https://github.com/user-attachments/assets/7e93e48d-3354-49f9-87ee-88b0fdf16032" />

Result: 

Thus, the program to insert a node in a linked list is verified successfully.

EXP NO:18 C PROGRAM TO TRAVERSE A DOUBLY LINKED LIST

Aim: 

To write a C program to traverse a doubly linked list.

Algorithm:

Initialize a temporary pointer (temp) to the head of the list.
Use a while loop to traverse the list until the end (temp == NULL) is reached.
Inside the loop, print the data of the current node.
Move to the next node by updating the temp pointer to point to the next node (temp = temp->next).

Program:

    struct Node
    {
    struct Node *prev; 
    struct Node *next; 
    int data;
    }*head;
    void display()
    {
    struct Node *temp; 
    temp=head; 
    while(temp!=0)
    {
        printf("%d ",temp->data); 
        temp=temp->next;
        
    }
    }
    
Output:

<img width="489" height="590" alt="image" src="https://github.com/user-attachments/assets/7f894e91-7f00-4c73-b0ca-05a08bf1f75e" />

Result:

Thus, the program to traverse a doubly linked list is verified successfully.

EXP NO:19 C PROGRAM TO INSERT AN ELEMENT IN DOUBLY LINKED LIST 

Aim: 

To write a C program to insert an element in doubly linked list

Algorithm:

Create a new node (newNode) and allocate memory for it.
Set the data of the new node to the provided value.
If the list is empty, set the new node as the head.
If the list is not empty, traverse the list to find the last node.
Set the new node's prev pointer to the last node and update the last node's next pointer to the new node.

Program:

    struct Node
    {
    struct Node *prev;
    struct Node *next;
    float data;
    }*head;
    void insert(float data)
    {
    struct Node *n=(struct Node*)malloc(sizeof(struct Node));
    struct Node *temp;
    if(head==NULL)
    {
    head=n;
    n->data=data;
    n->next=NULL; 
    n->prev=NULL; 
    temp=head;
    }
    else
    {
    while(temp->next!=NULL)
    {
        temp=temp->next;        
    }
    n->data=data; 
    n->next=NULL; 
    n->prev=temp; 
    temp->next=n;  
    }
    }
    
Output:


Result:

Thus, the program to insert an element in doubly linked list is verified successfully.

EXP NO:20 C FUNCTION TO DELETE A GIVEN ELEMENT IN THE GIVEN LINKED LIST

Aim: To write a C function that deletes a given element from a linked list.

Algorithm:

Check if the Linked List is Empty: o If the head of the linked list is NULL, print a message indicating the list is empty and exit the function.
Traverse the Linked List: o Start from the head node and iterate through the list to find the node that contains the given element (data).
Handle Deletion of the First Node: o If the element to be deleted is found in the head node:  Update the head of the linked list to point to the next node (i.e., head = head->next).  Free the memory allocated to the node to be deleted.  Exit the function.
Traverse and Delete from the Middle or End: o If the element is not in the head node, continue traversing the list by checking each node’s next pointer. o When the node with the element is found, update the previous node’s next pointer to point to the next node of the node to be deleted (prev->next = current->next). o Free the memory allocated to the node to be deleted.
Handle the Case when the Element is Not Found: o If the element is not found in any node, print a message indicating the element is not present in the list.
End the Function.

Program:

    struct Node{
    char data; 
    struct Node *next;
    }*head;
    void delete()
    {
    if(head==NULL){
        printf("List is empty\n");
        return;
    }
    else if(head->next==NULL){
        head=NULL;
        free(head);
        printf("Node deleted from the begining ...\n");
    }
    else{
        struct Node *ptr;
        ptr=head;
        head=head->next;
        free(ptr);
        printf("Node deleted from the begining ...\n");
    }

Output:

<img width="1033" height="646" alt="image" src="https://github.com/user-attachments/assets/610a9f6a-ede3-428e-bb5b-0ba0cad59ebd" />

Result: 

Thus, the function that deletes a given element from a linked list is verified successfully.


