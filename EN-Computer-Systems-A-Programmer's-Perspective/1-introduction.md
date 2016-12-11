#Introduction
##I. Information is Bits in Context
The source program is a sequence of bits, each with a value of 0 or 1, organized in 8-bit chunks called **bytes**.

All information in a system — including disk files, programs stored in memory, user data stored in memory, and data transferred across a network — is **represented as a bunch of bits.**
##II. Programs are Translated by Other Programs into Different Forms
The `hello` program begins life as a **high-level** C program because it can be read and understand by human beings in that form. However, in order to run hello.c on the system, the individual C statements must be translated by other programs into a sequence of **low-level** **machine-language** instructions.

The translation is performed in the sequence of **four phases**.
\[\xrightarrow[\text{source program(text)}]{hello.c}\boxed{\text{preprocessor}}
\xrightarrow[\text{modified source program (text)}]{hello.i}\boxed{\text{compiler}}\\
\xrightarrow[\text{assembly program (text)}]{hello.s}\boxed{\text{assembler}}
\xrightarrow[\text{relocatable object programs (binary)}]{hello.o}\boxed{\text{linker}}\\
\xrightarrow[\text{executable object program(binary)}]{hello}\]
1. **Preprocessing phase**. The **preprocessor** (cpp) **modifies** the original C program according to directives that begin with the `#` character.  The result is **another** C program, typically with the `.i` suffix.
1. **Compilation phase**. The **compiler** (cc1) translates the text file `hello.i` into the text file `hello.s`, which contains an **assembly-language** program.
1. **Assembly phase**. Next, the **assembler** (as) translates `hello.s` into **machine-language** instructions, packages them in a form known as a **relocatable object program**, and stores the result in the object file hello.o.
1. **Linking phase**. Notice that our `hello` program calls the `printf` function, which is part of the standard C library provided by every C compiler. The `printf` function resides in a separate **precompiled object file** called `printf.o`, which must somehow be merged with our `hello.o` program. The **linker** (ld) handles this merging. The result is the hello file, which is an **executable object file** (or simply executable) that is ready to be loaded into memory and executed by the system.
##III. It Pays to Understand How Compilation Systems Work
1. **Optimizing program performance**. In order to make good coding decisions in our C programs, we do need a basic understanding of assembly language and how the compiler translates different C statements into assembly language.
1. **Understanding link-time errors**. In our experience, some of the most perplexing programming errors are related to the operation of the linker, especially when are trying to build large software systems.
1. **Avoiding security holes**. These bugs exist because too many programmers are ignorant of the stack discipline that compilers use to generate code for functions.
##IV. Processors Read and Interpret Instructions Stored in Memory
