# Queues

-  Queue is a Data Structure that can hold many elements.
-  It follow FIFO.
-  Think of queue as people standing in line in a supermarket.


![image](https://github.com/user-attachments/assets/e5f34df4-d8d2-4c60-894d-27dec8c4e7c5)

Basic operations we can do on queue:

|Operations      | Meaning                                 |
|----------------|-----------------------------------------|
|Enqueue         |adds a new element to the queue.         |
|dequeue         |removes an element from the queue.       |
|peek            |returns the first element in the queue.  |
|isEmpty         |checks if the queue is empty             |
|size            |find the number of elements in the queue.|


![image](https://github.com/user-attachments/assets/1808a909-f0ff-4521-9e29-eb78689ac382)


The following python code shows operations on queues.

``` Python

queue = []

# Enqueue
queue.append('A')
queue.append('B')
queue.append('C')
print("Queue: ", queue)

# Dequeue
element = queue.pop(0)
print("Dequeue: ", element)

# Peek
frontElement = queue[0]
print("Peek: ", frontElement)

# isEmpty
isEmpty = not bool(queue)
print("isEmpty: ", isEmpty)

# Size
print("Size: ", len(queue))

```

Output:
```
Queue:  ['A', 'B', 'C']
Dequeue:  A
Peek:  B
isEmpty:  False
Size:  2
```
The following C code shows operations on queue:

``` C
#include<stdio.h>
#include<stdlib.h>
#define SIZE 4

void enqueue();
void dequeue();
void show();
int arr[SIZE];
int rear=-1;
int front=-1;

int main()
{
	int ch;
	while(1)
	{
		printf("*****Operations on Queue*****");
		printf("\nSelect one from below:");
		printf("\n1.Enqueue operation\n2.Dequeue operation\n3.Display the queue\n4.Exit\n");
		printf("Enter your choiceof operations:");
		scanf("%d",&ch);
		switch(ch)
		{
			case 1:
				enqueue();
				break;
			case 2:
				dequeue();
				break;
			case 3:
				show();
				break;
			case 4:
				exit(0);
			default:
				printf("\nInvalid choice\n");
		}
	}
}

void enqueue()
{
	int ins_item;
	if(rear==SIZE-1)
		printf("Overflow\n");
	else
	{
		if(front==-1)
	
		front=0;
		printf("Enter element to be inserted:");
		scanf("%d",&ins_item);
		rear=rear+1;
		arr[rear]=ins_item;		
	}
}

void dequeue()
{
	if(front==-1||front>rear)
	{
		printf("\nUnderflow");
		return;
	}
	else
	{
		printf("Element deleted from the queue:%d\n",arr[front]);
		front=front+1;
	}
}

void show()
{
	int s;
	if(front==-1)
	{
		printf("Empty queue\n");
	}
	else
	{
		printf("Queue:\n");
		for(s=front;s<=SIZE;s++)
		{
			printf("%d\n",arr[s]);
		}
	}
}
```

Output:

![image](https://github.com/user-attachments/assets/9c205e9d-3215-4bd1-a5ef-0d1fa20b8821)



