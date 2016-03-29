---
published: true
code: 1
title: Data structures and abstract data types
layout: post
category: computing
tags: CS3.2
summary: "Data structures store data in an organised yet accessible format, lending themselved to different contexts."
---


A **data structure** is a way of storing data in an organised but accessible format, and typically different data structures lend themselves to different contexts.

An **abstract data type** is a purely conceptual model of how this data is stored and operations that be done on them.

# Arrays
An **array** is a sequential list of data, where each item of data is called an **element**. These can have more than one dimension e.g. for a 2D image, you would use a two-dimension array to store the pixel values. In Java, we use the syntax:

```java
// when you have values to assign
int[] ages = {6, 7, 3, 23};
float[] weights = {60.5, 23.1, 223.4, 40.2};

// when you just want zeroes
int[][] pixels = new int[640][480];
```

In this example, `ages` is an array of `int`s because that is the type before the `[]` which indicate that the type is an array. Similarly, `weights` is an array of `float`s, and `pixels` is an array of `int[]`s.

# Files
Files are split into two categories: **binary** and **text** files.

## Binary files
These start with a bit sequence known as a **header** which indicate what kind of file this is, and only consist of bits. Some common formats are:

* JPEG, PNG and BMP files for storing images.
* ZIP files for compressing files.

### Reading from a binary file
In Java, we use the `DataInputStream` class to read binary data from a file:

```java
try {
    DataInputStream output = new DataInputStream(new FileInputStream("numbers.dat"));
    System.out.println(input.readUTF());
    System.out.println("answer to life = " + input.readInt());
    System.out.println("pi = " + input.readFloat());
    input.close();
} catch(FileNotFound ex) {
    System.err.println("Failed to open file");
}
```

### Writing to a binary file
In Java, we use the `DataOutputStream` class to write binary data to a file:

```java
try {
    DataOutputStream output = new DataOutputStream(new FileOutputStream("numbers.dat"));
    output.writeUTF("Hello, world!");
    output.writeInt(42);
    output.writeFloat(3.1415);
    output.close();
} catch(IOException ex) {
    System.err.println("Failed to open file");
}
```

## Text files
These may have a header, to indicate the file's structure, and an End-Of-File marker so the program can know when to stop reading in from the file.
This is a file that consists of lines of text, with a given encoding (usually UTF-8). Each line is known as a **record**. Some common formats are:

* HTML files for detailing the contents of a web page.
* CSV files for storing databases and tables. Each value between commas is known as a **field**.
* TXT files for storing plain text.

### Reading from a text file
In Java, we use the `Scanner` class combined with the `File` class to read textual data from a file:

```java
try {
    Scanner scanner = new Scanner(new File("greetings.txt"));
    ArrayList<String> greetings = new ArrayList();
    while(scanner.hasNext())
        greetings.add(scanner.next());
    scanner.close();
} catch(FileNotFoundException ex) {
    System.err.println("Failed to open file");
}
```

### Writing to a text file
In Java, we use the `FileWriter` class to write textual data to a file:

```java
try {
    FileWriter writer = new FileWriter("greetings.txt");
    writer.write("Hello\n");
    writer.write("Hola\n");
    writer.write("Bonjour\n");
    writer.write("Ohio\n");
    writer.close();
} catch(IOException ex) {
    System.err.println("Failed to open file");
}
```
