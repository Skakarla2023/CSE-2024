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
