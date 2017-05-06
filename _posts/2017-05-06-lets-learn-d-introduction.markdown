---
layout: post
title:  "Let’s learn D – #1: Introduction"
date:   2017-05-06 17:25:58 +0000
categories: tutorials
---
# What is D programming language?
The D programming language is an object-oriented, imperative, multi-paradigm system programming language created by Walter Bright of Digital Mars and released in 2001. Bright was joined in the design and development effort in 2007 by Andrei Alexandrescu. Though it originated as a re-engineering of C++, D is a distinct language, having redesigned some core C++ features while also taking inspiration from other languages, notably Java, Python, Ruby, C#, and Eiffel.

# Prerequisites
Before you start doing practice with some programming languange you should have an editor or even an IDE that fits your necessities. Here I prefer to use a text editor and a terminal emulator with some package for building and compiling because in a long term it’s more practical.

#### Building
For building, I highly recommend dub, an official supported building package for D programming languange files. To get more info and getting started with this new build system, see this official thread.

#### Compiling
For compiling, you have this highly supported compilers:
* DMD
* GDB
* LDC

In my opinion, I recommend to use DMD as your main compiler because its officially supported and it will always have the latest version of dlang. I also recommend the usage of LDC when you want to export your project as a final release because it’s LLVM-based.
# Hello World: Your first program
Let’s begin with a simple D program that displays a message. The following code uses the writeln() function to produce characters output.
```d
import std.stdio;

int main(string[] args_)
{
    writeln("Hello, world!");
}
```
***Attention:*** D, like many languanges, is case sensitive. It discriminates between uppercase and lowercase characters.

#### How can I compile and run it?
Here, in this tutorial collection, I’ll use DMD as a compiler, just a personal option, so you can use another compatible compiler without any problems.

1. Open a terminal window.
2. Go to the directory where you saved hello.d.
3. Enter the following commands. (Do not type the $ character; it is there to indicate the command line prompt.)

```shell
$ dmd hello.d
$ ./hello
```

If you did everything correctly, your program will output something like this:

`Hello, world!`

***Tip:*** For a beginner-friendly, step-by-step introduction on how to build your first D program see the this tutorial of Ali Çehreli’s online book Programming in D, which is recommended by the official dlang wiki in this thread.
