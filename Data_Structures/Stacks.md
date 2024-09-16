# Stacks

-  Stack is a Data Structure that can hold many elements.
-  It follows LIFO.
-  Basic Operations we do on stack are-
#### Push:
- Adds a new element to the stack.
#### Pop:
- Removes an element from the stack.
#### Peek:
- returns the top element of the stack.
#### isEmpty:
- returns true if the stack is empty and false if not
#### size:
- finds the number of elements in the stack.

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
The following Java code shows implementation of stack using LinkedList

```Java

public class Main {
    public static void main(String[] args) {
        Stack myStack = new Stack();
        
        myStack.push('A');
        myStack.push('B');
        myStack.push('C');

        System.out.println("Pop: " + myStack.pop());
        System.out.println("Peek: " + myStack.peek());
        System.out.println("isEmpty: " + myStack.isEmpty());
        System.out.println("Size: " + myStack.size());
    }
}

class Node {
    char value;
    Node next;
    Node(char value) {
        this.value = value;
        this.next = null;
    }
}

class Stack {
    private Node head;
    private int size;

    public Stack() {
        this.head = null;
        this.size = 0;
    }

    public void push(char value) {
        Node newNode = new Node(value);
        if (head != null) {
            newNode.next = head;
        }
        head = newNode;
        size++;
    }

    public char pop() {
        if (isEmpty()) {
            return ' ';
        }
        char popped = head.value;
        head = head.next;
        size--;
        return popped;
    }

    public char peek() {
        if (isEmpty()) {
            return ' ';
        }
        return head.value;
    }

    public boolean isEmpty() {
        return size == 0;
    }

    public int size() {
        return size;
    }
}


```
