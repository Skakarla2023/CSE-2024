# STACK & QUEUE


### Stacks-
A stack is a fundamental data structure in computer science, which operates on a Last In, First Out (LIFO) principle. This means that the last element added to the stack will be the first one to be removed. Think of it like a stack of plates: you can only take the top plate off, and you can only add a new plate on top

Basic Operations:

- Push: Add an element to the top of the stack.
  
- Pop: Remove the top element from the stack.
  
- Peek/Top: Retrieve the top element without removing it.
  
- isEmpty: Check if the stack is empty.
  
- isFull: (if using a fixed-size stack) Check if the stack is full.

A simple C program demonstrating operation on stack

```C
#include<stdio.h>
#include<stdlib.h>
#define SIZE 5

int top=-1,arr[SIZE];
void push();
void pop();
void show();
int isEmpty();
int isFull();

int main()
{
	int choice;
	
	while(1)
	{
		printf("****Operations on Stack*****\n");
		printf("\n1.Push element\n2.Pop element\n3.Show\n4.isEmpty\n5.isFull\n6.Exit\n");
		printf("Enter the choice:\n");
		scanf("%d",&choice);
		switch(choice)
		{
			case 1:
				push();
				break;
			case 2:
				pop();
				break;
			case 3:
				show();
				break;
			case 4:
				isEmpty();
				break;
			case 5:
				isFull();
				break;
			case 6:
				exit(0);
			default:
				printf("\nInvalid choice\n");
		}
	}
	return 0;
}

void push()
{
	int x;
	if(top==SIZE-1)
	{
		printf("Stack Overflow");
	}
	else
	{
		printf("Enter the element");
		scanf("%d",&x);
		arr[++top]=x;
	}
}

void pop()
{
	if(top==-1)
	{
		printf("Stack underflow");
	}
	else
	{
		printf("popped element: ",arr[top]);
		top--;
	}
}

void show()
{
	int i;
	if(top==-1)
	{
		printf("Stack underflow");
	}
	else
	{
		printf("\nElements inside the stack:");
		for(i=top;i>=0;i--)
		{
			printf("%d\n",arr[i]);
		}
	}
}

int isEmpty()
{
	if(top==-1)
	{
		printf("true\n");
	}
	else
	{
		printf("False\n");
	}
}

int isFull()
{
	if(top==-1)
	{
		printf("false\n");
	}
	else
	{
		printf("true\n");
	}
}
```

Output-
```
****Operations on Stack*****

1.Push element
2.Pop element
3.Show
4.isEmpty
5.isFull
6.Exit
Enter the choice:
1
Enter the element1
****Operations on Stack*****

1.Push element
2.Pop element
3.Show
4.isEmpty
5.isFull
6.Exit
Enter the choice:
1
Enter the element2
****Operations on Stack*****

1.Push element
2.Pop element
3.Show
4.isEmpty
5.isFull
6.Exit
Enter the choice:
1
Enter the element3
****Operations on Stack*****

1.Push element
2.Pop element
3.Show
4.isEmpty
5.isFull
6.Exit
Enter the choice:
3

Elements inside the stack:3
2
1
****Operations on Stack*****

1.Push element
2.Pop element
3.Show
4.isEmpty
5.isFull
6.Exit
Enter the choice:
4
False
****Operations on Stack*****

1.Push element
2.Pop element
3.Show
4.isEmpty
5.isFull
6.Exit
Enter the choice:
5
true
****Operations on Stack*****

1.Push element
2.Pop element
3.Show
4.isEmpty
5.isFull
6.Exit
Enter the choice:
6
```

### Application of stack

#### Infix to Postfix conversion

Here is a simple C program demonstrating Infix to Postfix conversion

