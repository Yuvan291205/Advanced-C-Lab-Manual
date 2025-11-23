### NAME: YUVAN M
### REG NO: 212223240188
EXP NO:16 C PROGRAM TO SEARCH A GIVEN ELEMENT IN THE GIVEN LINKED LIST.
Aim:
To write a C program to search a given element in the given linked list.

Algorithm:
1.	Define the structure for a node in a linked list.
2.	Define the search function to find a specific character in the linked list.
3.	Initialize the head of the linked list as needed.
4.	Call the search function and perform other linked list operations as needed.
 
Program:

```
struct Node{
    float data; 
    struct Node *next;
}*head;

void search(float data)
{
    struct Node *temp;
    int i = 0 ,flag;
    temp = head;
    if(temp == NULL){
        printf("Empty List");
    }
    else{
        while(temp!=NULL){
            if(temp->data == data){
                printf("item %.2f found at location %d\n",temp->data,i+1);
                flag = 0;
            }
            i++;
            temp=temp->next;
        }
        if(flag!=0){
            printf("Item not found\n");
        }
    }
}
```

Output:

<img width="1084" height="474" alt="image" src="https://github.com/user-attachments/assets/c8a93d2b-1f4c-449f-b30b-4b60f2a946c4" />



Result:
Thus, the program to search a given element in the given linked list is verified successfully.


 
EXP NO:17  PROGRAM TO INSERT A NODE IN A LINKED LIST.
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
    char data; 
    struct Node *next;
}*head;


void insert(char data)
{
    struct Node *n = (struct Node*)malloc(sizeof(struct Node));
    struct Node *t;
    if(head == NULL)
    {
        head = n;
        head->data = data;
        n->next = NULL;
        return;
    }
    t = head;
    while(t->next!=NULL)
    {
        t = t->next;
    }
    n->data = data;
    n->next = NULL;
    t->next = n;
}

```
Output:

<img width="992" height="581" alt="image" src="https://github.com/user-attachments/assets/bb08af86-7d06-4483-9825-a3a920d2cf81" />

 
Result:
Thus, the program to insert a node in a linked list is verified successfully.


 
EXP NO:18 C PROGRAM TO TRAVERSE A DOUBLY LINKED LIST
Aim:
To write a C program to traverse a doubly linked list.

Algorithm:
1.	Initialize a temporary pointer (temp) to the head of the list.
2.	Use a while loop to traverse the list until the end (temp == NULL) is reached.
3.	Inside the loop, print the data of the current node.
4.	Move to the next node by updating the temp pointer to point to the next node (temp = temp->next).
 
Program:

  ```
struct Node
{
    struct Node *prev;
    struct Node *next;
    float data;
}*head;

void display()
{
    struct Node *ptr;
    ptr = head;
    while(ptr!=NULL)
    {
        printf("%.2f\n",ptr->data);
        ptr = ptr->next;
    }
}
```
Output:

<img width="992" height="558" alt="image" src="https://github.com/user-attachments/assets/a008b0ec-44f4-4f9b-8244-aab62079f859" />


Result:
Thus, the program to traverse a doubly linked list is verified successfully. 



EXP NO:19 C PROGRAM TO INSERT AN ELEMENT IN DOUBLY LINKED LIST
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
struct Node
{
    struct Node *prev;
    struct Node *next;
    float data;
}*head;

void insert(float data)
{
    struct Node *ptr = (struct Node *)malloc(sizeof(struct Node));
    struct Node *temp;
    if(ptr == NULL)
    {
        printf("OVERFLOW\n");
    }
    else
    {
        ptr->data = data;
        if(head == NULL)
        {
            ptr ->prev = NULL;
            ptr->next = NULL;
            head = ptr;
        }
        else
        {
            temp = head;
            while(temp->next!=NULL){
                temp = temp->next;
            }
            temp -> next = ptr;
            ptr ->next = NULL;
            ptr ->prev = temp;
        }
    }
}
```

Output:

<img width="994" height="530" alt="image" src="https://github.com/user-attachments/assets/3c75fdc9-3472-447b-a956-d055657be67c" />


Result:
Thus, the program to insert an element in doubly linked list is verified successfully.




EXP NO:20 C FUNCTION TO DELETE A GIVEN ELEMENT IN THE GIVEN LINKED LIST




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
    int data; 
    struct Node *next;
}*head;
void delete()
{
    struct Node *ptr;
    
    if(head == NULL){
        printf("List is empty\n");
    }
    else
    {
        ptr = head;
        head = head->next;
        free(ptr);
        printf("Node deleted from the begining ...\n");
    }
}
```
Output:

<img width="1080" height="691" alt="image" src="https://github.com/user-attachments/assets/bf27c1ec-0016-4f62-a104-396178183566" />





Result:
Thus, the function that deletes a given element from a linked list is verified successfully.
