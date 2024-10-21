# Pointers

### Memory Address
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
#include<iostream>
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
