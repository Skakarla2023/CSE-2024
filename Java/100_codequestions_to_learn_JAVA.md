# 100 Coding Questions in Java(Simple-->Difficult)

## 1.Easy

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
