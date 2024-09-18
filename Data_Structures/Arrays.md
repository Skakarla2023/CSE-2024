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

