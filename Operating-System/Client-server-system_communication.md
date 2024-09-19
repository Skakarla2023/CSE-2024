# Communication in Client-Server System

Communication in client server system refers to exchange of data and services among multiple machines or processes.
In client-server system, the process that requests for a servce acts as a client and the process that provides the data serves as the server. 
In CSS, we can use different ways;
* Sockets Mechanism.
* Remote Procedure call
* Pipes

#### Sockets:
Sockets are the end points of communication between 2 machines. They provide a way for processes to communicate with each other,either on the same machine or over through internet also possible.
sockets enable the communication between server and client to transfer data in a bidirectional way.
They are used in a client/server framework and consist of the IP address and port number.
 
![image](https://github.com/user-attachments/assets/fc4d7761-a79e-4209-a3d4-415e23a834fc)

#### Remote Procedure Calls
These are interprocess communication techniques that are used for client-server based applications. A remote procedure call is also known as a subroutine call or a function call.
A client has a request that the RPC translates and sends to the server. This request may be a procedure or a function call to a remote server. When the server receives the request, it sends the required response back to the client.

![image](https://github.com/user-attachments/assets/cbaba678-712e-4c48-9831-b43f30ed92d6)

#### Pipes
These are IPC that contains 2 ends. Data is entered at one end and is retrieved at the other end. There are 2 types of pipes, named and ordinary.
Ordinary pipe allow only one way communication. Named pipes allow 2 way communication. 
Ordinary pipes have a parent child communication, that they can be accessed by the processes that created or inherited them.
Named pipes are more powerful than ordinary pipes, they exist even after the process using them has been terminated.They need to be explicitly deleted when no longer required.

![image](https://github.com/user-attachments/assets/9168e9da-8bde-4e41-9826-73bce92128fd)

