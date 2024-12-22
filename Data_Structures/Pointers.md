# Pointers

- Pointers are special variables that store the address of other variables.
- Pointers should be of the same datatype as the variable whose address it is going to store.
- POinters are also declared with * .
- 

### Memory Address

- WHen we create a variable, or declare it in memory in memory of the computer that variable would be occupying some space and the exact location of that variable in the memory is nothing but the Memory address of the variable.
- Memory address of a variable can be acquired using the (&) operator.

``` C
#include<iostream>
using namespace std;
int main()
{
	int a=10;
	cout<<&a<<endl;
	return 0;
}
```

Output:
```
0x6ffe1c
```
### Address of Operator

### Pointers

A simple question on pointers-

Source code-
``` Cpp
#include<iostream>
using namespace std;
int main()
{
	int a=5;
	int* p=&a;
	int** q=&p;
	
	cout<<*p<<endl;
	cout<<**q<<endl;
	cout<<p<<endl;
	cout<<*q<<endl;
}
```

Output:

![image](https://github.com/user-attachments/assets/f87fd5f5-0e8e-4711-8c08-43a25d06a04e)


![image](https://github.com/user-attachments/assets/0f4a7635-7f9e-43ec-a57b-c2d255a2a066)

### Null Pointer

- A null pointer is a pointer that points to nothing, i.e., NULL.
- It does'nt point to any location.
- We cannot dereference a NULL pointer, as it doesn't point to any valid memory location.
- If we try to access such memory location, we get segmentation fault, i.e., we're trying to access a memory loaction that is not possible to be accessed.

Source code-

``` C++
#include<iostream>
using namespace std;
int main()
{
	int* ptr=NULL;
	cout<<ptr;
}
```

Output-

![image](https://github.com/user-attachments/assets/f5ecb260-aafe-4154-88a8-e9613ea9032c)

### Pass by Reference

#### Pass by value

- In pass by value, we pass a copy of the variable as a paramater and try to change the value of variable, but value of the variable doesn't get changed.

Source code-

``` CPP
#include<iostream>
#include<vector>
using namespace std;

void change(int a)
{
	a=20;
	cout<<"Inside the function: "<<a<<endl;
}
int main()
{
	int a=10;
	change(a);
	cout<<"In main: "<<a<<endl;
	return 0;
}
```

Output:

![image](https://github.com/user-attachments/assets/95c658fb-47b5-4ea8-be9f-a53cc299ed55)

#### Pass by reference

In Pass by reference, we pass the address of the variable as the parameter so that it changes the original variable a, instead of another temporary or intermediate variable.

Source code-

```CPP
#include<iostream>
#include<vector>
using namespace std;

void change(int* ptr)
{
	*ptr=20;
	cout<<"Inside the function: "<<*ptr<<endl;
}
int main()
{
	int a=10;
	change(&a);
	cout<<"In main: "<<a<<endl;
	return 0;
}
```

Output:

![image](https://github.com/user-attachments/assets/c23f52fb-6f6d-4fcc-b3f3-a077b4a1fe4e)

- By using alias name, or refrence to the original variable, we change the value of a.

Source code-

``` CPP
#include<iostream> // pass by reference using alias
#include<vector>
using namespace std;

void change(int &b)
{
	b=20;
	cout<<"Inside the function: "<<b<<endl;
}
int main()
{
	int a=10;
	change(a);
	cout<<"In main: "<<a<<endl;
	return 0;
}
```

Output:

![image](https://github.com/user-attachments/assets/34828192-a0ee-4158-9f43-bbc89ab2eb0f)

### Array Pointers

The name of the array always points to the first element of the array.If we try to print the value of array it returns the address of first element of the array.

The name of the array is so called a "Constant pointer".

Example code-

```CPP
#include<iostream>
#include<vector>
using namespace std;

int main()
{
	int arr[]={1,2,3,4,5};
	cout<<arr<<endl;
	cout<<*arr<<endl;
	cout<<&(arr[0])<<endl;
	return 0;
}
```


Output:

![image](https://github.com/user-attachments/assets/737187f0-6c88-4827-b108-11a2bb799c69)

### Pointer Arithmetic

* Increment(++)/Decrement(--)

If we perform increment on normal variables, their value is increased by 1.But what if we perform the same operation on pointers, the size of the variable i.e., the memory size of the datatype is added each time we increment the pointer.

Sample code-
``` CPP
#include<iostream>
#include<vector>
using namespace std;

int main()
{
	int a =4;
	int*p =&a;
	
	cout<<"Before Increment-"<<p<<endl;
	p++;
	cout<<"After Increment-"<<p<<endl;
	
	cout<<"Before Decrement-"<<p<<endl;
	p--;
	cout<<"After Decrement-"<<p<<endl;
	
	return 0;
}
```
Output:

![image](https://github.com/user-attachments/assets/2cb70893-0bc2-480e-af47-68e58ef45541)



* Add/Subtract Number

When we add any number to a pointer, the same thing happens when we increment/decrement the pointer, the size of integer or the datatype is added that many times based on the value that we add to the variable.


Sample code-

``` CPP
#include<iostream>
#include<vector>
using namespace std;

int main()
{
	int a =4;
	int*p =&a;
	
	cout<<"Before Addition-"<<p<<endl;
	p=p+5;
	cout<<"After Addition-"<<p<<endl;
	
	cout<<"Before Subtraction-"<<p<<endl;
	p=p-2;
	cout<<"After Subtraction-"<<p<<endl;
	
	return 0;
}
```

Output:

![image](https://github.com/user-attachments/assets/657db2ec-192c-41c4-9c0e-3ccaf6c72116)

```CPP
#include<iostream>
#include<vector>
using namespace std;

int main()
{
	int arr[]={10,20,30,40};
	int* ptr=arr;
	cout<<*(ptr+1)<<endl;
	cout<<*(ptr+2)<<endl;
	ptr++;
	cout<<*ptr<<endl;
}
```
