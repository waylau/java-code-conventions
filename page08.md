##8 - White Space
###8.1 Blank Lines
Blank lines improve readability by setting off sections of code that are logically related.

Two blank lines should always be used in the following circumstances:

- Between sections of a source file
- Between class and interface definitions

One blank line should always be used in the following circumstances:

- Between methods
- Between the local variables in a method and its first statement
- Before a block (see [section 5.1.1](page05.md#511-block-comments)) or single-line (see [section 5.1.2](page05.md#512-single-line-comments)) comment
- Between logical sections inside a method to improve readability

###8.2 Blank Spaces
Blank spaces should be used in the following circumstances:

- A keyword followed by a parenthesis should be separated by a space. Example:

```java
while (true) {
    ...
}
```

Note that a blank space should not be used between a method name and its opening parenthesis. This helps to distinguish keywords from method calls.

- A blank space should appear after commas in argument lists.
- All binary operators except . should be separated from their operands by spaces. Blank spaces should never separate unary operators such as unary minus, increment (`++`), and decrement (`--`) from their operands. Example:

```java
a += c + d;
a = (a + b) / (c * d);
    
while (d++ = s++) {
    n++;
}
printSize("size is " + foo + "\n");
```

- The expressions in a `for` statement should be separated by blank spaces. Example:
```java
for (expr1; expr2; expr3)
```

- Casts should be followed by a blank space. Examples:

```java
myMethod((byte) aNum, (Object) x);
myMethod((int) (cp + 5), ((int) (i + 3)) + 1);
```
[CONTENTS](TOC.md)

[PREVIOUS](page07.md) [NEXT](page09.md)
