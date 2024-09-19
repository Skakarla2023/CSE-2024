# Java Abstraction

Data abstraction is the process of hiding certain details and showing only essential information to the user.
Abstraction can be achieved with either abstract classes or interfaces.

The following code shows how abstract classes and methods are written

``` Java
abstract class Bird                  
{
	public abstract void birdsound();  
    public void fly()              
    {
    	System.out.println("Oooo");
    }
}
class Crow extends Bird           
{
	public void birdsound() 
    {
    	System.out.println("The crow says kaw kaw");
    }
}
public class Main
{
	public static void main(String[] args)
    {
    	Crow mybird=new Crow();    
        mybird.birdsound();
        mybird.fly();
    }
}
```

Output:
```
The crow says kaw kaw
Oooo
```
### Java interface

Interfaces are completely abstract classes that are used to group relative methods with empty bodies / abstract methods.

Interfaces are implemented,like classes are extended.
- Like abstract classes interfaces cannot be used to create objects.
- Interface attributes are by default public,static and final.
- Interface methods are by default abstract and public.
- An interface cannot contain a constructor,as it cannot be used to create objects.
- By creating an interface you must override all of its methods.
- Interface methods do not have a body-the body is provided by the *implement* class.

The following code shows the implementation of interfaces.
``` Java
interface Animal 
{
  public void animalSound(); 
  public void sleep(); 
}

class Pig implements Animal
{
  public void animalSound()
  {
    System.out.println("The pig says: wee wee");
  }
  public void sleep()
  {
    System.out.println("Zzz");
  }
}

class Main 
{
  public static void main(String[] args)
  {
    Pig myPig = new Pig();
    myPig.animalSound();
    myPig.sleep();
  }
}
```
Output:
```
The pig says: wee wee
Zzz
```

### Multiple Interfaces

The following code shows how multiple interfaces can be implemented

``` Java
interface FirstInterface
{
  public void myMethod(); 
}

interface SecondInterface
{
  public void myOtherMethod(); 
}

class DemoClass implements FirstInterface, SecondInterface
{
  public void myMethod() 
  {
    System.out.println("Some text..");
  }
  public void myOtherMethod()
  {
    System.out.println("Some other text...");
  }
}

class Main 
{
  public static void main(String[] args) 
  {
    DemoClass myObj = new DemoClass();
    myObj.myMethod();
    myObj.myOtherMethod();
  }
}
```
Output:

```
Some text...
Some other text...
```

### Java Enums

Enum is a special class that is used to group constant variables(like the ones which are declared final).

Enums just like classes,are created using the keyword enum.
- You can also have an enum inside a class.
- Enums are often used in switch statements to check for correspoding values.

enum enum_name

{

  var1;
  
  var2;
  
  varn;
  
}

The following code depicts implementation of enum

``` Java
enum Level
{
  LOW,
  MEDIUM,
  HIGH
}

public class Main
{ 
  public static void main(String[] args) 
  { 
    Level myVar = Level.MEDIUM; 
    System.out.println(myVar); 
  } 
}
```

Output:

```
MEDIUM
```
### Java ArrayList

ArrayList is different from arrays in the following way:
- Arrays are not resizable where ArrayLists are.
- If you want to add new elements in an array,you have to create new one,but in an ArrayList you can add as many elements as you want.
To use ArrayList, we have to import the ArrayList class from the util package.

> import java.util.ArrayList;
