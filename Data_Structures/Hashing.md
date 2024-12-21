# Hashing

As we discussed in Arrays,we have different types of data to be stored and so we have different data structures.
- Hash Table is one such data structure in which we store keys in the table by using a method called hashing, that returns a 'hash key'(which is probably an index)to store the value.
- We have different methods for hashing, such as  modulo division method,mid-square method,digit-folding method.
- The Modulo-division method is the most commonly used method.
- The following C code shows the implementation of hash table using Modulo-division method:

``` C
#include<stdio.h>
int main()
{
	int n,k,i;
	printf("Enter  the number of keys to store:");
	scanf("%d",&k);
	printf("Enter the size of the table:");
	scanf("%d",&n);
	
	if(k>n)
	{
		printf("Error!!Number of keys should not be greater than table-size.");
		return 1;
	}
	
	int hasharray[n];
	for(i=0;i<n;i++)
	{
		hasharray[i]=-1;
	}
	
	printf("Enter k keys:");
	for(i=0;i<k;i++)
	{
		int key;
		scanf("%d",&key);
		int loc=key%n;
		if(hasharray[loc]==-1)
		{
			hasharray[loc]=key;
		}
		else
		{
			printf("Collision occured,unable to store the elements");
		}
	}
	
	printf("Elements after sorting keys:\n");
	for(i=0;i<n;i++)
	{
		if(hasharray[i]!=-1)
		{
			printf("Hasharray[%d]:[%d]\n",i,hasharray[i]);
		}
	}
}
```

Output:
```
Enter  the number of keys to store:5
Enter the size of the table:10
Enter k keys:
12
63
86
39
40
Elements after sorting keys:
Hasharray[0]:[40]
Hasharray[2]:[12]
Hasharray[3]:[63]
Hasharray[6]:[86]
Hasharray[9]:[39]
```


- Here we have certain cases where we get the  same hashkey for more thanone element, such a condition is called 'Collision'.
- There are some effective Collision resolution techniques that ensure better allocation of indices to the keys.
- The following are the different Collision Resolution Methods:
1. Linear Probing
2. Quadratic Probing
3. Seperate chaining

### Linear Probing:

Linear probing is the first and most basic collision resolution technique used.

If collision occurs at any location, it simply solves the problem by allocating new location in the following way.
```
int loc=(loc+1)%n;
```

The following code depicts Linear Probing.

``` C
#include<stdio.h>

int linearprob(int loc,int n)
{
	loc=(loc+1)%n;
	return loc;
}

int main()
{
	int n,k,i;
	printf("Enter  the number of keys to store:");
	scanf("%d",&k);
	printf("Enter the size of the table:");
	scanf("%d",&n);
	
	if(k>n)
	{
		printf("Error!!Number of keys should not be greater than table-size.");
		return 1;
	}
	
	int hasharray[n];
	for(i=0;i<n;i++)
	{
		hasharray[i]=-1;
	}
	
	printf("Enter k keys:");
	for(i=0;i<k;i++)
	{
		int key;
		scanf("%d",&key);
		int loc=key%n;
		while(hasharray[loc]!=-1)
		{
			loc=linearprob(loc,n);
		}
		hasharray[loc]=key;
	}
	
	printf("Elements after sorting keys:\n");
	for(i=0;i<n;i++)
	{
		if(hasharray[i]!=-1)
		{
			printf("Hasharray[%d]:[%d]\n",i,hasharray[i]);
		}
	}
}
```

Output:
```
Enter  the number of keys to store:5
Enter the size of the table:10
Enter k keys:23
54
92
84
12
Elements after sorting keys:
Hasharray[2]:[92]
Hasharray[3]:[23]
Hasharray[4]:[54]
Hasharray[5]:[84]
Hasharray[6]:[12]
```

### Quadratic probing

It is a collision resolution technique in which we use the following method to solve the problem of collision:
```
int loc=(loc+i*i)%n;
where i gets incremented each time;
```

The following C code depicts the use of Quadratic Probing:

``` C
#include<stdio.h>

int linearprob(int loc,int s,int n)
{
	return(loc+s*s)%n;
}

int main()
{
	int n,k,i;
	printf("Enter  the number of keys to store:");
	scanf("%d",&k);
	printf("Enter the size of the table:");
	scanf("%d",&n);
	
	if(k>n)
	{
		printf("Error!!Number of keys should not be greater than table-size.");
		return 1;
	}
	
	int hasharray[n];
	for(i=0;i<n;i++)
	{
		hasharray[i]=-1;
	}
	
	printf("Enter k keys:");
	for(i=0;i<k;i++)
	{
		int key;
		int s=0;
		scanf("%d",&key);
		int loc=key%n;
		while(hasharray[loc]!=-1)
		{
			loc=linearprob(loc,s,i);
		}	
		hasharray[loc]=key;	
	}
	
	printf("Elements after sorting keys:\n");
	for(i=0;i<n;i++)
	{
		if(hasharray[i]!=-1)
		{
			printf("Hasharray[%d]:[%d]\n",i,hasharray[i]);
		}
	}
}
```

Output:
```
Enter  the number of keys to store:5
Enter the size of the table:10
Enter k keys:32
62
55
89
77
Elements after sorting keys:
Hasharray[0]:[62]
Hasharray[2]:[32]
Hasharray[5]:[55]
Hasharray[7]:[77]
Hasharray[9]:[89]
```

### Separate Chaining

This is a collision resolution technique in which we use a linked list, at the index where collision occurs and we store all the keys which return that hash index so that collision would be resolved.

