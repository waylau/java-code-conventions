##7 - Statements
###7.1 Simple Statements
Each line should contain at most one statement. Example:

```java
argv++;         // Correct
argc--;         // Correct  
argv++; argc--; // AVOID!
```

Do not use the comma operator to group multiple statements unless it is for an obvious reason.
Example:

```java
if (err) {
    Format.print(System.out, "error"), exit(1); //VERY WRONG!
}
```

###7.2 Compound Statements
Compound statements are statements that contain lists of statements enclosed in braces `{ statements }`. See the following sections for examples.

- The enclosed statements should be indented one more level than the compound statement.
- The opening brace should be at the end of the line that begins the compound statement; the closing brace should begin a line and be indented to the beginning of the compound statement.
- Braces are used around all statements, even single statements, when they are part of a control structure, such as an `if-else` or `for` statement. This makes it easier to add statements without accidentally introducing bugs due to forgetting to add braces.

###7.3 return Statements
A `return` statement with a value should not use parentheses unless they make the return value more obvious in some way. Example:

```java
return;

return myDisk.size();

return (size ? size : defaultSize);
```

###7.4 if, if-else, if else-if else Statements
The `if-else` class of statements should have the following form:

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

**Note:** `if` statements always use braces, `{}`. Avoid the following error-prone form:

```java
if (condition) //AVOID! THIS OMITS THE BRACES {}!
    statement;
```
###7.5 for Statements
A ```for``` statement should have the following form:

```java
for (initialization; condition; update) {
    statements;
}
```

An empty `for` statement (one in which all the work is done in the initialization, condition, and update clauses) should have the following form:

```java
for (initialization; condition; update);
```

When using the comma operator in the initialization or update clause of a `for` statement, avoid the complexity of using more than three variables. If needed, use separate statements before the `for` loop (for the initialization clause) or at the end of the loop (for the update clause).

###7.6 while Statements
A `while` statement should have the following form:

```java
while (condition) {
    statements;
}
```

An empty `while` statement should have the following form:

```java
while (condition);
```

###7.7 do-while Statements
A `do-while` statement should have the following form:

```java
do {
    statements;
} while (condition);
```

###7.8 switch Statements
A `switch` statement should have the following form:

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

Every time a case falls through (doesn't include a `break` statement), add a comment where the `break` statement would normally be. This is shown in the preceding code example with the `/* falls through */` comment.

Every `switch` statement should include a default case. The `break` in the default case is redundant, but it prevents a fall-through error if later another `case` is added.

###7.9 try-catch Statements
A `try-catch` statement should have the following format:

```java
try {
    statements;
} catch (ExceptionClass e) {
     statements;
}
```

A `try-catch` statement may also be followed by `finally`, which executes regardless of whether or not the `try` block has completed successfully.

```java
try {
    statements;
} catch (ExceptionClass e) {
    statements;
} finally {
    statements;
}
```

[CONTENTS](TOC.md)

[PREVIOUS](page06.md) [NEXT](page08.md)
