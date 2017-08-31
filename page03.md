# 3 - 文件组织
一个文件由被空行分割而成的段落以及标识每个段落的可选注释共同组成。

超过2000行的程序难以阅读，应该尽量避免。

正确编码格式的范例，见 ["Java 源文件案例"](page11.md).

## 3.1 Java 源文件
每个 Java 源文件都包含一个单一的公共类或接口。若私有类和接口与一个公共类相关联，可以将它们和公共类放入同一个源文件。公共类必须是这个文件中的第一个类或接口。

Java 源文件还遵循以下规则：

- 开头注释
- 包和引入语句
- 类和接口声明 

### 3.1.1 开头注释
所有的源文件都应该在开头有一个C语言风格的注释，其中列出类名、版本信息、日期和版权声明:

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

### 3.1.2 包和引入语句

在多数 Java 源文件中，第一个非注释行是 `package` 语句。在它之后可以跟 `import` 语句。例如 :

```java
package java.awt;  
   
import java.awt.peer.CanvasPeer;
```


### 3.1.3 类和接口声明

下表描述了类和接口声明的各个部分以及它们出现的先后次序。见 ["Java 源文件案例"](page11.md) 一个包含注释的例子.

class/interface 声明的各个部分 | 注解
------------------------------------|-------
class/interface 文档注释 (`/**...*/`) | 详见 ["文档注释"](page05.md)
`class`或`interface` 声明 | 
class/interface 实现注释 (`/*...*/`)，如果有必要的话 | 该注释应包含任何有关整个类或接口的信息，而这些信息又不适合作为 class/interface 文档注释。
class (`static`) 变量 | 先是 `public` class 变量，接着是 `protected`，再是包级别 (没有访问修饰符)，再是 `private`。
实例变量 | 先是 `public` class 变量，接着是 `protected`，再是包级别 (没有访问修饰符)， 再是 `private`。
构造器 |
方法 | 这些方法应该按功能，而非作用域或访问权限分组。例如，一个私有的类方法可以置于两个公有的实例方法之间，其目的是为了更便于阅读和理解代码。


[PREVIOUS](page02.md) | [CONTENTS](SUMMARY.md) | [NEXT](page04.md)
