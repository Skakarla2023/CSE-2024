# Threads in OS


Threads in Operating System are referred to as light weight processes.

Each thread belongs to exactly one process. 

### MultiThreading Models
It is a process by which multiple threads are executed at the same time.
Multithreading allows the application to divide its task into individual threads. In multi-threads, the same process or task can be done by the number of threads, or we can say that there is more than one thread to perform the task in multithreading. With the use of multithreading, multitasking can be achieved.

The main drawback of single threading system is that only one process can be executed at a time,to overcome this ,multithreading was found which helps in multitasking i.e., running mutliple threads at a time.
It allows multiple tasks to be performed.

  ![image](https://github.com/user-attachments/assets/3f916c09-fbd8-4587-971b-d40d821e50f6)

In the above example client1,client2 and client3 are accessing the same server without any waiting,several tasks can be performed in the same time.

In Operating System threads are divided into user-level Threads and kernel-level threads.

### User Level Threads

The OS does not directly support threads,they're managed by a user-level thread library, which is part of the application. It manages the threads and schedules them on available processors. The advantages of user-level threads include *greater flexibility and portability*, as the application has more control over thread management. However, the disadvantage is that user-level threads are not as efficient as kernel-level threads, as they rely on the application to *manage thread scheduling*.

### Kernel Level Threads

In this ,the OS directly supports threads as part of the kernel. Each thread is a separate entity that can be scheduled and executed independently by the operating system. The advantages of kernel-level threads include *better performance and scalability*, as the operating system can schedule threads more efficiently. However, the disadvantage is that kernel-level threads are *less flexible* and *portable* than user-level threads, as they are *managed by the operating system*.

```
User-level:

Advantages:Greater flexibilty and portability,manage thread scheduling
Disadvantages:Not as efficient as kernel level threads

Kernel-level:

Advantages:Better performance and scalability
Disadvantages: Less flexible & Portable,thread scheduling managed by the OS
```
#### Hybrid models:

- Advantages:
Combines advantages of both models,
More scalable.

- Disadvantages:
  More complex,use more resources as they use both thread library and kernel support.

Many OS support user-level threads and kernel-level threads in a combined way, one such example is *Solaris*.

Multithreading models are of three types-
- Many to Many
- One to One
- Many to One
