# Origins of the C programming language

**C** was developed from 1969 to 1973 by Dennis Ritchie of Bell Laboratories. The American National Standards Institute (ANSI) ratified the ANSI C standard in 1989, and this standardization later became the responsibility of the International Standards Organization (ISO). The standards define the C language and a set of library functions known as the *C standard library*. Kernighan and Ritchie describe ANSI C in their classic book, which is known affectionately as “K&R”. In Ritchie’s words [92], C is “quirky, flawed, and an enormous success.” So why the success?

- C *was closely tied with the Unix operating system*. C was developed from the beginning as the system programming language for Unix. Most of the Unix kernel (the core part of the operating
system), and all of its supporting tools and libraries, were written in C. As Unix became popular in universities in the late 1970s and early 1980s, many people were exposed to C and found that they liked it. Since Unix was written almost entirely in C, it could be easily ported to new machines, which created an even wider audience for both C and Unix.
- C *is a small, simple language*.The design was controlled by a single person, rather than a committee, and the result was a clean, consistent design with little baggage. The K&R book describes the complete language and standard library, with numerous examples and exercises, in only 261 pages. The simplicity of C made it relatively easy to learn and to port to different computers.
- C *was designed for a practical purpose*. C was designed to implement the Unix operating system. Later, other people found that they could write the programs they wanted, without the language getting in the way.

C is the language of choice for system-level programming, and there is a huge installed base of application-level programs as well. However, it is not perfect for all programmers and all situations. C pointers are a common source of confusion and programming errors. C also lacks explicit support for useful abstractions such as classes, objects, and exceptions. Newer languages such as C++ and Java address these issues for application-level programs.

The original Bell Labs version of C was documented in the first edition of the book by Brian Kernighan and Dennis Ritchie [60]. Over time, C has evolved through the efforts of several standardization groups. The first major revision of the original Bell Labs C led to the ANSI C standard in 1989, by a group working under the auspices of the American National Standards Institute. ANSI C was a major departure from Bell Labs C, especially in the way functions are declared. ANSI C is described in the second edition of Kernighan and Ritchie’s book, which is still considered one of the best references on C.

The International Standards Organization took over responsibility for standardizing the C language, adopting a version that was substantially the same as ANSI C in 1990 and hence is referred to
as “ISO C90.”

This same organization sponsored an updating of the language in 1999, yielding “ISO C99.” Among other things, this version introduced some new data types and provided support for text strings requiring characters not found in the English language. A more recent standard was approved in 2011, and hence is named “ISO C11,” again adding more data types and features. Most of these recent additions have been *backward* compatible, meaning that programs written according to the earlier standard (at least as far back as ISO C90) will have the same behavior when compiled according to the newer standards.

The **GNU Compiler Collection** (gcc) can compile programs according to the conventions of several different versions of the C language, based on different command-line options, as shown in the table bellow. For example, to compile program ```prog.c``` according to ISO C11, we could give the command line:

```terminal
linux> gcc -std=c11 prog.c
```

The options ```-ansi``` and ```-std=c89``` have identical effect—the code is compiled according to the ANSI or ISO C90 standard. (C90 is sometimes referred to as “C89,” since its standardization effort began in 1989.) The option ```-std=c99``` causes the compiler to follow the ISO C99 convention.

| C version | GCC command-line option |
| --------- | ----------------------- |
| GNU 89 | none, ```-std=gnu89``` |
| ANSI, ISO C90 | ```-ansi```, ```-std=c89``` |
| ISO C99 | ```-std=c99``` |
| ISO C11 | ```std=c11``` |

