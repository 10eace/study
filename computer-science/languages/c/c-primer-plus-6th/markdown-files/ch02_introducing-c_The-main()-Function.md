# **Chapter 02 Introducing C**  


Gonna learn about:
- Operator:  
    `=`
- Functions:  
    `main()`, `printf()`
- Putting together a simple C program
- The newline character
- How to include comments in your programs, create programs containing more than one function, and find program errors
- What keywords are

<br/>

## **A Simple Example of C**
We're going to look at a simple C program which serves to point out some of the basic featrues of programming in C. 


```c
// Listing 2.1 The first.c program

#include <stdio.h>

int main(void){    /* a simple program */
    int num;    /* define a variable called num*/
    num = 1;    /* assign a value to num */
    
    printf("I am a simple ");    /* use the printf() function */
    printf("computer.\n");
    printf("My favorite number is %d because it is first.\n", num);

    return 0;
}
```

    I am a simple computer.
    My favorite number is 1 because it is first.


### The Example Explained  
We'll take two passes through the program's source code.  
- the first pass highlights the meaning of each line
- the second pass explores specific implications and details  


### Pass 1: Quick Synopsis  
**`#include <stdio.h>`**  
- It tells the compiler to include the information found in the file `stdio.h`
- `stdio.h` file is a standard part of all C compiler packages. It provides support for keyboard input and displaying output.  


**`int main(void)`**  
- C programs consist of functions, and the functions are basic modules of C program.
- This program consists of one function called `main`.
- parentheses identify `main()` as a function name.
- `int` indicates that the `main()` function returns an integer.
- `void` indicates that `main()` doesn't take arguments.
- `int` and `void` are part of the standard ANSI C way for defining `main()`  


**`/* a simple program */`**  
- Comments are enclosed by `/*` and `*/`
- Comments remark that help clarify a program.
- Comments are intended for the reader only and ignored by the compiler.  


**`{`**  
- It marks the start of the statements that make up the function.  


**`int num;`**  
- This statement announces that you are using a variable called `num`.
- The variable called `num` will be an `int` type.  


**`num = 1;`**  
- Assign the value `1` to the variable `num`.  


**`printf("I am a simple ");`**  
- It displays the phrase `I am a simple ` on your screen.
- Leaves the cursor on the same line after displaying.
- `printf()` is part of the standard C library and termed a function.
- Using a function in the program is termed 'calling a function'.  


**`printf("computer.\n);`**  
- The second function call.
- It displays the phrase `computer` to the end of the last phrase printed.
- `\n` tells the computer to start a new line.  


**`printf("My favorite number is %d because it is first.\n", num);`**  
- This code prints the value of `num` embedded in the phrase in quotes.
- `%d` instructs the computer where and in what form to print the value of `num`.  


**`return 0;`**  
- C function can furnish, or return, a number to the agency that used it.
- It could be regarded as the appropriate closing for a `main()`.  


**`}`**  
- The program ends with a closing brace.  

<br/>

### Pass 2: Program Details  
##### `#include` Directives and Header Files  
**`#include <stdio.h>`**  
- same as typing the entire contents of the `stdio.h` file into the source code file at the point where the `#include <stdio.h>` line appears  
&rightarrow; the statement is a cut-and-paste operation  
&rightarrow; `#include` statement provides a convenient way to share information and it is common to many programs  
- `#include` statement = an example of a C preprocessor directive  
    - preprocessing  
    -preparatory work performed by C compilers  
    - `stdio.h` file &subset; C compiler packages  
    -`stdio.h` contains information about input and output functions(ex. `printf()`)  
    -Standard Input/Output Header(stdio.h)  
    -header: collection of information that goes at the top of a file  
    -header files contain information used by the compiler to build the final excutable program  
    (ex. header files define constants or indicate the names of functions and how they should be used)  
    -the actual code for a function is in a library file of precompiled code, not in a header file  
    -the linker component of the compiler takes care of finding the library code you need  
    &rightarrow; header files help guide the compiler in putting your program together correctly  
- ANSI/ISO has standardized which header files a C compiler must make available  
    - ex. some programs need to include `stdio.h`, and some don't  
    - the documentation for a particular C implementation should include a description of the functions in the C library  
    (ex. the description for `printf()` syas to use `stdio.h`)


##### The `main()` Function  
**`int main(void)`**  
- this statement proclaims a function by teh name of `main`  
- a C program always begins execution with the `main()` function  
- except for `main()` function, you can choose names for functions whatever you want  
&rightarrow; `main()` must be there to start things  
- `()` identify `main()` as a function  
- functions are the basic modues of C program  
- `int`  
    - `main()`'s return type  
    &rightarrow; `main()` can return(to the operating system) the value which is integer type  
- `()`  
    - generally enclose information being passed along to the function  
    (ex. `(void)` means that there is nothing to be passed along)

