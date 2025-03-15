# 100 Coding Questions in Java(Simple-->Difficult)

## 0.Easy

1.A Simple Code to print Hello World.
```
public class Sample
{
	public static void main(String[] args)
	{
		System.out.println("Hello  World!");
	}
}
```

Output:
```
Hello World! 
```

2.Asking the user to enter their name
```
import java.util.*;
import java.lang.*;
public class Code2
{
	public static void main(String[] args)
	{
		Scanner obj=new Scanner(System.in);
		System.out.println("Enter Your name:");
		String name=obj.nextLine();
	}
}
```

Output:
```
Enter Your name:
ArunMuli
```

3.Basic Arithmetic
```
import java.util.*;
import java.lang.*;
public class Code3
{
	public static void main(String[] args)
	{
		Scanner obj=new Scanner(System.in);
		System.out.println("Enter Numbers:");
		int a=obj.nextInt();
		int b=obj.nextInt();
		System.out.println("Sum:"+(a+b));
		System.out.println("Difference:"+(a-b));
		System.out.println("Product:"+(a*b));
	}
}
```

Output:
```
Enter Numbers:
8
2
Sum:10
Difference:6
Product:16
```

4.Area of Rectangle
```
import java.util.*;
import java.lang.*;
public class Code4
{
	public static void main(String[] args)
	{
		Scanner obj=new Scanner(System.in);
		System.out.println("Enter length and breadth:");
		int l=obj.nextInt();
		int b=obj.nextInt();
		System.out.println("Area of Rectangle:"+(l*b));
	}
}
```

Output:
```
Enter length and breadth:
12
6
Area of Rectangle:72
```

5.Area of circle
```
public class Code5
{
	public static void main(String[] args)
	{
		int r=65;
		System.out.println("Radius of circle:"+r);		
		System.out.println("Area of Circle:"+(3.14*r*r));
	}
}

```

Output:
```
Radius of circle:65
Area of Circle:13266.5
```

6.Average of 3 numbers
```
import java.util.*;
import java.lang.*;
public class New1
{
	public static void main(String[] args)
	{
		Scanner obj=new Scanner(System.in);
		System.out.println("Enter three numbers:");
		int a=obj.nextInt();
		int b=obj.nextInt();
		int c=obj.nextInt();
		System.out.println("Average of 3 numbers is:"+((a+b+c)/3));
	}
}
```

Output:
```
Enter three numbers:
69
56
37
Average of 3 numbers is:54
```

7.Even or Odd
```
import java.util.*;
import java.lang.*;
public class New1
{
	public static void main(String[] args)
	{
		Scanner obj=new Scanner(System.in);
		System.out.println("Enter a number:");
		int a=obj.nextInt();
		if(a%2==0)
		{
			System.out.println("The given number is even.");
		}
		else
		{
			System.out.println("The given number is odd.");
		}
	}
}

```

Output:
```
Enter a number:
9
The given number is odd.

Enter a number:
8
The given number is even.
```

8.positive/negative/zero
```
import java.util.*;
import java.lang.*;
public class New1
{
	public static void main(String[] args)
	{
		Scanner obj=new Scanner(System.in);
		System.out.println("Enter a number:");
		int a=obj.nextInt();
		if(a>0)
		{
			System.out.println("The given number is positive.");
		}
		else if(a<0)
		{
			System.out.println("The given number is negative.");
		}
		else
		{
			System.out.println("The given number is zero.");
		}
	}
}
```

Output:
```
Enter a number:
-7
The given number is negative.

Enter a number:
8
The given number is positive.

Enter a number:
0
The given number is zero.
```

9.larger of 2 numbers
```
import java.util.*;
import java.lang.*;
public class New1
{
	public static void main(String[] args)
	{
		Scanner obj=new Scanner(System.in);
		System.out.println("Enter first number:");
		int a=obj.nextInt();
		System.out.println("Enter second number:");
		int b=obj.nextInt();
		if(a>b)
		{
			System.out.println("The first number is greater one.");
		}
		else
		{
			System.out.println("The second number is greater one.");
		}
	}
}
```

Output:
```
Enter first number:
78
Enter second number:
66
The first number is greater one.
```

10.Simple interest
```
import java.util.*;
import java.lang.*;
public class New1
{
	public static void main(String[] args)
	{
		Scanner obj=new Scanner(System.in);
		System.out.println("Enter P:");
		int p=obj.nextInt();
		System.out.println("Enter T:");
		int t=obj.nextInt();
		System.out.println("Enter R:");
		int r=obj.nextInt();
		int i=(p*t*r)/100;
		System.out.println("I="+i);
	}
}
```

