#Building Abstractions with Procedures
##I.The Elements of Programming
A powerful programming language is more than just a means for instructing a computer to perform tasks. The language also serves as a framework within which we organize our ideas about processes.
- **primitive expressions**, which represent **the simplest entities** the language is concerned with,
- **means of combination**, by which compound elements are **built from simpler ones**, and
- **means of abstraction**, by which compound elements can **be named and manipulated** as units

Thus, any powerful programming language should be able to **describe primitive data and primitive procedures** and should have **methods for combining** and abstracting procedures and data.
###i.Expressions
You type an **expression**, and the interpreter responds by displaying the result of its **evaluating** that expression.

Expressions representing numbers may be combined with an expression representing a **primitive procedure** (such as + or * ) to form a compound expression that represents the application of the procedure to those numbers.
```
(+ 137 349)
486
```
The leftmost element in the list is called the **operator**, and the other elements are called **operands**. The value of a combination is obtained by applying the procedure specified by the operator to the arguments that are the values of the operands.

The convention of placing the operator to the left of the operands is known as **prefix** notation, it can accommodate procedures that may take an **arbitrary number** of arguments.

A second advantage of prefix notation is that it extends in a straightforward way to allow combinations to be **nested**, that is, to have combinations whose elements are themselves **combinations**
```
(+ (* 3
      (+ (* 2 4)
         (+ 3 5)))
   (+ (- 10 7)
      6))
```
A formatting convention known as **pretty-printing**, in which each long combination is written so that the **operands are aligned vertically**.

Observe in particular that it is not necessary to explicitly instruct the interpreter to **print the value of the expression**.
>Lisp programmers know the value of everything but the cost of nothing.--Alan Perlis

##ii.Naming and the Environment
We say that the name identifies a **variable** whose value is the object.
```
(define size 2)
```
Define is our language’s simplest means of **abstraction**, for it allows us to use simple names to **refer to** the results of compound operations.
