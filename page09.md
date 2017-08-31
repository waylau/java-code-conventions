# 9 - 命名规范
命名规范使程序更易读，从而更易于理解。它们也可以提供一些有关标识符功能的信息，以助于理解代码，例如，不论它是一个常量，包，还是类

标识符类型 | 命名规则 | 示例
----------|---------|---------
包(Packages) | 一个唯一包名的前缀总是全部小写的ASCII字母并且是一个顶级域名，通常是com，edu，gov，mil，net，org，或1981年ISO 3166标准所指定的标识国家的英文双字符代码。包名的后续部分根据不同机构各自内部的命名规范而不尽相同。这类命名规范可能以特定目录名的组成来区分部门(department)，项目(project)，机器(machine)，或注册名(login names)。 | `com.sun.eng` `com.apple.quicktime.v2` `edu.cmu.cs.bovik.cheese`
类(Classes)	 | 命名规则：类名是个一名词，采用大小写混合的方式，每个单词的首字母大写。尽量使你的类名简洁而富于描述。使用完整单词，避免缩写词(除非该缩写词被更广泛使用，像URL，HTML) | `class Raster` `class ImageSprite`
接口(Interfaces) | 命名规则：大小写规则与类名相似 | `interface RasterDelegate` `interface Storing`
方法(Methods)	 | 方法名是一个动词，采用大小写混合的方式，第一个单词的首字母小写，其后单词的首字母大写。 | 	`run()` `runFast()` `getBackground()`
变量(Variables)	 | 除了变量名外，所有实例，包括类，类常量，均采用大小写混合的方式，第一个单词的首字母小写，其后单词的首字母大写。变量名不应以下划线或美元符号开头，尽管这在语法上是允许的。变量名应简短且富于描述。变量名的选用应该易于记忆，即，能够指出其用途。尽量避免单个字符的变量名，除非是一次性的临时变量。临时变量通常被取名为`i`，`j`，`k`，`m`和`n`，它们一般用于整型；`c`，`d`，`e`，它们一般用于字符型。 | 	`char c` `int i` `float myWidth`
实例变量(Instance Variables)	 | 大小写规则和变量名相似，除了前面需要一个下划线	 | `int _employeeId` `String _name` `Customer _customer`
常量(Constants)	 | 类常量和ANSI常量的声明，应该全部大写，单词间用下划线隔开。(尽量避免ANSI常量，容易引起错误)	 | `static final int MIN_WIDTH = 4` `static final int MAX_WIDTH = 999` `static final int GET_THE_CPU = 1`


[PREVIOUS](page08.md) | [CONTENTS](SUMMARY.md) | [NEXT](page10.md)
