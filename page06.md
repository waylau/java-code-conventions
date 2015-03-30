##6 - Declarations
###6.1 Number Per Line
One declaration per line is recommended since it encourages commenting. In other words,

```java
int level; // indentation level
int size;  // size of table
```

is preferred over

```java
int level, size;
```

Do not put different types on the same line. Example:

```java
int foo,  fooarray[]; //WRONG!
```

**Note:** The examples above use one space between the type and the identifier. Another acceptable alternative is to use tabs, e.g.:

```java
int     level;          // indentation level
int     size;           // size of table
Object  currentEntry;   // currently selected table entry
```

###6.2 Initialization
Try to initialize local variables where they're declared. The only reason not to initialize a variable where it's declared is if the initial value depends on some computation occurring first.

###6.3 Placement
Put declarations only at the beginning of blocks. (A block is any code surrounded by curly braces `{` and `}`.) Don't wait to declare variables until their first use; it can confuse the unwary programmer and hamper code portability within the scope.

```java
void myMethod() {
    int int1 = 0;         // beginning of method block

    if (condition) {
        int int2 = 0;     // beginning of "if" block
        ...
    }
}
```

The one exception to the rule is indexes of for loops, which in Java can be declared in the for statement:

```java
for (int i = 0; i < maxLoops; i++) { ... }
```

Avoid local declarations that hide declarations at higher levels. For example, do not declare the same variable name in an inner block:

```java
int count;
...
myMethod() {
    if (condition) {
        int count = 0;     // AVOID!
        ...
    }
    ...
}
```

###6.4 Class and Interface Declarations
When coding Java classes and interfaces, the following formatting rules should be followed:

- No space between a method name and the parenthesis `(` starting its parameter list
- Open brace `{` appears at the end of the same line as the declaration statement
- Closing brace `}` starts a line by itself indented to match its corresponding opening statement, except when it is a null statement the `}` should appear immediately after the `{`

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

- Methods are separated by a blank line

[CONTENTS](TOC.md)

[PREVIOUS](page05.md) [NEXT](page07.md)
