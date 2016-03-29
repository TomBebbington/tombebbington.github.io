---
published: true
code: 1
title: Programming
layout: post
category: computing
tags: CS3.1
summary: The basics of programming.
---


# Data types
A **data type** is what variables' types are classed as:

## Built-in data types
  * An **integer** is a whole number represented in binary.
    * A **signed** integer can store negative values as well as positive values.
    * An **unsigned** integer can **only** store positive values.
  * A **real** is a number with a decimal part.
    * A **float** is a 32-bit / 4-byte real.
    * A **double** is a 64-bit / 8-byte real.
  * A **boolean** is a true / false value represented as a single bit.
  * A **character** is a UTF character code-point.
  * A **string** is a sequence of characters.
  * A **date** will store data in a format that can be easily identified as a date.
  * A **pointer** points to another data type and can be **dereferenced** to get the data it is pointing to.
  * An **array** is a sequence of the same data type.

## User-definable data types

### Enums
**Enums** are an enumeration of values that can be one of a fixed number of values, but they all have different meanings that don't make sense to  use a number for. An example of this is a direction on a compass:

```java
enum Direction {
  NORTH;
  EAST;
  SOUTH;
  WEST;
}
```

### Objects
A **class** describes what an object has and what it can do, as well as what it is. Its **fields** are variables attached to the object, and its **methods** attach subroutines to the object. If any of these fields or methods have `static` in front, they are attached to the class itself instead. In Java, the following syntax is used:

```java
class Person {
  // fields
  String name;
  int age;
  // methods
  void print() {
    System.out.println(name + " - " + age);
  }
  public static void main() {
    Person kila = new Person();
    kila.name = "Light Yaogami";
    kila.age = 18;
    kila.print(); // "Light Yaogami - 18" is output
  }
}
```

An **object** is an instance of a class. You can access the object from any method using `this`.

#### Constructors
A **constructor** allows a class to give fields values from its arguments and is like any other method, except it is just called the name of the class, and has an empty return type:

```java
class Person {
  // fields
  String name;
  int age;
  // methods
  void print() {
    System.out.println(name + " - " + age);
  }
  Person(String name, int age) {
    this.name = name;
    this.age = age;
  }
  public static void main() {
    Person kila = new Person("Light Yaogami", 18);
    kila.print(); // "Light Yaogami - 18" is output
  }
}
```

# Programming concepts
The following kinds of statements can be used in Java:

## Variable declarations
A **variable declaration** is for when you want to give a name to a value that you want a whole block of code to be able to read and set.

```java
int howMany = 3;
...
System.out.println(howMany); // "3" is output
...
howMany = 4;
System.out.println(howMany); // "4" is output
```

## Constant declarations
A **constant declaration** is for when you want to give a name to a value that won't (and can't) be changed throughout the program.

```java
static final int DUCKS = 200;
...
System.out.println(DUCKS); // "200" is output
```

## Assignment
An **assignment** is for when you want to set a variable or field to a value.

```java
howMany = 4;
```
## Iteration
**Iteration** is the constant repetition of certain parts of a program. There are two kinds:

### Definite iteration
This is where a block is ran a fixed number of times - in Java we use the `for` loop for this:

```java
for(int i = 0; i < 20; i++) // 0, 1, 2, ..., 18. 19
    System.out.println(i);
```

### Indefinite iteration
This, conversely, is where a block is ran an unknown number of times - in Java we use the `while` loop for this:

```java
Scanner scanner = new Scanner(System.in);
while(scanner.hasNext())
	System.out.println(scanner.next());
```

We can exit from inside the while loop using the **break** statement:

```java
String word;
Scanner scanner = new Scanner(System.in);
while(scanner.hasNext()) {
    word = scanner.next();
	System.out.println(word);
    if(word.equals("quit"))
    	break;
}
```
And we can also skip an iteration by using the **continue** statement:

```java
String word;
Scanner scanner = new Scanner(System.in);
while(scanner.hasNext()) {
    word = scanner.next();
    if(word.equals("skip"))
    	continue;
	System.out.println(word);
    if(word.equals("quit"))
    	break;
}
```

## Selectoins
A **selection** is used when you want to run different parts of code when a certain value is different values. In Java, we use `switch` statements or `if` statements depending on if it is either an integer or enum, or not.

```java
int value = 3;
switch(value) {
    case 12:
        return "Yes, this is 12!";
    case 13:
        return "No, this is 13!";
    default:
        return "Whaaat";
}
float other = 3.4f;
if(other == 3.4f)
  return "All is well";
else if(other < 3.4f)
  return "Too smol!";
else
  return "Too berg!";
```
## Subroutines
A **subroutine** is a bit of code with a purpose that returns a specific data type. In Java, we use methods for this purpose:

