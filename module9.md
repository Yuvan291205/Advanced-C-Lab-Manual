# NAME: YUVAN M
# REG NO: 212223240188

EXP NO:11 C PROGRAM TO DISPLAY STACK ELEMENTS USING AN ARRAY.

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
int stack[100],top,i;
void display()
{
    if(top==-1){
        printf("Stack is empty");
    }
    
    else{
        for(i=top;i>=0;i--){
            printf("%d->",stack[i]);
        }
    }
}
```
Output:

<img width="994" height="662" alt="image" src="https://github.com/user-attachments/assets/61b48230-58a2-4011-ada8-5e3b43cd584d" />



Result:
Thus, the program to display stack elements using an array is verified successfully.
 

EXP NO:12  PROGRAM TO PUSH THE GIVEN ELEMENT IN TO A STACK USING ARRAY.
Aim:
To create a C program to push the given element in to a stack using array.
Algorithm:
1.	Declare global variables for the stack size, top index, and the stack itself.
2.	Define the push function to add a floating-point number to the stack.
3.	Initialize the stack size, top index, and the stack itself.
4.	Call the push function as needed.
 
Program:

```
int size=3,top=-1;
float stack[100];
void push (float data)
{
    if(top==size-1){
        printf("stack is full\n");
    }
    else{
        top++;
        stack[top] = data;
    }
}
```
Output:

<img width="989" height="589" alt="image" src="https://github.com/user-attachments/assets/845a4234-a1ae-41da-84c3-f68d50a95876" />




Result:
Thus, the program to push the given element in to a stack using array is verified successfully


 
EXP NO:13 C PROGRAM TO DISPLAY QUEUE ELEMENTS USING ARRAY.
Aim:
To write a C program to display queue elements using array

Algorithm:
1.	Declare global variables for the queue, rear, front, and iteration.
2.	Define the display function to print the elements of the queue.
3.	Initialize the queue, rear, and front as needed.
4.	Call the display function and perform other queue operations as needed.
 
Program:

```
float queue[50];
int front=-1,rear=-1;
void display()
{
    if(front == -1){
        printf("No elements to display\n");
    }
    else{
        for(int i = front;i<=rear;i++){
            printf("%.1f ",queue[i]);
        }
    }
}
```
Output:

<img width="991" height="588" alt="image" src="https://github.com/user-attachments/assets/1b9e8eb8-31bd-4e65-90df-3bc8a3c36570" />


Result:
Thus, the program to display queue elements using array is verified successfully.


 
EXP NO:14 C PROGRAM TO INSERT ELEMENTS IN QUEUE USING ARRAY.
Aim:
To write a C program to insert elements in queue using array.

Algorithm:
1.	Declare global variables for the size, rear, front, and the queue itself.
2.	Define the enqueue function to add a float to the queue.
3.	Initialize the rear, front, and size of the queue as needed.
4.	Call the enqueue function as needed.

Program:

```
float queue[50];
int size=10,front=-1,rear=-1;
void enqueue(float data)
{
    if(rear<size){
        if(front==-1){
            front=0;
        }
        rear++;
        queue[rear] = data;
    }
    
}
```
Output:

<img width="990" height="492" alt="image" src="https://github.com/user-attachments/assets/93eb61be-c551-4f61-bad7-ce43eefd6bec" />

Result:
Thus, the program to insert elements in queue using array is verified successfully.



 
EXP NO:15 C FUNCTION TO DELETE ELEMENTS IN QUEUE USING ARRAY



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
void dequeue()
{
    if(front==-1||front>rear){
        printf("No elements to display");
    }
    else{
        front++;
    }
}
```
Output:

<img width="999" height="731" alt="image" src="https://github.com/user-attachments/assets/e1382ce2-4254-45e5-b2e5-b341ed276f00" />


Result:
Thus, the function that deletes an element from a queue implemented using an array is verified successfully.
