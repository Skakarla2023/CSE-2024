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

``` C++

```

Output:
```

```
### Single Number

``` C++

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
