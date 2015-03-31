##7 - 语句
###7.1 简单语句
每行至多包含一条语句，例如:

```java

	argv++;         // 正确
	argc--;         // 正确  
	argv++; argc--; // 避免!

```
###7.2 复合语句
复合语句是包含在大括号中的语句序列，形如`{ statements }`。例如下面各段。

- 被括其中的语句应该较之复合语句缩进一个层次
- 左大括号"{"应位于复合语句起始行的行尾；右大括号"}"应另起一行并与复合语句首行对齐。
- 大括号可以被用于所有语句，包括单个语句，只要这些语句是诸如 `if-else` 或 `for`控制结构的一部分。这样便于添加语句而无需担心由于忘了加括号而引入bug。

###7.3 return 语句
一个带返回值的`return`语句不使用小括号"()"，除非它们以某种方式使返回值更为显见。例如:

```java
	
	return;
	
	return myDisk.size();
	
	return (size ? size : defaultSize);

```

###7.4 if, if-else, if else-if else 语句
`if-else`语句应该是以下形式:

```java

	if (condition) {
	    statements;
	}
	
	if (condition) {
	    statements;
	} else {
	    statements;
	}
	
	if (condition) {
	    statements;
	} else if (condition) {
	    statements;
	} else {
	    statements;
	}

```

**注意:** `if`语句通常使用`{}`。避免下面容易出错的形式:

```java

	if (condition) // 避免！这省略了括号{ }！
	    statement;

```

###7.5 for 语句
`for` 语句应该是如下形式:

```java

	for (initialization; condition; update) {
	    statements;
	}

```

空的`for`语句 (所有工作都在初始化，条件判断，更新子句中完成) 应该是如下形式:

```java

	for (initialization; condition; update);

```

当在for语句的初始化或更新子句中使用逗号时，避免因使用三个以上变量，而导致复杂度提高。若需要，可以在`for`循环之前(为初始化子句)或`for`循环末尾(为更新子句)使用单独的语句。

###7.6 while 语句
`while` 语句应该是如下形式:

```java

	while (condition) {
	    statements;
	}

```

空的 `while` 语句应该是如下形式:

```java

	while (condition);

```

###7.7 do-while 语句
`do-while` 语句应该是如下形式:

```java

	do {
	    statements;
	} while (condition);

```

###7.8 switch 语句
`switch` 语句应该是如下形式:

```java

	switch (condition) {
	case ABC:
	    statements;
	    /* falls through */
	case DEF:
	    statements;
	    break;
	case XYZ:
	    statements;
	    break;
	default:
	    statements;
	    break;
	}

```

每当一个case顺着往下执行时(因为没有`break`语句)，通常应在`break`语句的位置添加注释。上面的示例代码中就包含注释`/* falls through */`。

Every `switch` statement should include a default case. The `break` in the default case is redundant, but it prevents a fall-through error if later another `case` is added.

###7.9 try-catch 语句
`try-catch` 语句应该是如下格式:

```java

	try {
	    statements;
	} catch (ExceptionClass e) {
	     statements;
	}

```

一个`try-catch`语句后面也可能跟着一个`finally`语句，不论`try`代码块是否顺利执行完，它都会被执行。

```java

	try {
	    statements;
	} catch (ExceptionClass e) {
	    statements;
	} finally {
	    statements;
	}

```


[PREVIOUS](page06.md) | [CONTENTS](SUMMARY.md) | [NEXT](page08.md)