``` C
#include<stdio.h>
#include<string.h>
#include<ctype.h>

int get(char s)
{
	if(s=='^')
	{
		return 3;
	}
	if(s=='*'||s=='/')
	{
		return 2;
	}
	if(s=='+'||s=='-')
	{
		return 1;
	}
	return -1;
}

int main()
{
	char exp[]="(a+(b^c))-d/e";
	int len=strlen(exp);
	char ans[len+1];
	char stack[len];
	int ind1=0,ind2=0;
	int y;
	for(y=0;y<len;y++)
	{
		char d=exp[y];
		if('a'<=d&&d<='z')
		{
			ans[ind1++]=d;
		}
		else if(d=='(')
		{
			stack[ind2++]=d;
		}
		else if(d==')')
		{
			while(ind2>0&&stack[ind2-1]!='(')
			{
				ans[ind1++]=stack[--ind2];
			}
			if(ind2>0) ind2--;
		}
		else
		{
			while(ind2>0&&get(stack[ind2-1])>get(d))
			{
				ans[ind1++]=stack[--ind2];
			}
			stack[ind2++]=d;
		}
	}
	
	while(ind2>0)
	{
		ans[ind1++]=stack[--ind2];
	}
	ans[ind1]='\0';
	printf("Answer: %s",ans);
}
```

Output:

```
Answer: abc^+de/-
```

#### Infix to Prefix conversion

here is a simple C code demonstrating conversion of infix to prefix-

```C
#include <stdio.h>
#include <string.h>
#include <ctype.h>
int getPrecedence(char s)
{
    if(s == '^')
    {
        return 3;
    }
    if(s == '*' || s == '/')
    {
        return 2;
    }
    if(s == '+' || s == '-')
    {
        return 1;
    }
    return -1;
}
void reverse(char *str)
{
    int n = strlen(str);
	int i; 
    for (i = 0; i < n / 2; i++)
    {
        char temp = str[i];
        str[i] = str[n - i - 1];
        str[n - i - 1] = temp;
    }
}

int main()
{
    char exp[] = "(a+(b^c))-d/e";
    reverse(exp);
    int len = strlen(exp);
    char ans[len + 1];
    char stack[len];
    int ind1 = 0, ind2 = 0;
    int y;
    for ( y = 0; y < len; y++)
    {
        char d = exp[y];
        if (isalpha(d))
        {
            ans[ind1++] = d;
        }
        else if (d == ')')
        {
            stack[ind2++] = d;
        }
        else if (d == '(')
        {
            while (ind2 > 0 && stack[ind2 - 1] != ')')
            {
                ans[ind1++] = stack[--ind2];
            }
            if (ind2 > 0) ind2--;
        }
        else
        {
            while (ind2 > 0 && getPrecedence(stack[ind2 - 1]) >= getPrecedence(d))
            {
                ans[ind1++] = stack[--ind2];
            }
            stack[ind2++] = d;
        }
    }
    
    while (ind2 > 0)
    {
        ans[ind1++] = stack[--ind2];
    }
    ans[ind1] = '\0';
    reverse(ans);
    printf("Answer: %s", ans);
    
    return 0;
}
```

Output:

```
Answer: -+a^bc/de
```

#### Evaluation of Prefix expression

