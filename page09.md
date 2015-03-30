##9 - Naming Conventions
Naming conventions make programs more understandable by making them easier to read. They can also give information about the function of the identifier-for example, whether it's a constant, package, or class-which can be helpful in understanding the code.

Identifier Type | Rules for Naming | Examples
----------------|------------------|---------
Packages | The prefix of a unique package name is always written in all-lowercase ASCII letters and should be one of the top-level domain names, currently com, edu, gov, mil, net, org, or one of the English two-letter codes identifying countries as specified in ISO Standard 3166, 1981. Subsequent components of the package name vary according to an organization's own internal naming conventions. Such conventions might specify that certain directory name components be division, department, project, machine, or login names. | `com.sun.eng` `com.apple.quicktime.v2` `edu.cmu.cs.bovik.cheese`
Classes | Class names should be nouns, in mixed case with the first letter of each internal word capitalized. Try to keep your class names simple and descriptive. Use whole words-avoid acronyms and abbreviations (unless the abbreviation is much more widely used than the long form, such as URL or HTML). | <code>class&nbsp;Raster;</code> <code>class&nbsp;ImageSprite;</code>
Interfaces | Interface names should be capitalized like class names. | <code>interface&nbsp;RasterDelegate;</code> <code>interface&nbsp;Storing;</code>
Methods | Methods should be verbs, in mixed case with the first letter lowercase, with the first letter of each internal word capitalized. | `run();` `runFast();` `getBackground();`
Variables | Except for variables, all instance, class, and class constants are in mixed case with a lowercase first letter. Internal words start with capital letters. Variable names should not start with underscore `_` or dollar sign `$` characters, even though both are allowed. Variable names should be short yet meaningful. The choice of a variable name should be mnemonic- that is, designed to indicate to the casual observer the intent of its use. One-character variable names should be avoided except for temporary "throwaway" variables. Common names for temporary variables are `i`, `j`, `k`, `m`, and `n` for integers; `c`, `d`, and `e` for characters. | `int    i;` `char   c;` `float  myWidth;`
Constants | The names of variables declared class constants and of ANSI constants should be all uppercase with words separated by underscores (`_`). (ANSI constants should be avoided, for ease of debugging.) | <code>static&nbsp;final&nbsp;int&nbsp;MIN_WIDTH&nbsp;=&nbsp;4;</code> <code>static&nbsp;final&nbsp;int&nbsp;MAX_WIDTH&nbsp;=&nbsp;999;</code> <code>static&nbsp;final&nbsp;int&nbsp;GET_THE_CPU&nbsp;=&nbsp;1;</code>

[CONTENTS](TOC.md)

[PREVIOUS](page08.md) [NEXT](page10.md)
