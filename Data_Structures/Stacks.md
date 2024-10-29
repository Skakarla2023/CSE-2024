# Stacks

-  Stack is a Data Structure that can hold many elements.
- Stack is a linear data structure that follows a particular order in which operations are performed.
- Stacks follow LIFO-“Last in First Out”, i.e., the element that is inserted at last will be removed first.


![image](https://github.com/user-attachments/assets/af74648a-2fb7-46c0-912e-8b3a389c4def)




  Basic Operations we do on stack are-

| Operation    | Definition                         |
|--------------|------------------------------------|
|push()        |Adds an element to the stack        |
|pop()         |Removes element from stack          |
|peek()        |returns the top element of the stack|
|isEmpty()     |checks if the stack is empty        |
|size()        |counts the no.of elements in stack  |



The following python code shows operations that can be done on stacks.

``` Python

stack=[]
stack.append('A')
stack.append('B')
stack.append('C')

print("Stack: ",stack)

element=stack.pop()
print("Pop: ",element)

topelement=stack[-1]
print("Peek: ",topelement)

isEmpty=not bool(stack)
print("isEmpty: ",isEmpty)

print("Size: ",len(stack))
```

Stack implementation is often done using LinkedLists,
due to their dynamic size,extra memory and readability.

- The following C code shows basic operations that can be done on stack:

``` C
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
		top=top+1;
		top=arr[x];
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
		top=top-1;
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
		for(i=0;i<top;i++)
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

#### Splving Infix to Postfix using Stacks in C

``` C
#include<stdio.h>
#include<ctype.h>
char stack[20];
int top=-1;

void push(char x)
{
	stack[top++]=x;
}
char pop()
{
	if(top==-1)
		return -1;
	else
		return stack[top--];
}
int priority(char x)
{
	if(x==')')
		return 0;
	if(x=='+'||x=='-')
		return 1;
	if(x=='*'||x=='/')
		return 2;
}
int main()
{
	char exp[20];
	char *e,x;
	printf("Enter the expression: ");
	scanf("%s",&exp);
	e=exp;
	while(*e!='\0')
	{
		if(isalnum(*e))
		{
			printf("%c",*e);
		}
		else if(*e=='(')
		{
			push(*e);
		}
		else if(*e==')')
		{
			while((x=pop())!='(')
				printf("%c",x);
		}
		else
		{
			while(priority(stack[top])>=priority(*e))
				printf("%c",pop());
			push(*e);
		}
		e++;
	}
	while(top!=-1)
	{
		printf("%c",pop());
	}
}
```

Output:

![image](https://github.com/user-attachments/assets/8172f18a-9d95-4128-95cc-3d1f6a7c6efd)
