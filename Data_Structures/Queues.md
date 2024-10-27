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

```