Output:
```
Enter P:
1000
Enter T:
6
Enter R:
7
I=420
```

## 1. Basic control

11.Greatest of 3 no.s
```
import java.util.*;
import java.lang.*;
public class New1
{
	public static void main(String[] args)
	{
		Scanner obj=new Scanner(System.in);
		System.out.println("Enter first number:");
		int p=obj.nextInt();
		System.out.println("Enter second number:");
		int t=obj.nextInt();
		System.out.println("Enter third number:");
		int r=obj.nextInt();
		if(p>t && p>r)
		{
			System.out.println("The first number is the greatest of three.");
		}
		else if(t>p && t>r)
		{
			System.out.println("The second number is the greatest of three.");
		}
		else if(r>p && r>t)
		{
			System.out.println("The third number is the greatest of three.");
		}
		else
		{
			System.out.println("All three numbers are equal.");
		}
	}
}
```

Output:
```
Enter first number:
10
Enter second number:
7
Enter third number:
12
The third number is the greatest of three.

Enter first number:
9
Enter second number:
2
Enter third number:
1
The first number is the greatest of three.

Enter first number:
3
Enter second number:
3
Enter third number:
3
All three numbers are equal.
```

12.Leap year
```
import java.util.*;
import java.lang.*;
public class New1
{
	public static void main(String[] args)
	{
		Scanner obj=new Scanner(System.in);
		System.out.println("Enter year:");
		int p=obj.nextInt();
		if(p%4==0)
		{
			System.out.println("The given year is leap year.");
		}
		else
		{
			System.out.println("The given year is not leap year.");
		}
	}
}
```

Output:
```
Enter year:
2035
The given year is not leap year.

Enter year:
2020
The given year is leap year.
```

13.Grade
```
import java.util.*;
import java.lang.*;
public class New1
{
	public static void main(String[] args)
	{
		Scanner obj=new Scanner(System.in);
		System.out.println("Enter Maths marks:");
		int math=obj.nextInt();
		System.out.println("Enter Science marks:");
		int s=obj.nextInt();
		System.out.println("Enter English marks:");
		int e=obj.nextInt();
		System.out.println("Enter Social marks:");
		int social=obj.nextInt();
		System.out.println("Enter Physics marks:");
		int phy=obj.nextInt();
		int total=(math+s+e+social+phy)/5;
		if(total>90)
		{
			System.out.println("Congratulations!!!You've secured 'A' Grade");
		}
		else if(total>80 && total<90)
		{
			System.out.println("You've secured 'B' Grade");
		}
		else
		{
			System.out.println("You've secured 'C' Grade");
		}
	}
}

```

Output:
```
Enter Maths marks:
99
Enter Science marks:
90
Enter English marks:
89
Enter Social marks:
87
Enter Physics marks:
88
You've secured 'C' Grade
```

14.Sum of first n natural numbers
```
package g;
import java.util.*;
import java.lang.*;
public class New1
{
	public static void main(String[] args)
	{
		Scanner obj=new Scanner(System.in);
		System.out.println("Enter any number:");
		int num=obj.nextInt();
		int sum=0;
		for(int i=0;i<=num;i++)
		{
			sum+=i;
		}
		System.out.println("Sum of numbers upto "+num+" is:"+sum);
	}
}
```

Output:
```
Enter any number:
4
Sum of numbers upto 4 is:10
```

15.factorial of a number
```
package g;
import java.util.*;
import java.lang.*;
public class New1
{
	public static void main(String[] args)
	{
		Scanner obj=new Scanner(System.in);
		System.out.println("Enter any number:");
		int num=obj.nextInt();
		int fact=1;
		for(int i=1;i<=num;i++)
		{
			fact*=i;
		}
		System.out.println("Factorial of the number is:"+fact);
	}
}
```

Output:
```
Enter any number:
6
Factorial of the number is:720
```

16.Prime number
```
package g;
import java.util.*;
import java.lang.*;
public class New1
{
	public static void main(String[] args)
	{
		Scanner obj=new Scanner(System.in);
		System.out.println("Enter a number:");
		int num=obj.nextInt();
		if(num<=1)
		{
			System.out.println("Neither prime nor composite.");
		}
		else
		{
			for(int i=2;i<Math.sqrt(num);i++)
			{
				if(num%i==0)
				{
					System.out.println("The entered number is a composite number.");
				}
				else
				{
					System.out.println("The entered number is a Prime number.");
					break;
				}
			}
		}
	}
}
```

