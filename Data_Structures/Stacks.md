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