![image](https://github.com/user-attachments/assets/e8fa0983-99a4-4212-850e-55f33791e2db)

#### Evaluation of prefix expression

![image](https://github.com/user-attachments/assets/21ee74ec-b9e7-489f-a3c8-2af68ba44997)

![image](https://github.com/user-attachments/assets/9ce7a9ee-8fa8-476e-958a-d623400eae42)

#### Towers of Hanoii

![image](https://github.com/user-attachments/assets/239a1eb9-a575-4e54-ac11-b376a959de84)


### Queues

A queue is a fundamental data structure in computer science that operates on a First In, First Out (FIFO) principle. This means that the first element added to the queue will be the first one to be removed, similar to a line of people waiting for a service where the person at the front gets served first.

Basic Operations:

- Enqueue: Add an element to the end of the queue.

- Dequeue: Remove an element from the front of the queue.

- Front (or Peek): Retrieve the front element without removing it.

- isEmpty: Check if the queue is empty.

- isFull: (if using a fixed-size queue) Check if the queue is full.

A simple C program demonstrating operation on queue-

``` C
#include <stdio.h>
#include <stdlib.h>
#define SIZE 5  // Define the size of the queue

int front = -1, rear = -1, queue[SIZE];

void enqueue();
void dequeue();
void show();
int isEmpty();
int isFull();

int main()
{
    int choice;

    while (1)
    {
        printf("****Operations on Queue*****\n");
        printf("\n1.Enqueue element\n2.Dequeue element\n3.Show\n4.isEmpty\n5.isFull\n6.Exit\n");
        printf("Enter the choice:\n");
        scanf("%d", &choice);
        switch (choice)
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
                printf(isEmpty() ? "Queue is empty\n" : "Queue is not empty\n");
                break;
            case 5:
                printf(isFull() ? "Queue is full\n" : "Queue is not full\n");
                break;
            case 6:
                exit(0);
            default:
                printf("\nInvalid choice\n");
        }
    }
    return 0;
}

void enqueue()
{
    int x;
    if (isFull())
    {
        printf("Queue Overflow\n");
    }
    else
    {
        printf("Enter the element: ");
        scanf("%d", &x);
        if (isEmpty())
        {
            front = rear = 0;
        }
        else
        {
            rear++;
        }
        queue[rear] = x;
    }
}

void dequeue()
{
    if (isEmpty())
    {
        printf("Queue Underflow\n");
    }
    else
    {
        printf("Dequeued element: %d\n", queue[front]);
        if (front == rear)
        {
            front = rear = -1;  // Queue becomes empty
        }
        else
        {
            front++;
        }
    }
}

void show()
{
    if (isEmpty())
    {
        printf("Queue is empty\n");
    }
    else
    {
        printf("Queue elements are: ");
        for (int i = front; i <= rear; i++)
        {
            printf("%d ", queue[i]);
        }
        printf("\n");
    }
}

int isEmpty()
{
    return front == -1;
}

int isFull()
{
    return rear == SIZE - 1;
}
```

Output-

```
****Operations on Queue*****

1.Enqueue element
2.Dequeue element
3.Show
4.isEmpty
5.isFull
6.Exit
Enter the choice:
1
Enter the element: 1
****Operations on Queue*****

1.Enqueue element
2.Dequeue element
3.Show
4.isEmpty
5.isFull
6.Exit
Enter the choice:

1
Enter the element: 2
****Operations on Queue*****

1.Enqueue element
2.Dequeue element
3.Show
4.isEmpty
5.isFull
6.Exit
Enter the choice:
1
Enter the element: 3
****Operations on Queue*****

1.Enqueue element
2.Dequeue element
3.Show
4.isEmpty
5.isFull
6.Exit
Enter the choice:
3
Queue elements are: 1 2 3
****Operations on Queue*****

1.Enqueue element
2.Dequeue element
3.Show
4.isEmpty
5.isFull
6.Exit
Enter the choice:
4
Queue is not empty
****Operations on Queue*****

1.Enqueue element
2.Dequeue element
3.Show
4.isEmpty
5.isFull
6.Exit
Enter the choice:
5
Queue is not full
****Operations on Queue*****

1.Enqueue element
2.Dequeue element
3.Show
4.isEmpty
5.isFull
6.Exit
Enter the choice:
2
Dequeued element: 1
****Operations on Queue*****

1.Enqueue element
2.Dequeue element
3.Show
4.isEmpty
5.isFull
6.Exit
Enter the choice:
6
```

#### Circular queue

A circular queue is a type of data structure that overcomes the limitations of a regular linear queue by connecting the end of the queue back to the front, forming a circle. This ensures efficient use of space and avoids the problem of the queue being full despite having empty slots due to dequeuing.

- Key Characteristics of Circular Queue:

```
Circular Nature: The last position in the queue is connected to the first position, forming a circular structure.

Efficient Space Utilization: Allows reusing the vacated spaces at the beginning of the queue, preventing the need for shifting elements.

Fixed Size: The queue has a fixed maximum size, which is defined at the time of creation.
```

Basic Operations:

- Enqueue (Adding an element): Adds an element to the rear of the queue.
- Dequeue (Removing an element): Removes an element from the front of the queue.
- Front/Peek: Retrieves the front element without removing it.
- isEmpty: Checks if the queue is empty.
- isFull: Checks if the queue is full.

Benefits:
```
Efficient Space Utilization: Reuses vacated spaces, preventing overflow when there is still space available.
No Shifting Required: Unlike linear queues, there’s no need to shift elements after dequeuing.
Fixed and Predictable: The size is fixed, making it easy to manage and predict memory usage.
Circular queues are widely used in various applications like buffering data streams, round-robin scheduling, and managing resources in operating systems.
```

![image](https://github.com/user-attachments/assets/9248e5af-08b4-4602-aa93-bfe5f2462ea9)
