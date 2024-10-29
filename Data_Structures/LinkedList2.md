# Linked List

### Operations

Operations that we perform on a linked list-
- Creation

``` C
#include<stdio.h>
#include<stdlib.h>

typedef struct Node
{
	int data;
	struct Node* next;
	
}Node;

Node* createnode(int data)
{
	
	Node* newNode=(struct Node*)malloc(sizeof(struct Node));
	newNode->data=data;
	newNode->next=NULL;
	return newNode;		
}
```

#### Traversal

 Traversal involves visiting each node in the linked list and performing some operation on the data. A simple traversal function would print or process the data of each node.

- ALgorithm

```
1.start
2.Initialize a pointer current to the head of the list.
3.Using while loop iterate through the list until the current pointer reaches NULL.
4.print the data of the current node
5.move the current pointer to the next node.
6.stop
```
``` C
void traverseLinkedlist(Node* head)
{
	Node* current=head;
	while(current!=NULL)
	{
		printf("%d->",current->head);
		current=current->next;
	}
	printf("NULL");
}
```
#### Searching

Searching in a Singly Linked List refers to the process of looking for a specific element or value within the elements of the linked list.

- Algorithm
```
1.start
2.Traverse the Linked List starting from the head.
3.Check if the current node's data matches the target value.
4.If a match is found, return true.
5.Otherwise, Move to the next node and repeat steps 2.
6.If the end of the list is reached without finding a match, return false.
7.stop
```

```C
bool searchlinkedlist(Node* head,int target)
{
	while(head!=NULL)
	{
		if(head->data==target)
		{
			return true;
		}
		head=head->next;
	}
	return false;
}
```

#### Length

Finding Length in Singly Linked List refers to the process of determining the total number of nodes in a singly linked list.

- Algorithm
```
1.start
2.Initialize a counter length to 0.
3.Start from the head of the list, assign it to current.
4.Traverse the list:
  Increment length for each node.
  Move to the next node (current = current->next).
5.Return the final value of length.
6.stop
```

``` C
int findlength(Node* head)
{
	int len=0;
	
	Node* current=head;
	while(current!=NULL)
	{
		len++;
		current=current->next;
	}
	return len;
}
```

#### Insertion

Insertion is a fundamental operation in linked lists that involves adding a new node to the list. There are several scenarios for insertion:
 
##### At beginning

![image](https://github.com/user-attachments/assets/d4568b39-8d6c-40ec-a2f2-2d71b2305fdd)

- Algorithm
```
1.start
2.Create a new node with the given value.
3.Set the next pointer of the new node to the current head.
4.Move the head to point to the new node.
5.Return the new head of the linked list.
6.stop
```

``` C
Node* insertatbeginning(Node* head,int value)
{
	Node* node1=newNode(value);
	node1->next=head;
	head=node1;
	return head;
}
```

##### At End

![image](https://github.com/user-attachments/assets/f8f0627c-3d0d-4ccf-bc0f-65cf6b6e6ff4)

- Algorithm
```
1.start
2.Create a new node with the given value.
3.Check if the list is empty:
4.If it is, make the new node the head and return.
5.Traverse the list until the last node is reached.
6.Link the new node to the current last node by setting the last node's next pointer to the new node.
7.stop.
```

```C
Node* insertatend(Node* head,int value)
{
	Node* node1=newNode(value);
	if(head==NULL)
	{
		return node1;	
	}
	Node* current=head;
	while(current->data!=NULL)
	{
		current=current->next;
	}
	current->next=node1;
	return head;
}
```

##### At Position

To insert a node at a specific position, traverse the list to the desired position, link the new node to the next node, and update the links accordingly.

![image](https://github.com/user-attachments/assets/26627022-36e5-4006-a601-d5b6511b3c79)

- Algorithm
```

```

```C

```
### Types
