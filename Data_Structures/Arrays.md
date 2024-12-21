# Data Structures

- Every real life system such as websites or web applications or software,all these run on data.
- Data Structures are the structures that store and organise data.
- These are not only used for storing the data, they also ensure effective operations on the data such as retrieval,modifications and deletion.
- There are different types of data, that's why we need different types of data structures to store data.
- Some examples of data structures are:
```
Arrays
Linked lists
stacks
queues
graphs
trees
```
## Arrays
- Arrays are the basic data structures that are used to store data in a linear manner.
- Arrays store number of elements, with a single array_name.
- Array elements are stored contiguously in memory.
- Arrays have index that indicates position of any particular element in the array.
- Arrays store same type of data in them.
- Here's a C code showing different operations on an array:

``` C
#include<stdio.h>

void swap(int smallest,int largest)
{
	int temp=smallest;
	smallest=largest;
	largest=temp;
	printf("Smallest:%d\n",smallest);
	printf("Largest:%d\n",largest);
}

int main()
{
	int arr[5]={12,23,34,45,56}; 
	int n=sizeof(arr)/sizeof(arr[0]);
	int i;
	
	// printing the elements in the array
	printf("Elements in the array are:\n");
	for(i=0;i<n;i++)
	{
		printf("%d\n",arr[i]);
	}
	
	//printing ele in reverse order
	printf("In reverse order:\n");
	for(i=n-1;i>=0;i--)
	{
		printf("%d\n",arr[i]);
	}
	
	//finding the smallest
	int smallest=arr[0];
	for(i=0;i<n;i++)
	{
		if(arr[i]<smallest)
		{
			smallest=arr[i];
		}
	}
	printf("Smallest element in the array:%d\n",smallest);
	
	//finding the largest
	int largest=arr[n-1];
	for(i=0;i<n;i++)
	{
		if(arr[i]>largest)
		{
			largest=arr[i];
		}
	}
	printf("Largest element in the array:%d\n",largest);
	
	//sum of array ele
	int sum=0;for(i=0;i<n;i++)
	{
		sum+=arr[i];
	}
	printf("Sum of elements in array:%d\n",sum);
	
	//product of array ele
	int pro=1;
	for(i=0;i<n;i++)
	{
		pro*=arr[i];
	}
	printf("Product of elements in array:%d\n",pro);
	
	//swapping largest and smallest
	swap(smallest,largest);
	
	return 0;
}
```

Output:
```
Elements in the array are:
12
23
34
45
56
In reverse order:
56
45
34
23
12
Smallest element in the array:12
Largest element in the array:56
Sum of elements in array:170
Product of elements in array:23647680
Smallest:56
Largest:12
```





#### Bubble sort

- Bubble sort is an algorithm that sorts the array from lowest value to highest value.
* Alogorithm:

The following python code shows the implementation  of bubble sort:
``` Python
myarr=[64,34,25,22,12,11,90,5]
n=len(myarr)
for i in range(n-1);
  for j in range(n-i-1):
    if(myarr[j]>myarr[j+1]:
      myarr[j],myarr[j+1]=myarr[j+1],myarr[j]
print(sorted array:",myarr)
```
    
#### Selection sort

- Selection sort algorithm finds the lowest value in the array and moves it to the front.
- The loop loops through the array again and again until all the smaller elements are sent forward and the array is sorted.

  The following python code shows the implementation of selection sort:
``` Python
my_array = [64, 34, 25, 12, 22, 11, 90, 5]

n = len(my_array)
for i in range(n):
    min_index = i
    for j in range(i+1, n):
        if my_array[j] < my_array[min_index]:
            min_index = j   
    my_array[i], my_array[min_index] = my_array[min_index], my_array[i]

print("Sorted array:", my_array)
```

#### Quick sort

- As the name suggests,quick sort is the fastest working algorithm.
- The Quicksort algorithm takes an array of values, chooses one of the values as the 'pivot' element, and moves the other values so that lower values are on the left of the pivot element, and higher values are on the right of it.

The algorithm for Quick sort can be written as-
> Choose a value in the array to be the pivot element.
> 
> Order the rest of the array so that lower values than the pivot element are on the left, and higher values are on the right.
> 
> Swap the pivot element with the first element of the higher values so that the pivot element lands in between the lower and higher values.
> 
> Do the same operations (recursively) for the sub-arrays on the left and right side of the pivot element.

The following java code shows the implementation of quicksort-

``` Java
public class Qs2 
{
	public static int partition(int arr[],int low,int high)
	{
		int pivot=arr[high];
		int i=low-1;
		for(int j=low;j<high;j++)
		{
			if(arr[j]<pivot)
			{
				i++;
				int temp=arr[i];
				arr[i]=arr[j];
				arr[j]=temp;
			}
		}
		i++;
		int temp=arr[i];
		arr[i]=pivot;
		arr[high]=temp;
		return i;
	}
	public static void quicksort(int arr[],int low,int high)
	{
		if(low<high)
		{
			int pi=partition(arr,low,high);
			quicksort(arr,low,pi-1);
			quicksort(arr,pi+1,high);
		}
	}
	public static void main(String[] args)
	{
		int[] arr= {11,56,34,24,22,64,49};
		int n=arr.length;
		
		quicksort(arr,0,n-1);
		System.out.println("Sorted Array: ");
		for(int i:arr)
		{
			System.out.println(i+" ");
		}
		System.out.println();
	}
}
```
Output:
```
Sorted Array: 
11 
22 
24  
34 
49 
56 
64
```
#### Insertion sort
As the name sugests,in this type of sorting technique, we select the element and insert in the correct position based on its value,each value would be shifted to its next position or index each time a new index is added.

``` Python
arr=[12,45,23,68,43,93]
for i in range(1,len(arr)):
    ind=i
    for h in range(i-1,-1,-1):
        if arr[ind]<arr[h]:
            arr[ind],arr[h]=arr[h],arr[ind]
            ind=h
       
print(arr)
```
Output:
```
[12, 23, 43, 45, 68, 93]
```
