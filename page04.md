##4 - 缩进
4个空格常被作为缩进排版的一个单位。缩进的确切解释并未详细指定 (使用空格 还是 tab) . Tab 一定要设置为8个空格 (而非4个)。

###4.1 行长度
尽量避免一行的长度超过80个字符，因为很多终端和工具不能很好处理之。

**注意:** 用于文档中的例子应该使用更短的行长，长度一般不超过70个字符。

###4.2 换行
当一个表达式无法容纳在一行内时，可以依据如下一般规则断开:

- 在一个逗号后面断开
- 在一个操作符前面断开
- 宁可选择较高级别(higher-level)的断开，而非较低级别(lower-level)的断开
- 新的一行应该与上一行同一级别表达式的开头处对齐
- 如果以上规则导致你的代码混乱或者使你的代码都堆挤在右边，那就代之以缩进8个空格。

以下是断开方法调用的一些例子:

```java

	someMethod(longExpression1, longExpression2, longExpression3, 
	           longExpression4, longExpression5);
	 
	var = someMethod1(longExpression1,
	                  someMethod2(longExpression2,
	                              longExpression3));

```

以下是两个断开算术表达式的例子。前者更好，因为断开处位于括号表达式的外边，这是个较高级别的断开。

```java

	longName1 = longName2 * (longName3 + longName4 - longName5)
	            + 4 * longname6; // 推荐
	
	longName1 = longName2 * (longName3 + longName4
	                         - longName5) + 4 * longname6; // 避免 
	                         
```

以下是两个缩进方法声明的例子。前者是常规情形。后者如果按照常规的缩进方法就会使得第二行和第三行太靠右边，所以只缩进8个字符。

```java

	//常规缩进
	someMethod(int anArg, Object anotherArg, String yetAnotherArg,
	           Object andStillAnother) {
	    ...
	}
	
	//缩进8个空格来避免缩进的太深
	private static synchronized horkingLongMethodName(int anArg,
	        Object anotherArg, String yetAnotherArg,
	        Object andStillAnother) {
	    ...
	}

```

if语句的换行通常使用8个空格的规则，因为常规缩进(4个空格)会使语句体看起来比较费劲。比如:

```java

	//不要使用这种
	if ((condition1 && condition2)
	    || (condition3 && condition4)
	    ||!(condition5 && condition6)) { //BAD WRAPS
	    doSomethingAboutIt();            //MAKE THIS LINE EASY TO MISS
	} 
	
	//用这个来代替
	if ((condition1 && condition2)
	        || (condition3 && condition4)
	        ||!(condition5 && condition6)) {
	    doSomethingAboutIt();
	} 
	
	//或用这种
	if ((condition1 && condition2) || (condition3 && condition4)
	        ||!(condition5 && condition6)) {
	    doSomethingAboutIt();
	}

```

这里有三种可行的方法用于处理三元运算表达式:

```java

	alpha = (aLongBooleanExpression) ? beta : gamma;  
	
	alpha = (aLongBooleanExpression) ? beta
	                                 : gamma;  
	
	alpha = (aLongBooleanExpression)
	        ? beta 
	        : gamma;

```



[PREVIOUS](page03.md) | [CONTENTS](SUMMARY.md) | [NEXT](page05.md)
