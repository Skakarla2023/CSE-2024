# Queues

-  Queue is a Data Structure that can hold many elements.
-  It follow FIFO.
-  Think of queue as people standing in line in a supermarket.


![image](https://github.com/user-attachments/assets/e5f34df4-d8d2-4c60-894d-27dec8c4e7c5)





Basic operations we can do on queue:
#### Enqueue:
- adds a new element to the queue.
#### Dequeue:
-  removes and returns the first element from the queue.
#### Peek:
-  returns the first element in the queue.
#### isEmpty:
-  checks if the queue is empty.
#### size:
- find the number of elements in the queue.


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


### Queues implementation using LinkedLists

The following java code shows queues implementation using LinkedLists

``` Java

public class Main {
    public static void main(String[] args) {
        Queue myQueue = new Queue();
        
        myQueue.enqueue('A');
        myQueue.enqueue('B');
        myQueue.enqueue('C');
        System.out.print("Queue: ");
        myQueue.printQueue();
        
        System.out.println("Dequeue: " + myQueue.dequeue());
        System.out.println("Peek: " + myQueue.peek());
        System.out.println("isEmpty: " + myQueue.isEmpty());
        System.out.println("Size: " + myQueue.size());
    }
}

class Node {
    char data;
    Node next;
    
    public Node(char data) {
        this.data = data;
        this.next = null;
    }
}

class Queue {
    Node front;
    Node rear;
    int length;
    
    public Queue() {
        this.front = null;
        this.rear = null;
        this.length = 0;
    }
    
    public void enqueue(char element) {
        Node newNode = new Node(element);
        if (this.rear == null) {
            this.front = this.rear = newNode;
            length++;
            return;
        }
        this.rear.next = newNode;
        this.rear = newNode;
        length++;
    }
    
    public char dequeue() {
        if (isEmpty()) {
            System.out.println("Queue is empty");
            return ' ';
        }
        Node temp = this.front;
        this.front = temp.next;
        if (this.front == null) {
            this.rear = null;
        }
        length--;
        return temp.data;
    }
    
    public char peek() {
        if (isEmpty()) {
            System.out.println("Queue is empty");
            return ' ';
        }
        return this.front.data;
    }
    
    public boolean isEmpty() {
        return length == 0;
    }
    
    public int size() {
        return length;
    }
    
    public void printQueue() {
        Node temp = this.front;
        while (temp != null) {
            System.out.print(temp.data + " ");
            temp = temp.next;
        }
        System.out.println();
    }
}

```

