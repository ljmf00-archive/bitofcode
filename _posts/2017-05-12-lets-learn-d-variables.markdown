---
layout: post
title:  "Let’s learn D – #2: Variables"
date:   2017-05-12 20:16:00 +0000
categories: tutorials
---

# What is a variable?

In programming, a [**variable**](https://en.wikipedia.org/wiki/Variable_(computer_science)) is a storage location paired with an associated symbolic name, which contains some known or unknown quantity of information referred to as a _value_. The variable name is the usual way to reference the stored value; this separation of name and content allows the name to be used independently of the exact information it represent. Each variable in D has a specific type, which determines the size and layout of the variable's memory; the range of values that can be stored within that memory; and the set of operations that can be applied to the variable. The name of a variable can be composed of letters, digits, and the underscore character. It must begin with either a letter or an underscore. Upper and lowercase letters are distinct because D is case-sensitive.

#### **Basic Data Types**

There are following some basic types of variables in D:
<table>
<tbody>
<tr>
<th class="donthyphenate" style="text-align: center;"><b>Keyword</b></th>
<th class="donthyphenate"><b>Default Initializer
</b></th>
<th class="donthyphenate" style="text-align: center;"><b>Description</b></th>
</tr>
<tr>
<td><span class="d_inlinecode donthyphenate notranslate">void</span></td>
<td><span class="d_inlinecode donthyphenate notranslate">-</span></td>
<td>no type</td>
</tr>
<tr>
<td><span class="d_inlinecode donthyphenate notranslate">bool</span></td>
<td><span class="d_inlinecode donthyphenate notranslate">false</span></td>
<td>boolean value</td>
</tr>
<tr>
<td><span class="d_inlinecode donthyphenate notranslate">byte</span></td>
<td><span class="d_inlinecode donthyphenate notranslate">0</span></td>
<td>signed 8 bits</td>
</tr>
<tr>
<td><span class="d_inlinecode donthyphenate notranslate">int</span></td>
<td><span class="d_inlinecode donthyphenate notranslate">0</span></td>
<td>signed 32 bits</td>
</tr>
<tr>
<td><span class="d_inlinecode donthyphenate notranslate">float</span></td>
<td><span class="d_inlinecode donthyphenate notranslate">float.nan</span></td>
<td>32 bit floating point</td>
</tr>
<tr>
<td><span class="d_inlinecode donthyphenate notranslate">double</span></td>
<td><span class="d_inlinecode donthyphenate notranslate">double.nan</span></td>
<td>64 bit floating point</td>
</tr>
<tr>
<td><span class="d_inlinecode donthyphenate notranslate">real</span></td>
<td><span class="d_inlinecode donthyphenate notranslate">real.nan</span></td>
<td>largest FP size implemented in hardware<span class="footnote">Implementation Note: 80 bits for x86 CPUs or <span class="d_inlinecode donthyphenate notranslate">double</span> size, whichever is larger</span></td>
</tr>
<tr>
<td><span class="d_inlinecode donthyphenate notranslate">char</span></td>
<td><span class="d_inlinecode donthyphenate notranslate">0xFF</span></td>
<td>unsigned 8 bit (UTF-8 code unit)</td>
</tr>
</tbody>
</table>
For more data types, click [here](https://dlang.org/spec/type.html#basic-data-types).

# Variable Definition

A variable definition means to tell the compiler where and how much to create the storage for the variable. A variable definition specifies a data type, and contains a list of one or more variables of that type as follows this syntax:

```
type variable_name;
```

*   **type**: this need to be a valid data type. It can be predefined or user defined;
*   **variable_name**: the name of the variable. it must start with a letter or an underscore.

#### Examples

```d
int integer, i, n; char c, ch;
```

# Variable Declaration

A variable declaration provides assurance to the compiler that there is one variable existing with the given type and name so that compiler proceed for further compilation without needing complete detail about the variable. A variable declaration has its meaning at the time of compilation only, compiler needs actual variable definition at the time of linking of the program.

#### Examples

```d
int i = 42; int n; n = 33; char ch = 'f';
```

# Example
To see how variables works in action within a program, let's have a look at the entire D code of the example about what you learned in this tutorial:

```d
import std.stdio;

int i = 1;

int main(string[] args_)
{
    char ch = 'a';
    int n;
    n = 2;

    writeln(i);
    writeln(n);
    writeln(ch);
}
```
