##3 - File Organization
A file consists of sections that should be separated by blank lines and an optional comment identifying each section.

Files longer than 2000 lines are cumbersome and should be avoided.

For an example of a Java program properly formatted, see ["Java Source File Example"](page11.md#111-java-source-file-example).

###3.1 Java Source Files
Each Java source file contains a single public class or interface. When private classes and interfaces are associated with a public class, you can put them in the same source file as the public class. The public class should be the first class or interface in the file.

Java source files have the following ordering:

- Beginning comments (see ["Beginning Comments"](#311-beginning-comments))
- Package and Import statements
- Class and interface declarations (see ["Class and Interface Declarations"](#313-class-and-interface-declarations))

###3.1.1 Beginning Comments
All source files should begin with a c-style comment that lists the class name, version information, date, and copyright notice:

```java
/*
 * Classname
 * 
 * Version information
 *
 * Date
 * 
 * Copyright notice
 */
```

###3.1.2 Package and Import Statements
The first non-comment line of most Java source files is a `package` statement. After that, `import` statements can follow. For example:

```java
package java.awt;

import java.awt.peer.CanvasPeer;
```  

###3.1.3 Class and Interface Declarations
The following table describes the parts of a class or interface declaration, in the order that they should appear. See ["Java Source File Example"](page11.md#111-java-source-file-example) for an example that includes comments.

Part of class/interface declaration | Notes
------------------------------------|-------
Class/interface documentation comment (`/**...*/`) | See ["Documentation Comments"](page05.md#52-documentation-comments) for information on what should be in this comment.
`class` or `interface` statement | 
Class/interface implementation comment (`/*...*/`), if necessary | This comment should contain any class-wide or interface-wide information that wasn't appropriate for the class/interface documentation comment.
Class (`static`) variables | First the `public` class variables, then the `protected`, then package level (no access modifier), and then the `private`.
Instance variables | First the `public` class variables, then the `protected`, then package level (no access modifier), and then the `private`.
Constructors |
Methods | These methods should be grouped by functionality rather than by scope or accessibility. For example, a private class method can be in between two public instance methods. The goal is to make reading and understanding the code easier.

[CONTENTS](TOC.md)

[PREVIOUS](page02.md) [NEXT](page04.md)