Output:
```
Enter a number:
31
The entered number is a Prime number.
```

17.Fibonacci
```
package g;
import java.util.*;
import java.lang.*;
public class New1
{
	int Calfib(int num)
	{
		if(num<=1)
		{
			return num;
		}
		int[] fib=new int[num+1];
		fib[0]=0;
		fib[1]=1;
		for(int i=2;i<=num;i++)
		{
			fib[i]=fib[i-1]+fib[i-2];
		}
		return fib[num];
	}
	public static void main(String[] args)
	{
		Scanner sc=new Scanner(System.in);
		System.out.println("Enter number:");
		New1 obj=new New1();
		int num=sc.nextInt();
		if(num<1)
		{
			System.out.println("Enter valid number");
		}
		else
		{
			System.out.println("Fibonacci upto "+ num +"is:"+obj.Calfib(num));
		}
	}
	
}
```

Output:
```
Enter number:
8
Fibonacci upto 8is:21

Enter number:
11
Fibonacci upto 11is:89
```

18.Palindrome
```
package g;
import java.util.*;
import java.lang.*;
public class New1
{
	public static void main(String[] args)
	{
		Scanner sc=new Scanner(System.in);
		System.out.println("Enter any String:");
		String str=sc.nextLine();
		StringBuilder sb=new StringBuilder(str);
		sb.reverse();
		String str2=sb.toString();
		if(str.equals(str2))
		{
			System.out.println("The given String is a Palindrome.");
		}
		else
		{
			System.out.println("Not a Palindrome.");
		}
	}
}
```

Output:
```
Enter any String:
madam
The given String is a Palindrome.

Enter any String:
satwika
Not a Palindrome.
```

19.Reverse a string
```
package g;
import java.util.*;
import java.lang.*;
public class New1
{
	public static void main(String[] args)
	{
		Scanner obj=new Scanner(System.in);
		System.out.println("Enter any string:");
		String str=obj.nextLine();
		System.out.println("Reverse of the given string is:");
		for(int i=(str.length()-1);i>=0;i--)
		{
			System.out.print(str.charAt(i));
		}
	}
}
```

Output:
```
Enter any string:
Github
Reverse of the given string is:
buhtiG
```

20.Count vowels
```
package g;
import java.util.*;
import java.lang.*;
public class New1
{
	public static void main(String[] args)
	{
		Scanner sc=new Scanner(System.in);
		System.out.println("Enter any String:");
		String str=sc.nextLine();
		System.out.println("The given string is:"+str);
		int count=0;
		for(int i=0;i<str.length();i++)
		{
			if(str.charAt(i)=='a'||str.charAt(i)=='e'||str.charAt(i)=='i'||str.charAt(i)=='o'||str.charAt(i)=='u')
			{
				count++;
			}
		}
		System.out.println("Number of vowels in the given string:"+count);
	}
}
```

Output:
```
Enter any String:
satwika
The given string is:satwika
Number of vowels in the given string:3
```

21.Sum of digits
```
package g;

import java.util.*;

public class New1
{
	public static void main(String[] args)
	{
		Scanner sc=new Scanner(System.in);
		System.out.println("Enter a number:");
		int num=sc.nextInt();
		int sum=0;
		for(;num!=0;)
		{
			int r=num%10;
			sum+=r;
			num/=10;
		}
		System.out.println("Sum of digits is:"+sum);
	}
}
```

Output:
```
Enter a number:
9999
Sum of digits is:36
```

22.Armstrong
```

```

Output:
```

```

23.Multiplication table
```
package g;

import java.util.*;

public class New1
{
	public static void main(String[] args)
	{
		Scanner sc=new Scanner(System.in);
		System.out.println("Enter a number:");
		int num=sc.nextInt();
		for(int i=1;i<=10;i++)
		{
			System.out.println(num+"x"+i+"="+(num*i));
		}
	}
}
```

Output:
```
Enter a number:
5
5x1=5
5x2=10
5x3=15
5x4=20
5x5=25
5x6=30
5x7=35
5x8=40
5x9=45
5x10=50
```