```java
public static int add(int a, int b) {
    return a + b;
}
```

# Arithmetic operations
These do an operation on two numbers, yielding a number:

  * **addition** is used when you want to add two values or get the summation of several values.

```java
x + y
```
  * **subtraction** is used when you want to take away one value from another.

```java
x - y
```

  * **multiplication** is used when you want to get the product of two or more values.

```java
x * y
```

  * **division** is used when you want to do the inverse of multiplication.
    * **real division** makes the remainder a fraction and adds it to the result.
    * **integer division** ignores the remainder completely.

```java
x / y
```


  * **exponentiation** is used when you want to raise a number to a given power. In Java, we use the `Math.pow` method:

```java
Math.pow(x, y)
```
In Python, we use the built-in operator:
```python
x ** y
```

  * **rounding** is used when you only want a certain degree of accuracy.

```java
Math.round(x / y) * y
```

  * **truncation** is used when you don't want the decimal part of a real value.

# Relation operations
These compare two values, yielding a `boolean`:

  * The **equal to** operator checks if two values are the same. If the value is an object, this checks that it is the same instance of the object.

```java
x == y
```

  * The **not equal to** operator checks if two values are not the same. If the value is an object, this checks that it isn't the same instance of the object.

```java
x != y
```
 
  * The **less than** operator checks if one value is lesser than the other, but does not allow them to be equal.

```java
x < y
```

  * The **less than or equal to** operator checks if one value is lesser than or equal to the other.

```java
x <= y
```

  * The **greater than** operator checks if one value is greater than the other, but does not allow them to be equal.

```java
x > y
```

  * The **greater than or equal to** operator checks if one value is greater than or equal to the other.

```java
x >= y
```

# Boolean operations
These do an operation on booleans, yielding a boolean:
The following boolean operations exist:

  * The **NOT** operator yields the inverse of the value given.

```java
!x
```

  * The **AND** operator returns `true` if both values are `true`.

```java
x && y
```

  * The **OR** operator returns `true` if at least one of the values is `true`.

```java
x || y
```

  * The **XOR** operator yields `true` if just one of the values is `true`.

```java
x ^ y
```

# Constants and variables

## Variables
A **variable** is a value that has been given an identifier and can be changed:

```java
int total = 5;
total = 8;
return total;
```

## Constants
A **constant** is a value that has been given an identifier but can *not* be changed. In Java, a variable can be constant if it has the `final` keyword before it:

```java
final int attempts = 5;
return attempts;
```

# Strings
Strings are declared by surrounding text in double-quotes with a backslash to indicate special characters:

```java
final String text = "Hello, world!";
```

The following operations can be done on strings:
* Its length can be found by the following:

```java
text.length(); // 13
```
* The position of a substring inside a string can be found by:

```java
text.indexOf("world") // 7
```
* The text between positions in a string can be found by:

```java
text.substring(0, 5); // "Hello"
```

* Strings can be joined together using `+`, i.e.:

```java
text + " Hereeee's Johhny" // "Hello, world! Hereeee's Johhny"
```
or:

```java
StringBuilder builder = new StringBuilder();
builder.append(text);
builder.append(" Hereeee's Johhny");
builder.toString(); // "Hello, world! Hereeee's Johhny"
```

* The character at a certain offset of a string can be found by:

```java
text.charAt(5); // ' '
```

To convert a character to a character code (from an `int` to a `char` in Java):

```java
(int) 'a'; // 97
```

And the inverse, to convert a character code to a character (from a `char` to an `int` in Java):

```java
(char) 97; // 'a'
```

* A string can be converted to a primitive in Java by finding the boxed / class version of that primitive then calling its `parse_` method:
```java
int a = Integer.parseInt("32"); // 32
float b = Float.parseFloat("45.321"); // 45.321
double s = Double.parseDouble("3.14159265"); // 3.14159265
```

* Similarly, a primitive can be converted to a string in Java by using the `Primitive.toString` method, where `Primitive` is the boxed version of the primitive. For example:

```java
String a = Integer.toString(32);// "32"
String b = Float.toString(45.321f); // "45.321"
String s = Double.toString(3.14159265d); // "3.14159265"
```

# Random numbers

## Using Math.random
The most flexible way of generating random numbers in Java is by using the method `Math.random`, which returns a **double** between `0` and `1`:

