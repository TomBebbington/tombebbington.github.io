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
final int DUCKS = 200;
```

  * an **assignment** is for when you want to set a variable or field to a value.

```java
howMany = 4;
```

  * **iteration** is the constant repetition of certain parts of a program . If it is **definite iteration**, then it will be ran a set number of times. If it is **indefinite iteration** then it is ran until a certain condition is met.

```java
for(int i = 0; i < 20; i++)
    System.out.println(i);
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

  * a **function** is a bit of code with a purpose that returns a specific data type.

```java
public static int add(int a, int b) {
    return a + b;
}
```

**Operations** are kinds of expressions you can run on one or more of the same data type.

**Arithmetic operations** are those that are done on numbers, and the following are basic examples:

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

  * **rounding** is used when you only want a certain degree of accuracy.

```java
Math.round(x / y) * y
```

  * **truncation** is used when you don't want the decimal part of a real value.

The following relational operations exist:

  * The **equal to** operator (==) checks if two values are the same. If the value is an object, this checks that it is the same instance of the object.
  * The **not equal to** operator (!=) checks if two values are not the same. If the value is an object, this checks that it isn't the same instance of the object.
  * The **less than** (<) operator checks if one value is lesser than the other, but does not allow them to be equal.
  * The **less than or equal to** (<=) operator checks if one value is lesser than or equal to the other.
  * The **greater**** than**** **(>) operator checks if one value is greater than the other, but does not allow them to be equal.
  * The **greater than or equal to** (>=) operator checks if one value is greater than or equal to the other.

The following boolean operations exist:

  * The **NOT** operation (!) returns the inverse of the value given.
  * The **AND** operation (&&) returns true if both values are true.
  * The **OR** operation (||) returns true if at least one of the values is true.
  * The **XOR** operation (^) returns true if just one of the values is true.