24.Simple calc
```
package g;

import java.util.*;

public class New1
{
	public static void main(String[] args)
	{
		Scanner sc=new Scanner(System.in);
		System.out.println("Enter first number:");
		int a=sc.nextInt();
		System.out.println("Enter first number:");
		int b=sc.nextInt();
		Scanner obj=new Scanner(System.in);
		System.out.println("Enter operation:");
		String op=obj.nextLine();
		switch(op)
		{
		case "m":
			int m=a*b;
			System.out.println(a+"x"+b+"="+m);
			break;
		case "s":
			int s=a-b;
			System.out.println(a+"+"+b+"="+s);
			break;
		case "a":
			int add=a+b;
			System.out.println(a+"-"+b+"="+add);
			break;
		case "d":
			int d=a/b;
			System.out.println(a+"/"+b+"="+d);
			break;
		default:
			System.out.println("Enter valid symbol");
		}
	}
}
```

Output:
```
Enter first number:
8
Enter first number:
8
Enter operation:
s
8+8=0
```

25.number guessing
```

```

Output:
```

```

## 2.Arrays & Loops  

26.Sum of elements in Array
```
package g;

import java.util.*;

public class New1
{
	public static void main(String[] args)
	{
		int arr[]= {1,6,2,8,3,9,4,6,5};
		System.out.println("The array is:");
		for(int i=0;i<arr.length;i++)
		{
			System.out.print(arr[i]+" ");
		}
		System.out.println();
		int sum=0;
		for(int i=0;i<arr.length;i++)
		{
			sum+=arr[i];
		}
		System.out.println("Sum of array elements:"+sum);
	}
}
```

Output:
```
The array is:
1 6 2 8 3 9 4 6 5 
Sum of array elements:44
```

27.Average of array elements
```
package g;

import java.util.*;

public class New1
{
	public static void main(String[] args)
	{
		int arr[]= {1,6,2,8,3,9,4,6,5};
		System.out.println("The array is:");
		for(int i=0;i<arr.length;i++)
		{
			System.out.print(arr[i]+" ");
		}
		System.out.println();
		int sum=0;
		for(int i=0;i<arr.length;i++)
		{
			sum+=arr[i];
		}
		int n=arr.length;
		int avg=sum/n;
		System.out.println("Average of array elements:"+avg);
	}
}
```

Output:
```
The array is:
1 6 2 8 3 9 4 6 5 
Average of array elements:4
```

28.Maximum element in array
```
package g;

import java.util.*;

public class New1
{
	public static void main(String[] args)
	{
		int arr[]= {1,6,2,8,3,9,4,6,5};
		System.out.println("The array is:");
		for(int i=0;i<arr.length;i++)
		{
			System.out.print(arr[i]+" ");
		}
		System.out.println();
		int lar=arr[0];
		for(int i=1;i<arr.length;i++)
		{
			if(arr[i]>lar)
			{
				lar=arr[i];
			}
		}
		System.out.println("Maximum element in array:"+lar);
	}
}
```

Output:
```
The array is:
1 6 2 8 3 9 4 6 5 
Maximum element in array:9
```

29.Minimum element in array
```
package g;

import java.util.*;

public class New1
{
	public static void main(String[] args)
	{
		int arr[]= {1,6,2,8,3,9,4,6,5};
		System.out.println("The array is:");
		for(int i=0;i<arr.length;i++)
		{
			System.out.print(arr[i]+" ");
		}
		System.out.println();
		int lar=arr[0];
		for(int i=1;i<arr.length;i++)
		{
			if(arr[i]<lar)
			{
				lar=arr[i];
			}
		}
		System.out.println("Maximum element in array:"+lar);
	}
}
```

Output:
```
The array is:
1 6 2 8 3 9 4 6 5 
Maximum element in array:1
```

30.Linear search
```
package g;
import java.util.*;
import java.lang.*;
public class New1
{
	public static void main(String[] args)
	{
		int arr[]= {12,43,25,66,89};
		int flag=0;
		Scanner sc=new Scanner(System.in);
		System.out.println("Enter key to find:");
		int key=sc.nextInt();
		for(int i=0;i<arr.length;i++)
		{
			if(arr[i]==key)
			{
				flag=1;
				break;
			}
		}
		if(flag==1)
		{
			System.out.println("Element found in the array");
		}
		else
		{
			System.out.println("Element not found in the array.");
		}
	}
}
```

Output:
```
Enter key to find:
66
Element found in the array

Enter key to find:
33
Element not found in the array.

```

32.Binary Search
```

```

Output:
```

```

33.
```

```

Output:
```

```

34.
```

```

Output:
```

```

35.
```

```

Output:
```

```

36.
```

```

Output:
```

```

37.
```

```

Output:
```

```

38.
```

```

Output:
```

```

39.
```

```

Output:
```

```

40.
```

```

Output:
```

```