```java
boolean doTheThing = Math.random() < 0.5;
int randomPercent = (int) (Math.random() * 100.);
```

## Just plain Random
Alternatively, random numbers of any numeric type can be generated using the various methods of the `Random` class in Java:

```java
Random rng = new Random();
int a = rng.nextInt();
long bigA = rng.nextLong();
boolean doTheThing = rng.nextBoolean();
double regularOlRandom = rng.nextDouble();
```

# Exception handling
**Exceptions** are errors thrown by a program internally to handle things that *could* error, but don't always. In Java, C, and a lot of similar languages, we use the `try-catch` syntax for this:

```java
String text = null;
try {
  System.out.println(text.length()); // cannot call method on null
} catch(NullPointerException e) {
  System.err.println("Text is null!");
}
```

This example will print `"Text is null!"`, as the 3rd line attempts to call the `length` method on a `null` value which is invalid behaviour, hence the exception being thrown.

# Subroutines
A **subroutine** is a block of code that is give a name, and can be called by writing its name with a set of parentheses after it. In Java, we use methods as subroutines:

```java
static void bark() {
  System.out.println("Bark!");
}
...
bark(); // Bark!
```

In Python, we use functions as subroutines:

```python
def bark():
  print "Bark!"
...
bark(); # Bark!
```

# Subroutine parameters

Subroutines can be passed values when they are called and these values can be given names, similarly to variables. These values are called **arguments**, or **parameters**. In Java, we use the same syntax as with variables:

```java
static void blindMode(String attempt1, String attempt2, String thing) {
  System.out.println("Is it a " + attempt1 + "? Is it a " + attempt2 + "? No, it's " + thing + "!");
}
...
blindMode("bird", "plane", "Superman"); // "Is it a bird? Is it a plane? No, it's Superman!" is output
blindMode("zombie", "mummy", "your reflection"); // "Is it a zombie? Is it a mummy? No, it's your reflection!" is output
```

In Python, we similarly use the same syntax as with variables:

```python
def blind_mode(attempt1, attempt2, thing):
  print "Is it a ", attempt1, "? Is it a ", attempt2, "? No, it's ", thing, "!"
...
blind_mode("bird", "plane", "Superman"); # "Is it a bird? Is it a plane? No, it's Superman!" is output
blind_mode("zombie", "mummy", "your reflection"); # "Is it a zombie? Is it a mummy? No, it's your reflection!" is output
```

# Returning data from a subroutine
So far, none of  the example subroutines have returned nothing, hence they are classified as procedurers, as they:

* Have a return type of `void`.
* Don't contain a `return` statement.

In Java, to make a method return a value, we replace the `void` type with the type we want to return and add a `return` statement:

```java
static String blindMode(String attempt1, String attempt2, String thing) {
  return "Is it a " + attempt1 + "? Is it a " + attempt2 + "? No, it's " + thing + "!";
}
...
blindMode("bird", "plane", "Superman"); // "Is it a bird? Is it a plane? No, it's Superman!"
blindMode("zombie", "mummy", "your reflection"); // "Is it a zombie? Is it a monster? No, it's your reflection!"
```

In Python, we similarly use the same syntax as with variables:

```python
def blind_mode(attempt1, attempt2, thing):
  return "Is it a ", attempt1, "? Is it a ", attempt2, "? No, it's ", thing, "!"
...
print(blind_mode("bird", "plane", "Superman")); # "Is it a bird? Is it a plane? No, it's Superman!"
print(blind_mode("zombie", "mummy", "your reflection")); # // "Is it a zombie? Is it a monster? No, it's Superman!"
```

# Local variables in a subroutine

When a variable is declared inside of a subroutine, it is known as a **local variable** and has the following properies:

* It only exists inside the subroutine.
* It can only be accessed from the subroutine.

In Java, if a class field has `static` before it, it is *not* a local variable.

```java
static int count(String text) {
  int c = 0; // c is a local variable
  for(int i = 0; i < text.length(); i++) // i is a local variable
    c++; // never ever actually do this
  return c;
}
```


# Global variables

When a variable is declared outside of a subroutine, it is known as a **global variable** and has the following properties:

* It exists throughout the entire program.
* It can be accessed from any part of the program.

In Java, any class field preceded by a `static` is a global variable:

```java
class Thing {
  static int count;

  void run() {
    count++; // add one to count
  }
  static void runTwo() {
    count++; // add one to count
  }
  static void main() {
    run();
    runTwo();
    System.out.println(count); // 2
  }
}
```
