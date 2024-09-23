# Classes and Objects

Contents
- Introduction to classes,objects
- Constructurs-types,overloading
- Methods-overloading
- Keywords-this,static,final
- Garbage Collection
# Inheritance

Contents
- Types
- Method overriding
- super keyword
- interface
- abstract class

### Introduction to classes and objects

#### Class:
Class is like an object constructor.

It is a blueprint for creating objects.

To create a class use the keyword class.

``` Java
class Main
{
  //variables
  //methods
}
```
#### Objects
Object of a class is created in another class.

To create an object for a class, specify the class name and use the keyword new.
``` Java
public class Main
{
  int x=5;
}
class Execute
{
  public static void main(String[] args)
  {
    Main myobj=new Main();
  }
}
```

#### Constructors

* Constructor is a special method used to initialize objects.

* Constructor name is the same name as the class name.

* We cannot extend constructor.

* A constructor does not have any return type.

* Constructor is automatically called when an object is created.

* A constructor is used to create one object at a time.

eg:

``` Java
public class Main
{
  int x;
  Main(int y)
  {
    x=y;
  }
}
public class Execute
{
  public static void main(String[] args)
  {
    Main myobj=new Main(5);
    System.out.println(myobj.x);
  }
}
```
Types of constructors:

1)Default: This types of constructors have no parameters.Default constructor is called when creating objects.

2)Parametrised: These constructors have parameters.

#### Constructor Overloading

When a constructor is used multiple times in a class with different parameters each time used, It is called constructor overloading.

Example code:
``` Java
class Main
{
  Main(int a,int b,int c)
  {
    first=a;
    second=b;
    third=c;
  }
  Main()
  {
    first=second=last=5;
  }
  Main(int val)
  {
    first+second+third=val;
  }
}
public class Execute
{
  public static void main(String[] args)
  {
    Main obj1=new Main(4,5,6);
    Main obj2=new Main();
    Main obj3=new Main(8);
    sum=obj1.


    System.out.println("
