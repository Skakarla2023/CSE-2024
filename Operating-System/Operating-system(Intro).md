# Operating system

- An Operating system is an interface between computer hardware and the user.
- An Operating system is a software which performs all the basic operations relaated to computer such as file management,disk management, memory management, handling input and output, and also handling peripheral devices like drives and disks etc.
- An Operating system is a software that allows applications to interact with the computer hardware.
- The Software that contains all the core components of an Operating system is called the 'kernel'.
- The function of an operating system is to provide the user an environment in which he can run applications effectively.

## Functionalities of an OS

#### Device Management:  
The Operating systems takes care of the number of devices present in the computer.I t can also be referred to as input/output controller as it decides which process or user gets the device and for how much time.
#### File Management:
It keeps track of number of files in the computer and also certain operations performed on files such as creation,deletion and modification.
#### Job Accounting:
It keeps track of number resources and processes that are used by various jobs and user.
#### Error-Detecting Aids:
It provides several methods such as generating error messages,traces and dumps for detecting errors.
#### Security:
It prevents unauthorised access to data and resources present in the conputer by providing passwords or some other protection methods.
#### Control over System Performance:
It records the time between request for a service by a user and the allocation by the syetm.

## Functions/ Services provided by OS

### Memory Management:
1. The Operating system manages the primary memory i.e., the main memory in the computer.
2. For a process to be executed it must be first loaded in the main memory.
3. The Main memory is made of largearray of bytes or words where each word has certain memory addresses.
4. The OS keeps track of the memory allocated to each process and for how long is the memory allocated to a process.
5. It also ensures that the memory allocated to one process is not used by other processes.
6. It allocates the memory to a process when a process requests for it and deallocates when the process is terminated.
7. It also decides the order in which memory is allocated for different processes.

### Process Management:
1. In multiprogramming environment, an OS decides the allocation of a processor to a process and fow how much processing time each process has.
2. This mechanism of OS is called Process Scheduling.
3. It ensures that each process gets enough time from the processor to function properly.
4. It keeps track of the status of the process.
5. The one that does this job is called Traffic controller.
6. It allocates the processor to a process and deallocates when it is no longer required.

### File Management:
1. A file system is organized into directories for efficient or easy navigation and usage.
2. These directories may contain other directories and other files.
3. An Operating System carries out the following file management activities.
4. It keeps track of where information is stored, user access settings, the status of every file, and more.
5. These facilities are collectively known as the file system.
6. An OS keeps track of information regarding the creation, deletion, transfer, copy, and storage of files in an organized way.

## Types of Operating systems

### Batch Operating System
This type of operating system does not interact with the computer directly. There is an operator which takes similar jobs having the same requirements and groups them into batches. It is the responsibility of the operator to sort jobs with similar needs. Batch Operating System is designed to manage and execute a large number of jobs efficiently by processing them in groups.

