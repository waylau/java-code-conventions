##5 - 注释
Java 有两类注释: implementation comments（实现注释）和 documentation comments（文档注释）。 实现注释常见于 C++,使用 `/*...*/`,和 `//`。文档注释 (也称为"doc comments") 是 Java 独有的,使用 `/**...*/`。文档注释可以通过 javadoc 工具转成 HTML 文件。

实现注释用以注释代码或者特殊的实现。 文档注释从 implementation-free (实现自由)的角度描述代码的规范。它可以被那些手头没有源码的开发人员读懂。

注释应被用来给出代码的总览，并提供代码自身没有提供的附加信息。注释应该仅包含与阅读和理解程序有关的信息。例如，相应的包如何被建立或位于哪个目录下之类的信息不应包括在注释中。

在注释里，对设计决策中重要的或者不是显而易见的地方进行说明是可以的，但应避免提供代码中己清晰表达出来的重复信息。多余的的注释很容易过时。通常应避免那些代码更新就可能过时的注释。

**注意:** 频繁的注释有时反映出代码的低质量。当你觉得被迫要加注释的时候，考虑一下重写代码使其更清晰。

注释不应写在用星号或其他字符画出来的大框里。

注释不应包括诸如制表符和回退符之类的特殊字符。

###5.1 实现注释的格式
实现注释的格式主要有4种: block（块）, single-line（单行）, trailing（尾端）, 和 end-of-line（行末）.

####5.1.1 块注释
块注释通常用于提供对文件，方法，数据结构和算法的描述。块注释被置于每个文件的开始处以及每个方法之前。它们也可以被用于其他地方，比如方法内部。在功能和方法内部的块注释应该和它们所描述的代码具有一样的缩进格式。

块注释之首应该有一个空行，用于把块注释和代码分割开来，比如：

```java

	/*
	 * Here is a block comment.
	 */

```

```java

	/*-indent
	
	<blockquote>/*-
	 * Here is a block comment with some very special
	 * formatting that I want indent(1) to ignore.
	 *
	 *    one
	 *        two
	 *            three
	 */

```

**Note:`/*-indent`** 详见于 5.2 节 "Documentation Comments"

####5.1.2 单行注释
短注释可以显示在一行内，并与其后的代码具有一样的缩进层级。如果一个注释不能在一行内写完，就该采用块注释(参见"5.1.1 块注释")。单行注释之前应该有一个空行。以下是一个 Java 代码中单行注释的例子：:

```java

	if (condition) {

	    /* Handle the condition. */
	    ...
	}

```

####5.1.3 尾端注释
极短的注释可以与它们所要描述的代码位于同一行，但是应该有足够的空白来分开代码和注释。若有多个短注释出现于大段代码中，它们应该具有相同的缩进。

以下是一个Java代码中尾端注释的例子：

```java

	if (a == 2) {
	    return TRUE;            /* special case */
	} else {
	    return isPrime(a);      /* works only for odd a */
	}

```

####5.1.4 行末注释
注释界定符 `//` ，可以注释掉整行或者一行中的一部分。它一般不用于连续多行的注释文本；然而，它可以用来注释掉连续多行的代码段。以下是所有三种风格的例子：

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

####5.2 文档注释
注意：此处描述的注释格式之范例，参见["Java 源文件范例"](page11.md)。

更多细节，详见"How to Write Doc Comments for Javadoc"，里面包含了文档注释标签的信息(@return, @param, @see): 

[链接](http://www.oracle.com/technetwork/java/javase/documentation/index-137868.html)

更多关于文档注释和 javadoc，详见 javadoc 主页

[这里](http://www.oracle.com/technetwork/java/javase/documentation/codeconventions-141999.html#)

文档注释描述Java的类、接口、构造器，方法，以及字段(field)。每个文档注释都会被置于注释定界符 `/**...*/`之中，一个注释对应一个类、接口或成员。该注释应位于声明之前：

```java

	/**
	 * The Example class provides ...
	 */
	public class Example { ...

```

注意顶层(top-level)的类和接口是不缩进的，而其成员是缩进的。描述类和接口的文档注释的第一行(`/**`)不需缩进；随后的文档注释每行都缩进1格(使星号纵向对齐)。成员，包括构造函数在内，其文档注释的第一行缩进4格，随后每行都缩进5格。

若你想给出有关类、接口、变量或方法的信息，而这些信息又不适合写在文档中，则可使用实现块注释(见5.1.1)或紧跟在声明后面的单行注释(见5.1.2)。例如，有关一个类实现的细节，应放入紧跟在类声明后面的实现块注释中，而不是放在文档注释中。

文档注释不能放在一个方法或构造器的定义块中，因为Java会将位于文档注释之后的第一个声明与其相关联。



[PREVIOUS](page04.md) | [CONTENTS](SUMMARY.md) | [NEXT](page06.md)
