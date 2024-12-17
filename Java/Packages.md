# Packages

Packages are directories that contains set of classes and interfaces as a unit.
Packages are a way to organise related classes and interfaces into namespaces.
There are two kinds of packages:

1. User-defined packages
2. In-built packages

## In-built Packages
java provides a set of inbuilt packages that come with java Development Kit(JDK),and provide wide range of functionality such as data structures and file handling etc.

Here's an example program for in-built packages

``` Java
package g;
import java.util.*;

public class InbuiltP
{
	public static void main(String[] args)
	{
		String str;
		Scanner sc=new Scanner(System.in);
		System.out.println("Enter the name:");
		str=sc.nextLine();
		System.out.println("Name:"+str);
	}
}
```

Output:
```
Enter the name:
Alliswell
Name:Alliswell
```

## User-defined packages

These packages are created by the user to group related classes and interfaces.
Here's an example program for User-defined packages

``` Java
package mypackage;

class Bird {
    public void fly() {
        System.out.println("Bird flies");
    }
}

class Crow extends Bird {
    public void fly() {
        System.out.println("Crow flies");
    }
}

public class Main {
    public static void main(String[] args) {
        Bird b = new Bird();
        b.fly(); // Output: Bird flies

        Crow c = new Crow();
        c.fly(); // Output: Crow flies
    }
}
```
