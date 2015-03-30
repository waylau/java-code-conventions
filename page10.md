##10 - Programming Practices
###10.1 Providing Access to Instance and Class Variables
Don't make any instance or class variable public without good reason. Often, instance variables don't need to be explicitly set or gotten-often that happens as a side effect of method calls.

One example of appropriate public instance variables is the case where the class is essentially a data structure, with no behavior. In other words, if you would have used a `struct` instead of a class (if Java supported `struct`), then it's appropriate to make the class's instance variables public.

###10.2 Referring to Class Variables and Methods
Avoid using an object to access a class (`static`) variable or method. Use a class name instead. For example:

```java
classMethod();             //OK
AClass.classMethod();      //OK
anObject.classMethod();    //AVOID!
```

###10.3 Constants
Numerical constants (literals) should not be coded directly, except for `-1`, `0`, and `1`, which can appear in a `for` loop as counter values.

###10.4 Variable Assignments
Avoid assigning several variables to the same value in a single statement. It is hard to read. Example:

```java
fooBar.fChar = barFoo.lchar = 'c'; // AVOID!
```

Do not use the assignment operator in a place where it can be easily confused with the equality operator. Example:

```java
if (c++ = d++) {        // AVOID! (Java disallows)
    ...
}
```

should be written as

```java
if ((c++ = d++) != 0) {
    ...
}
```

Do not use embedded assignments in an attempt to improve run-time performance. This is the job of the compiler. Example:

```java
d = (a = b + c) + r;        // AVOID!
```

should be written as

```java
a = b + c;
d = a + r;
```

###10.5 Miscellaneous Practices
####10.5.1 Parentheses
It is generally a good idea to use parentheses liberally in expressions involving mixed operators to avoid operator precedence problems. Even if the operator precedence seems clear to you, it might not be to others-you shouldn't assume that other programmers know precedence as well as you do.

```java
if (a == b && c == d)     // AVOID!
if ((a == b) && (c == d)) // RIGHT
```

####10.5.2 Returning Values
Try to make the structure of your program match the intent. Example:

```java
if (booleanExpression) {
    return true;
} else {
    return false;
}
```
  
should instead be written as

```java
return booleanExpression;
```

Similarly,

```java
if (condition) {
    return x;
}
return y;
```

should be written as

```java
return (condition ? x : y);
```

####10.5.3 Expressions before `?' in the Conditional Operator
If an expression containing a binary operator appears before the `?` in the ternary `?:` operator, it should be parenthesized. Example:

```java
(x >= 0) ? x : -x;
````

####10.5.4 Special Comments
Use `XXX` in a comment to flag something that is bogus but works. Use `FIXME` to flag something that is bogus and broken.

[CONTENTS](TOC.md)

[PREVIOUS](page09.md) [NEXT](page11.md)
