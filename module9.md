## EXP NO:11 C PROGRAM TO DISPLAY STACK ELEMENTS USING AN ARRAY.

Aim:
To write a C program to display stack elements using an array.
Algorithm:
1.	Include Necessary Header Files
2.	Declare Global Variables
3.	Define the Display Function
4.	Main Function (or Other Relevant Code)
5.	Initialize the stack and top as needed.
6.	Perform stack operations (push, pop, etc.).
7.	Use the display function to visualize the stack's contents 
 
Program:
```
#include <stdio.h>
float stack[100];
int top = -1;

void display(){
    if (top == -1){
        printf("Stack is empty\n");
    }else{
        for (int i = top; i >= 0; i--)
            printf("%.1f\n", stack[i]);
    }
}
```

Output:

<img width="594" height="988" alt="image" src="https://github.com/user-attachments/assets/dfec0de0-ac96-4dfc-8d8f-de43b49a74a8" />




Result:
Thus, the program to display stack elements using an array is verified successfully.
 

## EXP NO:12  PROGRAM TO PUSH THE GIVEN ELEMENT IN TO A STACK USING ARRAY.
Aim:
To create a C program to push the given element in to a stack using array.
Algorithm:
1.	Declare global variables for the stack size, top index, and the stack itself.
2.	Define the push function to add a floating-point number to the stack.
3.	Initialize the stack size, top index, and the stack itself.
4.	Call the push function as needed.
 
Program:
```
int size=3;
float stack[100];
int top=-1;
void push(float data)
{
    if(top==size-1)
    {
        printf("stack is full\n");
    }
    else
    {
        top++;
        stack[top]=data;
    }
}
```

Output:


<img width="1012" height="863" alt="image" src="https://github.com/user-attachments/assets/0ce32dfb-bf31-47e3-ae56-6a39d79902eb" />





Result:
Thus, the program to push the given element in to a stack using array is verified successfully


 
## EXP NO:13 C PROGRAM TO DISPLAY QUEUE ELEMENTS USING ARRAY.
Aim:
To write a C program to display queue elements using array

Algorithm:
1.	Declare global variables for the queue, rear, front, and iteration.
2.	Define the display function to print the elements of the queue.
3.	Initialize the queue, rear, and front as needed.
4.	Call the display function and perform other queue operations as needed.
 
Program:
```
int rear,front;
int i;
char queue[50];
void display()
{
    if(rear==-1&&front==-1)
    {
    printf("No elements to display");
    }
    else
    {
        for(i=front;i<=rear;i++)
        {
            printf("%c\n",queue[i]);
        }
    }
}
```

Output:

<img width="1270" height="809" alt="image" src="https://github.com/user-attachments/assets/6de3e23f-6b0e-48ee-a044-c4e1cc6986b9" />



Result:
Thus, the program to display queue elements using array is verified successfully.


 
## EXP NO:14 C PROGRAM TO INSERT ELEMENTS IN QUEUE USING ARRAY.
Aim:
To write a C program to insert elements in queue using array.

Algorithm:
1.	Declare global variables for the size, rear, front, and the queue itself.
2.	Define the enqueue function to add a float to the queue.
3.	Initialize the rear, front, and size of the queue as needed.
4.	Call the enqueue function as needed.

Program:

```
int size=10,rear=-1,front=-1;
float queue[50];
void enqueue(float data)
{
    if(rear<size)
    {
        if(front==-1)
        {
            front=0;
        }
        rear++;
        queue[rear]=data;
    }
}
```

Output:

<img width="1272" height="685" alt="image" src="https://github.com/user-attachments/assets/d2cf0607-597e-4495-8128-84db92abee59" />


Result:
Thus, the program to insert elements in queue using array is verified successfully.



 
## EXP NO:15 C FUNCTION TO DELETE ELEMENTS IN QUEUE USING ARRAY



Aim:

To create a function in C that deletes an element from a queue implemented using an array.

Algorithm:

1.	Check if the Queue is Empty
o	If the front pointer is -1, it means the queue is empty, and there are no elements to delete. Print a message indicating that the queue is empty.
2.	Delete the Front Element
o	If the queue is not empty, the element at the front index is deleted.
o	Increment the front pointer by 1 to remove the element and point to the next element in the queue.
3.	Check if the Queue Becomes Empty After Deletion:
o	After deletion, check if the front pointer has passed the rear pointer (front > rear). If this is true, reset both front and rear to -1, indicating that the queue is now empty.
4.	End the Function.



Program:

```
int front, rear;
void dequeue(){
    if(rear==-1&&front==-1)
        printf("Queue Underflow.\n");
    else
        front=+1;
}
```

Output:

<img width="962" height="904" alt="image" src="https://github.com/user-attachments/assets/191876fe-0219-4f5c-905b-0adfa20e2e2b" />



Result:
Thus, the function that deletes an element from a queue implemented using an array is verified successfully.
