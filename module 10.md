## EXP NO:16 C PROGRAM TO SEARCH A GIVEN ELEMENT IN THE GIVEN LINKED LIST.
Aim:
To write a C program to search a given element in the given linked list.

Algorithm:
1.	Define the structure for a node in a linked list.
2.	Define the search function to find a specific character in the linked list.
3.	Initialize the head of the linked list as needed.
4.	Call the search function and perform other linked list operations as needed.
 
Program:

```
#include <stdio.h>
struct Node{
    int data;
    struct Node *next; 
} *head = NULL;

void search(int data){
    struct Node *temp = head;
    int pos = 1;
    int found = 0;
    while (temp != NULL){
        if (temp->data == data){
            printf("item %d found at location %d\n", data, pos);
            found = 1;
            break;  
        }
        temp = temp->next;
        pos++;
    }
    if (!found) 
        printf("Item not found\n");
}

```

Output:

<img width="1250" height="889" alt="image" src="https://github.com/user-attachments/assets/52f2f528-b533-4dff-a4d9-527ba9340fab" />




Result:
Thus, the program to search a given element in the given linked list is verified successfully.


 
## EXP NO:17  PROGRAM TO INSERT A NODE IN A LINKED LIST.
Aim:
To write a C program to insert a node in a linked list.
Algorithm:
1.	Define the structure for a node in a linked list
2.	Define the insert function to insert a new node with character data at the end of the linked list.
3.	Initialize the head of the linked list as needed.
4.	Call the insert function and perform other linked list operations as needed.
 
Program:

```
struct Node{
    int data;
    struct Node *next;
} *head;

void insert(int data){
    struct Node *newN = (struct Node*)malloc(sizeof(struct Node));
    newN->data = data;
    newN->next = NULL;
    
    if (head == NULL){
        head = newN;   
    }else{
        struct Node *temp = head;
        while (temp->next != NULL)
            temp = temp->next;
        temp->next = newN;  
    }
}
```

Output:

<img width="708" height="925" alt="image" src="https://github.com/user-attachments/assets/f912fdbf-530d-46f2-87e6-3e18abdb8cab" />


 
Result:
Thus, the program to insert a node in a linked list is verified successfully.


 
## EXP NO:18 C PROGRAM TO TRAVERSE A DOUBLY LINKED LIST
Aim:
To write a C program to traverse a doubly linked list.

Algorithm:
1.	Initialize a temporary pointer (temp) to the head of the list.
2.	Use a while loop to traverse the list until the end (temp == NULL) is reached.
3.	Inside the loop, print the data of the current node.
4.	Move to the next node by updating the temp pointer to point to the next node (temp = temp->next).
 
Program:

```
struct Node{
    struct Node *prev;
    struct Node *next;
    float data;
}*head;

void display(){
    struct Node *ptr;
    ptr = head;
    while(ptr != NULL){
        printf("%.2f\n",ptr->data);
        ptr=ptr->next;
    }
}
```

Output:

<img width="464" height="661" alt="image" src="https://github.com/user-attachments/assets/645ee7f9-dde5-4edf-86a8-b702bbca4559" />



Result:
Thus, the program to traverse a doubly linked list is verified successfully. 



## EXP NO:19 C PROGRAM TO INSERT AN ELEMENT IN DOUBLY LINKED LIST
Aim:
To write a C program to insert an element in doubly linked list

Algorithm:
1.	Create a new node (newNode) and allocate memory for it.
2.	Set the data of the new node to the provided value.
3.	If the list is empty, set the new node as the head.
4.	If the list is not empty, traverse the list to find the last node.
5.	Set the new node's prev pointer to the last node and update the last node's next pointer to the new node.
 
Program:

```
struct Node {
    struct Node *prev;
    struct Node *next;
    int data;
} *head;

void insert(int data){
    struct Node *newNode = (struct Node*)malloc(sizeof(struct Node));
    newNode->data = data;
    newNode->next = NULL;
    newNode->prev = NULL;

    if (head == NULL){
        head = newNode;
        return;
    }
    struct Node *temp = head;
    while (temp->next != NULL)
        temp = temp->next;
    temp->next = newNode;
    newNode->prev = temp;
}

```

Output:

<img width="664" height="873" alt="image" src="https://github.com/user-attachments/assets/17dbad46-85fd-4c19-b801-e24764fa55dd" />



Result:
Thus, the program to insert an element in doubly linked list is verified successfully.




## EXP NO:20 C FUNCTION TO DELETE A GIVEN ELEMENT IN THE GIVEN LINKED LIST




Aim:
To write a C function that deletes a given element from a linked list.

Algorithm:
1.	Check if the Linked List is Empty:
o	If the head of the linked list is NULL, print a message indicating the list is empty and exit the function.
2.	Traverse the Linked List:
o	Start from the head node and iterate through the list to find the node that contains the given element (data).
3.	Handle Deletion of the First Node:
o	If the element to be deleted is found in the head node:
	Update the head of the linked list to point to the next node (i.e., head = head->next).
	Free the memory allocated to the node to be deleted.
	Exit the function.
4.	Traverse and Delete from the Middle or End:
o	If the element is not in the head node, continue traversing the list by checking each node’s next pointer.
o	When the node with the element is found, update the previous node’s next pointer to point to the next node of the node to be deleted (prev->next = current->next).
o	Free the memory allocated to the node to be deleted.
5.	Handle the Case when the Element is Not Found:
o	If the element is not found in any node, print a message indicating the element is not present in the list.
6.	End the Function.


Program:

```
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
}

```

Output:

<img width="970" height="766" alt="image" src="https://github.com/user-attachments/assets/b44baa83-c426-4af0-ab97-7f1eccac26ee" />






Result:
Thus, the function that deletes a given element from a linked list is verified successfully.





