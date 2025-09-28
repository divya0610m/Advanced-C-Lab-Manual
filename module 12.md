

## EXP NO 26: C PROGRAM TO DISPLAY STACK ELEMENTS USING LINKED LIST.

Aim:

To write a C program to display stack elements using linked list.

Algorithm:

1.	Define a structure Node with two members: data to store the integer value and next to point to the next node in the linked list.
2.	Declare a global variable head representing the starting node of the linked list.
3.	Define a function display to print the elements of the linked list.
4.	Declare a pointer p and initialize it with the head of the linked list.
5.	Use a while loop to traverse the linked list:
6.	Print the data of the current node.
7.	Move to the next node using the next pointer. 
 
Program:

```
struct Node
{
  int data;
  struct Node *next;
}*head;
void display()
{
  struct Node *p;
  p=head;
  while(p!=NULL)
  {
    printf("%d\n",p->data);
    p=p->next;
  }
}

```

Output:

![image](https://github.com/user-attachments/assets/74ed14da-5bf7-42d5-91f1-d5396c0556d7)



Result:
Thus, the program to display stack elements using linked list is verified successfully. 



## EXP.NO 27: C PROGRAM TO POP AN ELEMENT FROM THE GIVEN STACK USING LINKED LIST.

Aim:

To write a C program to pop an element from the given stack using liked list.

Algorithm:

1.	Check for Empty Stack
2.	If head is equal to NULL, Print "Stack is empty."
3.	Else Proceed to the next step.
4.	Set head to point to the next node in the stack.
 
Program:

```
struct Node
{
int data;
struct Node *next;
}*head;
void pop()
{
  if(head==NULL)
  {
    printf("stack is empty");
  }
  else
  {
    head=head->next;
  }
}

```

Output:

![image](https://github.com/user-attachments/assets/f4120875-446e-4cd9-8968-55bf9bc2ab5d)




Result:
Thus, the program to pop an element from the given stack using liked list is verified successfully.

 
## EXP NO:28 C PROGRAM TO DISPLAY QUEUE ELEMENTS USING LINKED LIST.

Aim:

To write a C program to display queue elements using linked list.

Algorithm:

1.	Check if Queue is Empty
2.	Display Queue Elements
3.	Print the data of the current node pointed to by front
4.	Update front to point to the next node.
5.	End the display function.
 
Program:

```
struct Node
{
  char data;
  struct Node *next;
}*front=NULL,*rear=NULL;
void display()
{
  if(front==NULL)
  {
    printf("queue is empty");
  }
  else
  {
    printf("queue elements:\n");
    while(front!=NULL)
    {
      printf("%c\n",front->data);
      front=front->next;
    }
  }
}

```

Output:

![image](https://github.com/user-attachments/assets/63fba068-787c-4f01-a610-7a339ecd69ca)


Result:
Thus, the program to display queue elements using linked list is verified successfully.


 
## EXP NO:29 C PROGRAM TO INSERT ELEMENTS IN QUEUE USING LINKED LIST

Aim:

To write a C program to insert elements in queue using linked list

Algorithm:

1.	Allocate Memory for New Node
2.	Set Data and Next Pointer
3.	Check if Queue is Empty
4.	Set both front and rear to point to the new node p.
5.	Set the next pointer of the current rear to point to the new node p.
6.	End of Enqueue Operation
 
Program:

```
struct Node
{
  int data;
  struct Node *next;
}*front=NULL,*rear=NULL;
void enqueue(int data)
{
  struct Node *p=(struct Node*)malloc(sizeof(struct Node));
  p->data=data;
  p->next=NULL;
  if(front==NULL)
  {
    front=rear=p;
  }
  else
  {
    rear->next=p;
    rear=p;
  }
}

```

Output:

![image](https://github.com/user-attachments/assets/0aa232f1-62ff-41d7-81a2-d80af1922184)


Result:
Thus, the program to insert elements in queue using linked list is verified successfully.



## EXP NO:30 C FUNCTION TO FIND THE PEEK OF QUEUE USING LINKED LIST.


Aim:

The aim of this function is to retrieve the "peek" (the front element) of a queue implemented using a linked list

Algorithm:

1.	Check if the queue is empty:
o	If the queue is empty (i.e., the front pointer is NULL), return an error or a message indicating that the queue is empty.
2.	Access the front element:
o	If the queue is not empty, return the data stored in the front node of the linked list (i.e., the element at the head of the queue).

Program:

```
struct Node
{
   char data;
   struct Node *next;
}*front=NULL,*rear=NULL;
void peek()
{
    printf("%c",front->data);
}

```

Output:

![image](https://github.com/user-attachments/assets/510d44a2-a9b4-466b-a2d4-4803f2f48731)




Result:

Thus, the program to retrieve the "peek" (the front element) of a queue implemented using a linked list is verified successfully.

