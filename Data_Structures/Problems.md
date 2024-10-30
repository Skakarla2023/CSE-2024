# Some Important Problem statements of DSA

### Maximum Subarray Sum

Subarray refers to a continuous part of an array.

for example if we have an array-{1,2,3,4,5}, 

its subarrays are-{1},{2},{3},{4},{5},{1,2},{2,3},{3,4},{4,5},{1,2,3},{2,3,4},{3,4,5},{1,2,3,4},{2,3,4,5},{1,2,3,4,5}

Source code(BY Brute-Force approach)-
``` C++
#include<iostream>
#include<vector>
using namespace std;

int main()
{
	int n=5;
	int arr[5]={-1,2,-3,4,5};
	
	int maxsum=INT_MIN;
	
	for(int st=0;st<n;st++)
	{
		int currentsum=0;
		for(int end=st;end<n;end++)
		{
			currentsum+=arr[end];
			maxsum=max(currentsum,maxsum);
		}
	}
	cout<<"Maximum subarraysum: "<<maxsum<<endl;
	return 0;
}
```

Output:

```
Maximum subarraysum: 9
```

Source code(By kadane's Algorithm)-

Kadane's algorithm works on the principle that, if there are any negative numbers in the array, then there might be chance that sometimes the sum might change to zero and sometimes even less than zero. i.e., if there is a lesser positive number and bigger negative number the result goes to negative, and in the same way if there is smaller negative number and bigger positive number the result remains positive. So instead of adding such negative numbers, it is better to add '0' to the currentr sum value, so everytime the currentsum tends to a value less than zero, we'll initialize the current sum to 0, again calculating the current sum value.

Updating of currentsum to zero is always done at the end, bcz some arrays contain elements that are negative i.e., all elements are negtaive, then the result has to be negative, not zero(such cases are called edge cases or corner cases).--
		
Source code:

``` C++
#include<iostream>
#include<vector>
using namespace std;

int main()
{
	int n=5;
	int arr[5]={-2,4,-1,5,7};
	int maxsum=INT_MIN;
	int currentsum=0;
	for(int i=0;i<n;i++)
	{
		currentsum+=arr[i];
		maxsum=max(currentsum,maxsum);
		if(currentsum<0)
		{
			currentsum=0;
		}
	}
	cout<<"Result found by Kadane's Algorithm:"<<endl;
	cout<<"Maximum subarray sum: "<<maxsum;
}
```

Output:
```
Result found by Kadane's Algorithm:
Maximum subarray sum: 15
```
### Single Number

In this problem statement we'ew gonna find the single element, element which is unique and is not repeated,i.e., the element which occurs only once in the array,
if we have both positive and negative numbers we can simply add them so that the numbers which are equal to each other but have opposite sign cancel each other. But how do we do this to an array which has all positive numbers.

here's a simple solution to it-

``` C++
#include<iostream>
#include<vector>
using namespace std;

int main()
{
	int v[5]={1,3,3,5,1};
	int n=5;
	int sum=0;
	for(int i=0;i<n;i++)
	{
		sum^=v[i];
	}
	cout<<"Single number:"<<sum;
}
```

Output:
```
Single number:5
```
###

``` C++

```
###
###
###
###
###
###
###
###
###
