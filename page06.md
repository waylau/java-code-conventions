# 6 - 声明
## 6.1 每行声明变量的数量
推荐一行一个声明，因为这样以利于写注释。即,

```java

	int level; // indentation level
	int size;  // size of table

```

要优于

```java

	int level, size;

```

不要将不同类型变量的声明放在同一行，例如:

```java

	int foo,  fooarray[]; // 错误!

```

**注意:** 上面的例子中，在类型和标识符之间放了一个空格，另一种被允许的替代方式是使用制表符:

```java

	int     level;          // indentation level
	int     size;           // size of table
	Object  currentEntry;   // currently selected table entry

```

## 6.2 初始化
尽量在声明局部变量的同时初始化。唯一不这么做的理由是变量的初始值依赖于某些先前发生的计算。

## 6.3 布局
只在代码块的开始处声明变量。（一个块是指任何被包含在大括号`{` 和 `}`中间的代码。）不要在首次用到该变量时才声明之。这会把注意力不集中的程序员搞糊涂，同时会妨碍代码在该作用域内的可移植性。

```java

	void myMethod() {
	    int int1 = 0;         // beginning of method block
	
	    if (condition) {
	        int int2 = 0;     // beginning of "if" block
	        ...
	    }
	}

```

该规则的一个例外是for循环的索引变量:

```java

	for (int i = 0; i < maxLoops; i++) { ... }

```

避免声明的局部变量覆盖上一级声明的变量。例如，不要在内部代码块中声明相同的变量名:

```java

	int count;
	...
	myMethod() {
	    if (condition) {
	        int count = 0;     // 避免!
	        ...
	    }
	    ...
	}

```

## 6.4 类和接口的声明
当编写类和接口是，应该遵守以下格式规则：

- 在方法名与其参数列表之前的左括号`(`间不要有空格
- 左大括号`{`位于声明语句同行的末尾
- 右大括号`}`另起一行，与相应的声明语句对齐，除非是一个空语句，`}`应紧跟在`{`之后

```java

	class Sample extends Object {
	    int ivar1;
	    int ivar2;
	
	    Sample(int i, int j) {
	        ivar1 = i;
	        ivar2 = j;
	    }
	
	    int emptyMethod() {}
	
	    ...
	}

```

- 方法与方法之间以空行分隔


[PREVIOUS](page05.md) | [CONTENTS](SUMMARY.md) | [NEXT](page07.md)
