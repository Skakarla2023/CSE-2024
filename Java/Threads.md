# Threads

In Java, a thread always exists in any one of the following states. These states are:

```
 New
 Runnable
 Running
 Blocked  
 Waiting
 Terminated
```

- New state:
  This is the state when the thread is created, here when a thread is in new state, the code has not been run and hasn't started to execute.
- Runnable:
  In runnable state the thread is about to run and may start it's execution may start at any instance of time,and it is the job of the scheduler to assign it the amount of time to start execute.
- Running-
  When a thread is running or executing it is said to be in running state.
- Blocked:
  When a thread is making use of any resources, it is kept in blocked state.

##### Thread Creation

We can create a thread by extending the thread class  or implementing the Runnable interface.

After extending the Thread class, we've to override it's run() method.

``` Java
public class Threads1 extends Thread
{
	public static void main(String[] args)
	{
		Threads1 th=new Threads1();
		th.start();
		System.out.println("This code is running outside the thread");
	}
	public void run()
	{
		System.out.println("This code is running inside the thread\n");
	}
}
```

Output:
```
This code is running outside the thread
This code is running inside the thread
```

Code written by implementing an interface

``` Java
public class Mythread implements Runnable
{
	public static void main(String[] args)
	{
		Mythread mt=new Mythread();
		Thread th=new Thread(mt);
		th.start();
		System.out.println("This code is running outside the thread.");
	}
	public void run()
	{
		System.out.println("This code is running inside the thread");
	}
}
```
Output:
```
This code is running outside the thread
This code is running inside the thread
```

- The major difference is that when a class extends the Thread class, you cannot extend any other class, but by implementing the Runnable interface, it is possible to extend from another class as well, like: class MyClass extends OtherClass implements Runnable.
- Because threads run at the same time as other parts of the program, there is no way to know in which order the code will run. When the threads and main program are reading and writing the same variables, the values are unpredictable. The problems that result from this are called concurrency problems.
-  
