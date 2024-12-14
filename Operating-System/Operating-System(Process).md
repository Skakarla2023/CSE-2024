# Process

## Process States

## Process Control Block

While creating a process, the operating system performs several operations. To identify the processes, it assigns a process identification number (PID) to each process. As the operating system supports multi-programming, it needs to keep track of all the processes. For this task, the process control block (PCB) is used to track the process’s execution status. Each block of memory contains information about the process state, program counter, stack pointer, status of opened files, scheduling algorithms, etc.

![image](https://github.com/user-attachments/assets/8511c3fd-52b2-4e3b-be89-dbb8d0a51b87)

```
Pointer: It is a stack pointer that needs to be changed when a process is shifted from one state to another.

Process state:It stores the respective state of the process.

Program counter:It stores the instruction that is to be next executed by the process.

Process number:Each process is identified with a unique identification number known as process ID.

Memory limit: This field contains the information of memory management system used by the Operating System.

List of opened files: This field contains information of list of all files opened while a process is being executed.
```
## Process Scheduling

One of the most important areas of scheduling is which programs will work on the CPU. This task is handled by the Operating System (OS) of the computer and there are many different ways in which we can choose to configure programs.

Process schedulers are fundamental components of operating systems responsible for deciding the order in which processes are executed by the CPU. In simpler terms, they manage how the CPU allocates its time among multiple tasks or processes

#### Categories of Scheduling
Scheduling falls into one of two categories:

1. Non-Preemptive: In this case, a process’s resource cannot be taken before the process has finished running. When a running process finishes and transitions to a waiting state, resources are switched.
2. Preemptive: In this case, the OS assigns resources to a process for a predetermined period. The process switches from running state to ready state or from waiting state to ready state during resource allocation. This switching happens because the CPU may give other processes priority and substitute the currently active process for the higher priority process.

### Process Schedulers
There are three types of Process schedulers
1. Long-term or Job Schedulers:

this brings a process to the ready queue. It maintains the degree i.e., number of processes present in the ready queue at any pont of time.
It has to make careful selection among I/O bound processes and CPU Bound processes.

2. short term or CPU schedulers:

It is responsible for selecting one process from the ready state for scheduling it on the running state. Note: Short-term scheduler only selects the process to schedule it doesn’t load the process on running.  Here is when all the scheduling algorithms are used. The CPU scheduler is responsible for ensuring no starvation due to high burst time processes.

![image](https://github.com/user-attachments/assets/e443057a-7c57-4617-8f75-1f73717f3719)

3. Medium Term Schedulers:

It is responsible for suspending and resuming the process. It mainly does swapping (moving processes from main memory to disk and vice versa). Swapping may be necessary to improve the process mix or because a change in memory requirements has overcommitted available memory, requiring memory to be freed up.

![image](https://github.com/user-attachments/assets/03e8659e-cd92-40f5-8cbd-b56572c3c47b)

#### Context Switching:
Context switching refers to switching of CPU between 2 processes. More likely, saving the state of old process in PCB and loads new process for running.
