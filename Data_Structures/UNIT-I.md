# UNIT-I

#### Algorithm- 
It is a step by step process of solving a given problem.

### Performance analysis of an algorithm:
The efficiency of an algorithm can be decided by measuring the performance of an algorithm.We can measure this by using 2 factors.
They are-

#### Time complexity
Time complexity can be defined as the amount of time taken by the algorithm to execute as function of length of input.

#### Space complexity
Space complexity can be referred as the amount of memory used by the algorithm as a function of length of input.It includes both amount of memory used by the algorithm as well as the input.

- There are different types of notation to represent time complexity of an algorithm. they are called asymptotic notations.
They are-
```
1.Big O notation
2.Theta notation
3.Omega notation
4.small o notation
5.small omega notation
```

|Symbol   | Notation meaning  | example                |
|---------|-------------------|------------------------|
| O(1)    | constant          | sum of 2 numbers       |
| O(n)    | linear            | linear search          |
| O(logn) | logarithmic       | sorting                |
| O(nlogn)| linear arithmetic | divide and conquer     |
| O(n^2)  | quadratic         | addition of 2 matrices |
| O(n^3)  | cubic             |simultaneous linear eqns|
| O(2^n)  | exponential       | towers of hanoii       |

 - A data structure that manitains a linear relationship among its elements is called a LINEAR DATA STRUCTURE.
 - A Data Structure in which elements are not arranged in sequential order is called a NON-LINEAR DATA STRUCTURE.

#### Hashing or Hash Table
Hash table is a data structure used for stoing and retrieving data very quickly.
Insertion of element in hash table is based on the key.

![image](https://github.com/user-attachments/assets/9af6a500-202e-4ea4-bc4d-2fa8d6f8551f)

- Types of hash methods
  1. Modulo division method
  2. Mid-square method
  3. digit folding method
  4. Multiplicative method

There are several methods to map keys to indexes 
#### Collision
In data structures collision occurs when two keys map to the same index in a hash table.

- There are several methods called collision resolution techniques to solve the problem of collision
```
1.Linear Probing
2.Quadratic Probing
3.Seperate chaining
```

binary search, Interpolation Search,
Insertion Sort, Shell sort, Quick Sort, Merge Sort..

##### Linear search-
Linear search is a sequential searching algorithm in data structures in which we search each element sequentially starting from the beginning.
It works sequentially by starting from the beginning of the list and go until the desired element is found or the list ends.

The following C code shows the implementation of linear search in C
```
#include<stdio.h>
int main()
{
	int arr[5]={12,36,47,50,79};
	int i,k,flag;
	printf("Enter key value:\n");
	scanf("%d",&k);
	int len=sizeof(arr)/sizeof(arr[0]);
	for(i=0;i<len;i++)
	{
		if(k==arr[i])
		{
			flag==1;
			break;
		}
	}
	if(flag==1)
	{
		printf("Element is found\n");
	}
	else
	{
		printf("Element not found\n");
	}
	return 0;
}
```

##### Binary search
Binary search is a searching algorithm that works on sorted arrays or lists. It operates by dividing the arra into half and calculating the mid and finding the required element.

The following C code shows the implementation of binary search in C-

```
#include<stdio.h>

int main()
{
    int a[10] = {1, 2, 3, 4, 5, 6, 7, 8, 9, 10};  
    int mid, fi, li, key, n, i;
    n = sizeof(a) / sizeof(a[0]);  
    fi = 0, li = n - 1;
    
    printf("The array is: ");
    for(i = 0; i < n; i++)
    {
        printf("%d ", a[i]);
    }
    printf("\nEnter the key you want to search: ");
    scanf("%d", &key);
    
    while (fi <= li)
    {  
        mid = (fi + li) / 2;
        
        if (a[mid] == key)
        {
            printf("Element is found at index %d\n", mid);
            return 0; 
        }
        else if (a[mid] < key)
        {
            fi = mid + 1;
        }
        else
        {
            li = mid - 1;
        }
    }    
    printf("Element is not found\n"); 
    return 0;
}
```

##### Insertion sort
Insertion sort is a comparision based sorting algorithm, it starts from second element considering first element as sorted and it inserts each element in such a way that each time the swapping happens it compares its previous element and next element to the current element.

```

```
