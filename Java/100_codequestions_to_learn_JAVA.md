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

```

Output:
```

```

18.Palindrome
```

```

Output:
```

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

```

Output:
```

```

21.
```

```

Output:
```

```

22.
```

```

Output:
```

```

23.
```

```

Output:
```

```

24.
```

```

Output:
```

```

25.
```

```

Output:
```

```

## 2.Arrays & Loops

26.
```

```

Output:
```

```

27.
```

```

Output:
```

```

28.
```

```

Output:
```

```

29.
```

```

Output:
```

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
