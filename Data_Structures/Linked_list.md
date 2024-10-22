#  Linked Lists


#### Comparision with Arrays
Linked List:

- Data Structure: Non-contiguous
- Memory Allocation: Typically allocated one by one to individual elements
- Insertion/Deletion: Efficient
- Access: Sequential
  
Array:

- Data Structure: Contiguous
- Memory Allocation: Typically allocated to the whole array
- Insertion/Deletion: Inefficient
- Access: Random

#### Introduction

A Linked list is a list of nodes linked together.

Each node contains 2 parts- data and the address of its previous element.

Linked follows dynamic memory allocation.

When we add or remove elements we need not have to shift the elements like arrays.

A big benefit with using linked lists is that nodes are stored wherever there is free space in memory, the nodes do not have to be stored contiguously right after each other like elements are stored in arrays.

The image below shows how a linked list can be stored in memory. The linked list has four nodes with values 3, 5, 13 and 2, and each node has a pointer to the next node in the list.

![image](https://github.com/user-attachments/assets/d0df3d88-9201-4aa3-8050-85ca3627c3df)

The first node in a linked list is called the "Head", and the last node is called the "Tail".

Something not so good with linked lists is that we cannot access a node directly like we can with an array by just writing myArray[5] for example. To get to node number 5 in a linked list, we must start with the first node called "head", use that node's pointer to get to the next node, and do so while keeping track of the number of nodes we have visited until we reach node number 5.

A sample code describing creation of a linked list in C:

``` C
#include<stdio.h>
#include<stdlib.h>

typedef struct Node			//creating a structure node.
{
	
	int data;				// data which represents data stored in the node.
	struct Node* next;		//a pointer named node that points to the next data item's address in the current node.
	
}Node;

Node* createnode(int data)	// a function createnode to create such nodes
{
	Node* newNode=(Node*)malloc(sizeof(Node));// dynamically allocating memory for our newnode, this operation is performed each time we create a newnode
	if(!newNode)			//checks whether the newnode pointer is null
	{
		printf("Memory Allocation failed");	  //if the newnode pointer is null, prints this statement
		exit(1);			//it is a fucntion call that terminates the program immediately.
	}
	newNode->data=data;		//the argument that we pass in the function is the dataitem of our node,and we assign that to our newnode here.
	newNode->next=NULL;		//every time we add a dataitem we assign the next i.e., the next pointer which has to store the address of the next node
	return newNode;			//returing the newnode
}

void printlist(Node* node)
{
	while(node)				//this while pointer checks if the node pointer is not null,if true prints the data;
	{
		printf("%d->",node->data);
		node=node->next;
	}
	printf("null\n");		//as the next pointer of the last node is null,this statement prints null right next to the last node.
}

int main()
{
	Node* node1=createnode(1);//adding newnodes using createnode() function
	Node* node2=createnode(2);
	Node* node3=createnode(3);
	Node* node4=createnode(4);
	Node* node5=createnode(5);
	
	node1->next=node2;		  //pointing the next pointer of each node to the next data that we're adding above
	node2->next=node3;
	node3->next=node4;
	node4->next=node5;
	
	printlist(node1);
	
	free(node1);				//right after the creation of all nodes is completed, we'll free up the space that we've alloacted for all the nodes as it is considered a good practise as it prevents memory leaks.
	free(node2);
	free(node3);
	free(node4);
	free(node5);
	
	return 0;
	
}
```

#### Types of Linked Lists
There are three basic forms of linked lists:

Singly linked lists
Doubly linked lists
Circular linked lists

### Single Linked List
A singly linked list is the simplest kind of linked lists. It takes up less space in memory because each node has only one address to the next node, like in the image below.

A singly linked list.
A doubly linked list has nodes with addresses to both the previous and the next node, like in the image below, and therefore takes up more memory. But doubly linked lists are good if you want to be able to move both up and down in the list.

![image](https://github.com/user-attachments/assets/401d9322-f8e4-4998-b319-e86e787b8269)

#### Operations on Single Linked List

We can perform the following operations on a SLL.

They are-

##### Traversing/Traversal

Traversing refers to travelling through each and every node of the Linked List.\

here's a C code describing Traversing through and printing all elements of a Singly Linked List.

Source Code:

``` C
#include <stdio.h>			// C code for traversal through a linkedlist
#include <stdlib.h>

typedef struct Node 		//creating a node structure
{
    int data;
    struct Node* next;
} Node;

void traverseAndPrint(Node* head)//function to traverse through the LL and print the elements
{
    Node* currentNode = head;	//we'll first point the current node to head.
    while (currentNode) 		//a while loop to check whether the node does not point to NULL
    {
        printf("%d -> ", currentNode->data);// if the pointer does not point to NULL,it prints the data that the next is pointing to
        currentNode = currentNode->next;	//make the next node as currentnode
    }
    printf("null\n");			//printing NULL statement for the last node,whose pointer points to NULL
}

int main()
{
    Node* node1 = (Node*)malloc(sizeof(Node));//dynamically allocating memory for all the newnodes
    Node* node2 = (Node*)malloc(sizeof(Node));
    Node* node3 = (Node*)malloc(sizeof(Node));
    Node* node4 = (Node*)malloc(sizeof(Node));
    Node* node5 = (Node*)malloc(sizeof(Node));

    node1->data = 7;			//assiging data values to the node
    node2->data = 11;
    node3->data = 3;
    node4->data = 2;
    node5->data = 9;

    node1->next = node2;		//pointing next pointer of each node to it's next node
    node2->next = node3;
    node3->next = node4;
    node4->next = node5;
    node5->next = NULL;

    traverseAndPrint(node1);	//function call to traverse through and print the linked list

    // Free the allocated memory
    free(node1);
    free(node2);
    free(node3);
    free(node4);
    free(node5);
    return 0;
}
```

output:

![image](https://github.com/user-attachments/assets/119db57a-a2b0-49a4-a568-f4cc9a20cfed)

#### Insertion



A doubly linked list.
A circular linked list is like a singly or doubly linked list with the first node, the "head", and the last node, the "tail", connected.


![image](https://github.com/user-attachments/assets/5a40444e-2763-49c7-a44c-307c4338629e)


In singly or doubly linked lists, we can find the start and end of a list by just checking if the links are null. But for circular linked lists, more complex code is needed to explicitly check for start and end nodes in certain applications.

Circular linked lists are good for lists you need to cycle through continuously.

![image](https://github.com/user-attachments/assets/615a34cd-d7cc-40b9-9e80-617bf0dc3c0f)


The image below is an example of a singly circular linked list:

A circular singly linked list.
The image below is an example of a doubly circular linked list:

A circular doubly linked list.
