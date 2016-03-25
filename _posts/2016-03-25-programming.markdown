---
title: 3.1.1 - Programming
layout: post
category: computing
tags: CS3.1
layout: post
---

# Data types
A **data type** is what variables' types are classed as. The following are the fundamental, built-in data types:

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
  * An **object** is an instance of a class that can have its methods called.
  * A **class** is a description of an object and some static variables and methods.
  * An **enum** is an enumeration of values i.e. can be one of a fixed number of values, that all have different meanings.

# Programming concepts
The following kinds of statements can be used in Java:

  * a **variable declaration** is for when you want to give a name to a value or change the value easily. i.e.:

```java
int howMany = 3;
```

  * a **constant declaration** is for when you want to give a name to a value that won't (and can't) be changed throughout the program.

```java
static final int DUCKS = 200;
```

  * an **assignment** is for when you want to set a variable or field to a value.

```java
howMany = 4;
```

  * **iteration** is the constant repetition of certain parts of a program . If it is **definite iteration**, then it will be ran a set number of times. If it is **indefinite iteration** then it is ran until a certain condition is met. This is typically done with the `for` loop as it is included in most languages. In Java:

```java
for(int i = 0; i < 20; i++)
    System.out.println(i);
```

In Rust:

```rust
for i in 0...20 {
  println!("{}", i);
}
```

  * a **selection** is used when you want to run different parts of code when a certain value is different values. In Java, we use `switch` statements or `if` statements depending on if it is either an integer or enum, or not.

```java
switch(value) {
    case 12:
        return "Yes, this is 12!";
    case 13:
        return "No, this is 13!";
    default:
        return "Whaaat";
}
```

  * a **subroutine** is a bit of code with a purpose that returns a specific data type. In Java, we use methods for this purpose:

```java
public static int add(int a, int b) {
    return a + b;
}
```

While in Rust, we use functions:

```rust
fn add(a: i32, b: i32) -> i32 {
  a + b
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
These compare two values, yielding a **boolean**:
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
  * The **NOT** operation (!) returns the inverse of the value given.

```java
!x
```

  * The **AND** operation (&&) returns true if both values are true.

```java
x && y
```

  * The **OR** operation (||) returns true if at least one of the values is true.

```java
x || y
```

  * The **XOR** operation (^) returns true if just one of the values is true.

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
text.length()
```
* The position of a substring inside a string can be found by:

```java
text.indexOf("world")
```
* The text between positions in a string can be found by:

```java
text.substring(0, 5);
```

* Strings can be concatenated by:

```java
text + " Hereeee's Johhny"
```
or:

```java
StringBuilder builder = new StringBuilder();
builder.append(text);
builder.append(" Hereeee's Johhny");
builder.toString();
```

* The character at a certain offset of a string can be found by:
```java
text.charAt(5);
```
To convert a character to a character code (from an `int` to a `char` in Java):

```java
(int) 'a';
```

And the inverse:

```java
(char) 30;
```

* A string can be converted to a primitive in Java by using the `Primitive.parsePrimitive` method, where `Primitive` is the boxed version of the primitive. For example:
```java
int a = Integer.parseInt("32");
float b = Float.parseFloat("45.321");
double s = Double.parseDouble("3.14159265");
```

* Similarly, a primitive can be converted to a string in Java by using the `Primitive.toString` method, where `Primitive` is the boxed version of the primitive. For example:

```java
String a = Integer.toString(32);
String b = Float.toString(45.321f);
String s = Double.toString(3.14159265d);
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
  System.out.println(text.length());
} catch(NullPointerException e) {
  System.err.println("Text is null!");
}
```

# Subroutines
A **subroutine** is a block of code that is give a name, and can be called by writing its name with a set of parentheses after it. In Java, we use methods as subroutines:

```java
static void bark() {
  System.out.println("Bark!");
}
...
bark();
```

In Python, we use functions as subroutines:

```python
def bark():
  print "Bark!"
...
bark();
```

# Subroutine parameters

Subroutines can be passed values when they are called and these values can be given names, similarly to variables. These values are called **arguments**, or **parameters**. In Java, we use the same syntax as with variables:

```java
static void blindMode(String attempt1, String attempt2, String thing) {
  System.out.println("Is it a " + attempt1 + "? Is it a " + attempt2 + "? No, it's " + thing + "!");
}
...
blindMode("bird", "plane", "Superman");
blindMode("zombie", "mummy", "your reflection");
```

In Python, we similarly use the same syntax as with variables:

```python
def blind_mode(attempt1, attempt2, thing):
  print "Is it a ", attempt1, "? Is it a ", attempt2, "? No, it's ", thing, "!"
...
blind_mode("bird", "plane", "Superman");
blind_mode("zombie", "mummy", "your reflection");
```

# Returning data from a subroutine
So far, none of  the example subroutines have returned nothing, hence they are classified as procedurers, as they:
* Have a return type of `void`.
* Don't contain a `return` statement.

In Java, we replace the `void` type with the type we want to return and add a `return` statement:

```java
static String blindMode(String attempt1, String attempt2, String thing) {
  return "Is it a " + attempt1 + "? Is it a " + attempt2 + "? No, it's " + thing + "!";
}
...
blindMode("bird", "plane", "Superman");
blindMode("zombie", "mummy", "your reflection");
```

In Python, we similarly use the same syntax as with variables:

```python
def blind_mode(attempt1, attempt2, thing):
  return "Is it a ", attempt1, "? Is it a ", attempt2, "? No, it's ", thing, "!"
...
print(blind_mode("bird", "plane", "Superman"));
print(blind_mode("zombie", "mummy", "your reflection"));
```

# Local variables in a subroutine

When a variable is declared inside of a subroutine, it is known as a **local variable** and has the following properies:
* It only exists inside the subroutine.
* It can only be accessed from the subroutine.

# Global variables

When a variable is declared outside of a subroutine, it is known as a **global variable** and has the following properties:
* It exists throughout the entire program.
* I can be accessed from any part of the program.

In Java, any class field preceded by a `static` is a global variable.