![image](https://github.com/user-attachments/assets/b5efc5f8-b4e1-4552-a64d-d1eea7f9a110)

### Multi-Programming Operating System
Multiprogramming Operating Systems can be simply illustrated as more than one program is present in the main memory and any one of them can be kept in execution. This is basically used for better utilization of resources.

![image](https://github.com/user-attachments/assets/14b7fdc0-0949-4c6e-b026-f0d3062850b7)

### Multi-Processing Operating System
Multi-Processing Operating System is a type of Operating System in which more than one CPU is used for the execution of resources. It betters the throughput of the System

![image](https://github.com/user-attachments/assets/0fca25eb-9396-47af-8e4e-dc9b53a89941)

### Multi-Tasking Operating System
Multitasking Operating System is simply a multiprogramming Operating System with having facility of a Round-Robin Scheduling Algorithm. It can run multiple programs simultaneously.

There are two types of Multi-Tasking Systems which are listed below.

Preemptive Multi-Tasking
Cooperative Multi-Tasking

![image](https://github.com/user-attachments/assets/3dc83f16-61b6-4f94-8e08-bdf0f0b360e3)

### Time-Sharing Operating Systems
Each task is given some time to execute so that all the tasks work smoothly. Each user gets the time of the CPU as they use a single system. These systems are also known as Multitasking Systems. The task can be from a single user or different users also. The time that each task gets to execute is called quantum. After this time interval is over OS switches over to the next task.

![image](https://github.com/user-attachments/assets/1a5932a6-98b9-471a-a500-194764607a80)

### Distributed Operating Systems
Distributed operating systems are a recent advancement in computer technology, gaining rapid global acceptance. These systems consist of autonomous, interconnected computers that communicate via a shared network, each with its own memory unit and CPU. Known as loosely coupled systems, they vary in processor size and function. A key benefit is remote access, allowing users to access files or software from other systems within the network.

![image](https://github.com/user-attachments/assets/7cdc6c7b-f186-4294-befb-e4f78bff7795)

### Network Operating Systems
These systems run on a server and provide the capability to manage data, users, groups, security, applications, and other networking functions. These types of operating systems allow shared access to files, printers, security, applications, and other networking functions over a small private network. One more important aspect of Network Operating Systems is that all the users are well aware of the underlying configuration, of all other users within the network, their individual connections, etc. and that’s why these computers are popularly known as tightly coupled systems .

![image](https://github.com/user-attachments/assets/94111176-ce19-4209-bed2-5c43528a510a)

## OS Structures
The operating system can be implemented with the help of various structures. The structure of the OS depends mainly on how the various standard components of the operating system are interconnected and merge into the kernel. 
A system structure for an operating system is like the blueprint of how an OS is organized and how its different parts interact with each other.Because operating systems have complex structures, we want a structure that is easy to understand so that we can adapt an operating system to meet our specific needs. Similar to how we break down larger problems into smaller, more manageable subproblems, building an operating system in pieces is simpler.
### Types of Operating Systems Structures

#### Simple Structure:

Simple structure os do not have well defined structure, they are simple,small and limited.
The interfaces and layers of functionalities in this structure are not well seperated.
These type of OS structures cause the entire system to fail if any of the user program fails.
MS-DOS OS is an example of Simple OS.

![image](https://github.com/user-attachments/assets/8dc956c7-c12e-481e-b36c-f0060679840f)

#### Micro-kernel Structure:

Micro-Kernel structure designs the operating system by removing all non-essential components from the kernel and implementing them as system and user programs. This results in a smaller kernel called the micro-kernel. Advantages of this structure are that all new services need to be added to user space and does not require the kernel to be modified. 
Mac OS is an example of this type of OS.

![image](https://github.com/user-attachments/assets/1e0e64ae-cb62-4c90-a6a3-60ca07dac5c4)

#### layered Structure

An OS can be broken into pieces and retain much more control over the system. In this structure, the OS is broken into a number of layers (levels). The bottom layer (layer 0) is the hardware, and the topmost layer (layer N) is the user interface. These layers are so designed that each layer uses the functions of the lower-level layers. This simplifies the debugging process, if lower-level layers are debugged and an error occurs during debugging, then the error must be on that layer only, as the lower-level layers have already been debugged.

![image](https://github.com/user-attachments/assets/0977a5c0-2c83-455b-8b30-0972c8f6bd4b)

#### Modular Structure

It is considered as the best approach for an OS. It involves designing of a modular kernel. The kernel has only a set of core components and other services are added as dynamically loadable modules to the kernel either during runtime or boot time. It resembles layered structure due to the fact that each kernel has defined and protected interfaces, but it is more flexible than a layered structure as a module can call any other module. 

![image](https://github.com/user-attachments/assets/09302e27-dec5-4258-ba50-d98fc730d5f0)

#### Hybrid-Kernel Structure

Hybrid-Kernel structure is nothing but just a combination of both monolithic-kernel structure and micro-kernel structure. Basically, it combines properties of both monolithic and micro-kernel and make a more advance and helpful approach. It implement speed and design of monolithic and modularity and stability of micro-kernel structure.

![image](https://github.com/user-attachments/assets/169ed20d-77d8-4d65-8caa-714bc58f83bb)


## System Calls
System calls are interfaces provisioned by the operating system to allow user-level applications to interact with low-level hardware components & make use of all the services provided by the kernel, which is a core component and the heart of an operating system that manages all the hardware and the services provided by the OS.

These system calls are essential for every process to interact with the kernel and properly use the services provided by it. System calls are an interface between a process and the operating system. And they're the only way to switch from user mode to kernel mode.

### Types of System Calls
![image](https://github.com/user-attachments/assets/8aba74b4-45ec-4879-8e95-c6c0db50c60b)

#### File System 
These system calls are made while working with files in OS, File manipulation operations such as creation, deletion, termination etc.

1. open(): Opens a file for reading or writing. A file could be of any type like text file, audio file etc.
2. read(): Reads data from a file. Just after the file is opened through open() system call, then if some process want to read the data from a file, then it will make a read() system call.
3. write(): Writes data to a file. Wheneve the user makes any kind of modification in a file and saves it, that's when this is called.
4. close(): Closes a previously opened file.
5. seek(): Moves the file pointer within a file.

#### Process Control
These types of system calls deal with process creation, process termination, process allocation, deallocation etc. Basically manages all the process that are a part of OS.

1. fork(): Creates a new process (child) by duplicating the current process (parent). This call is made when a process makes a copy of itself and the parent process is halted temporarily until the child process finishes its execution.
2. exec(): Loads and runs a new program in the current process and replaces the current process with a new process.
3. wait(): The primary purpose of this call is to ensure that the parent process doesn't proceed further with its execution until all its child processes have finished their execution.
4. exit(): It simply terminates the current process.
5. kill(): This call sends a signal to a specific process and has various purpose including - requesting it to quit voluntarily, or force quit, or reload configuration. 

#### IPC
When two or more process are required to communicate, then various IPC mechanism are used by the OS which involves making numerous system calls. 

1. pipe(): Creates a unidirectional communication channel between processes. 
2. socket(): Creates a network socket for communication.
3. shmget(): It is short for - 'shared-memory-get'.
4. semget(): It is short for - 'semaphore-get'. 
5. msgget(): It is short for - 'message-get'.

#### Device Management
The device management system calls are used to interact with various peripherial devices attached to the PC or even the management of the current device.

1. SetConsoleMode(): This call is made to set the mode of console (input or output). It allows a process to control various console modes. In windows, it is used to control the behaviour of command line.
2. WriteConsole(): It allows us to write data on console screen.
3. ReadConsole(): It allows us to read data from console screen (if any arguments are provided).
4. open(): This call is made whenever a device or a file is opened. A unique file descriptor is created to maintain the control access to the opened file or device.
5. close(): This call is made when the system or the user closes the file or device.
#### Memory Management
These types of system calls deals with memory allocation, deallocation & dynamically changing the size of a memory allocated to a process. 

1. brk(): Changes the data segment size for a process in HEAP Memory.
2. sbrk(): This call is also for memory management in heap, it also takes an argument as an integer (+ve or -ve) specifying whether to increase or decrease the size respectively.
3. mmap(): Memory Map - It basically maps a file or device into main memory 
4. munmap(): Unmaps a memory-mapped file from a process's address space and out of main memory
5. mlock() and unlock(): memory lock defines a mechanism through which certain pages stay in memory and are not swapped out to the swap space in the disk.

![image](https://github.com/user-attachments/assets/7194d8ab-932b-4568-bbdb-a2ff5a779ad3)


