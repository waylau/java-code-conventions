##5 - Comments
Java programs can have two kinds of comments: implementation comments and documentation comments. Implementation comments are those found in C++, which are delimited by `/*...*/`, and `//`. Documentation comments (known as "doc comments") are Java-only, and are delimited by `/**...*/`. Doc comments can be extracted to HTML files using the javadoc tool.

Implementation comments are meant for commenting out code or for comments about the particular implementation. Doc comments are meant to describe the specification of the code, from an implementation-free perspective. to be read by developers who might not necessarily have the source code at hand.

Comments should be used to give overviews of code and provide additional information that is not readily available in the code itself. Comments should contain only information that is relevant to reading and understanding the program. For example, information about how the corresponding package is built or in what directory it resides should not be included as a comment.

Discussion of nontrivial or nonobvious design decisions is appropriate, but avoid duplicating information that is present in (and clear from) the code. It is too easy for redundant comments to get out of date. In general, avoid any comments that are likely to get out of date as the code evolves.

**Note:** The frequency of comments sometimes reflects poor quality of code. When you feel compelled to add a comment, consider rewriting the code to make it clearer.

Comments should not be enclosed in large boxes drawn with asterisks or other characters.

Comments should never include special characters such as form-feed and backspace.

###5.1 Implementation Comment Formats
Programs can have four styles of implementation comments: block, single-line, trailing, and end-of-line.

####5.1.1 Block Comments
Block comments are used to provide descriptions of files, methods, data structures and algorithms. Block comments may be used at the beginning of each file and before each method. They can also be used in other places, such as within methods. Block comments inside a function or method should be indented to the same level as the code they describe.

A block comment should be preceded by a blank line to set it apart from the rest of the code.

```java
/*
 * Here is a block comment.
 */
```

```java
/*
 * Here is a block comment with some very special
 * formatting that I want indent(1) to ignore.
 *
 *    one
 *        two
 *            three
 */
```

**Note:** See also ["Documentation Comments"](#52-documentation-comments).

####5.1.2 Single-Line Comments
Short comments can appear on a single line indented to the level of the code that follows. If a comment can't be written in a single line, it should follow the block comment format (see [section 5.1.1](#511-block-comments)). A single-line comment should be preceded by a blank line. Here's an example of a single-line comment in Java code (also see ["Documentation Comments"](#52-documentation-comments)):

```java
if (condition) {
    /* Handle the condition. */
    ...
}
```

####5.1.3 Trailing Comments
Very short comments can appear on the same line as the code they describe, but should be shifted far enough to separate them from the statements. If more than one short comment appears in a chunk of code, they should all be indented to the same tab setting.

Here's an example of a trailing comment in Java code:

```java
if (a == 2) {
    return true;            /* special case */
} else {
    return isPrime(a);      /* works only for odd a */
}
```

####5.1.4 End-Of-Line Comments
The `//` comment delimiter can comment out a complete line or only a partial line. It shouldn't be used on consecutive multiple lines for text comments; however, it can be used in consecutive multiple lines for commenting out sections of code. Examples of all three styles follow:

```java
if (foo > 1) {
    // Do a double-flip.
    ...
}
else
    return false;          // Explain why here.

//if (bar > 1) {
//
//    // Do a triple-flip.
//    ...
//}
//else
//    return false;
```

####5.2 Documentation Comments
Note: See ["Java Source File Example"](page11.md#111-java-source-file-example) for examples of the comment formats described here.

For further details, see "How to Write Doc Comments for Javadoc" which includes information on the doc comment tags (@return, @param, @see): [link](http://www.oracle.com/technetwork/java/javase/documentation/index-137868.html)

Doc comments describe Java classes, interfaces, constructors, methods, and fields. Each doc comment is set inside the comment delimiters `/**...*/`, with one comment per class, interface, or member. This comment should appear just before the declaration:

```java
/**
 * The Example class provides ...
 */
public class Example { ...
```

Notice that top-level classes and interfaces are not indented, while their members are. The first line of doc comment (`/**`) for classes and interfaces is not indented; subsequent doc comment lines each have 1 space of indentation (to vertically align the asterisks). Members, including constructors, have 4 spaces for the first doc comment line and 5 spaces thereafter.

If you need to give information about a class, interface, variable, or method that isn't appropriate for documentation, use an implementation block comment (see [section 5.1.1](#511-block-comments)) or single-line (see [section 5.1.2](#512-single-line-comments)) comment immediately *after* the declaration. For example, details about the implementation of a class should go in in such an implementation block comment *following* the class statement, not in the class doc comment.

Doc comments should not be positioned inside a method or constructor definition block, because Java associates documentation comments with the first declaration *after* the comment.

[CONTENTS](TOC.md)

[PREVIOUS](page04.md) [NEXT](page06.md)
