# Vectors

### Vectors:

Vectors can also be referred to as Dynamic arrays, that can be resized automatically each time a anew element is added in or deleted from the vetor.

We have to include < vector > header file each time we operate with vectors.

The only difference between arrays and vectors is that these are resizable.

Arrays has static memory and vectors are dynamic memory.

The size of the vector increases each time we add a new element.

Vectors are used in place of arrays where we have large number of users, for example any web applications or apps etc.

Vectors are also allocated in two ways in the memory, static(compile time) and dynamic(run time).

static-
```
vector<int> vec={data elements};
vector<dataType> name(size, value); 
```

dynamic-
```
        vector<int> vec;
        vec.pushback(ele);        
        vec.pushback(ele);
 ```
       
There are certain functions in vectors:
- push_back()- inserting new elements
- pop_back()- deleting elements from the vector
- size()- returns the length or number of elements in the vector.
- front()- returns the first/starting element of the vector.
- back()- returns the last/ending element of the vector.
- at()- returns particular index element.

``` C++
#include<iostream>
#include<vector>
using namespace std;
int main()
{
	vector<int> vec;
	vec.push_back(5);
	vec.push_back(4);
	vec.push_back(3);
	vec.push_back(2);
	vec.push_back(1);
	cout<<vec.front()<<endl;
	cout<<vec.back()<<endl;
	cout<<vec.size()<<endl;
	cout<<vec.capacity()<<endl;
	cout<<vec.at(2)<<endl;
	return 0;
}
```

