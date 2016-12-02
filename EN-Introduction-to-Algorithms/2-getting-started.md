#Getting Started
##I. Insertion sort
###Pseudocode
What separates pseudocode from "real" code is that in pseudocode, we employ whatever expressive method is **most clear and concise** to specify a given algorithm. Another difference between pseudocode and real code is that pseudocode is **not typically concerned with issues of software engineering**. Issues of **data abstraction, modularity, and error handling** are often ignored in order to **convey the essence of the algorithm** more concisely.

###Insertion Sort
An efficient algorithm for sorting a small number of elements.
```
INSERTION-SORT(A)
1 for j = 2 to A.length
2   key = A[j]
3   //Insert A[j] to the sorted sequence A[1 .. j-1]
4   i = j - 1
5   while i > 0 and A[i] > key
6     A[i+1] = A[i]
7     i = i - 1
8   A[i+1] = key
```
###Loop invariants and the correctness of insertion sort
####Loop invariants
At the start of each iteration of the for loop of lines 1–8, the subarray `A[1 .. j-1]` **consists of the elements originally in** `A[1 .. j-1]` , but in **sorted order**.

We use loop invariants to help us understand why an algorithm is correct. We must show three things about a loop invariant:
1. Initialization: It is **true** prior to the **first iteration** of the loop.
1. Maintenance: If it is **true before an iteration** of the loop, it **remains true before the next iteration**.
1. Termination: When the loop terminates, the invariant gives us a **useful property** that **helps show that the algorithm is correct**.

When the first two properties hold, the loop invariant is true prior to every iteration of the loop. (Of course, we are free to use established facts other than the loop invariant itself to prove that the loop invariant remains true before each iteration.) Note the similarity to **mathematical induction**, where to prove that a property holds, you prove a base case and an inductive step.

The third property is perhaps **the most important one**, since we are using the loop invariant to show correctness. Typically, we use **the loop invariant along with the condition** that **caused the loop to terminate**. The termination property **differs** from how we usually use mathematical induction, in which we **apply the inductive step infinitely**; here, we **stop the "induction"** when the loop **terminates**.

####Initialization
The moment at which we **check the loop invariant** just prior to the first iteration is immediately after **the initial assignment to the loop-counter variable** and just before **the first test in the loop header**. In the case of INSERTION-SORT, this time is after assigning 2 to the variable j but before the first test of whether j <= A.length.

####Maintenance
Showing that each iteration **maintains the loop invariant**. Informally, the body of the for loop works by **moving** `A[j-1]`, `A[j-2]`, `A[j-3]`, and so on by one position to the right until it finds the proper position for `A[j]`  (lines 4–7), at which point it inserts the value of `A[j]`  (line 8). The subarray `A[1 ... j]`  then **consists of the elements originally** in `A[1 ... j]` , but in **sorted order**. Incrementing j for the next iteration of the for loop then **preserves the loop invariant**.

####Termination
What happens when the **loop terminates**. The condition causing the for loop to terminate is that `j > A.length = n`. Because each loop iteration increases j by 1, we must have **j = n + 1** at that time. **Substituting n + 1 for j** in the wording of loop invariant, we have that the subarray `A[1 ... n]` consists of the elements originally in `A[1 ... n]`, but in sorted order. Observing that the subarray `A[1 ... n]` is **the entire array**, we conclude that the entire array is sorted. Hence, the algorithm is correct.

**We shall use this method of loop invariants to show correctness later in this chapter and in other chapters as well.**

###Pseudocode conventions
1. **Indentation indicates block structure**. Using indentation instead of conventional indicators of block structure, such as `begin` and `end` statements, greatly reduces clutter while preserving, or even **enhancing, clarity**.
1. **The loop counter retains its value after exiting the loop**, unlike some situations that arise in C++, Java, and Pascal.
1. **The symbol “//” indicates that the remainder of the line is a comment.**
1. **A multiple assignment of the form `i = j = e` assigns to both variables i and j the value of expression e**; it should be treated as equivalent to the assignment `j = e` followed by the assignment `i = j` .
1. Variables (such as i, j , and key) are **local to the given procedure**. We shall not use global variables without explicit indication.
1. We access array elements by **specifying the array name** followed by the index in square brackets. For example, `A[i]` indicates the **ith element** of the array A. The notation “...” is used to indicate a range of values within an array.Thus, `A[1 ... j]`  indicates the subarray of A consisting of the `j` elements `A[1]`; `A[2]`; ... ; `A[j]`.
1. We typically **organize compound data** into **objects**, which are composed of **attributes**. Sometimes, a pointer will refer to no object at all. In this case, we give it the **special value NIL**.
1. We pass parameters to a procedure **by value**: the called procedure receives **its own copy of the parameters**, and if it assigns a value to a parameter, the change is not seen by the calling procedure. When objects are passed, the pointer to **the data representing the object is copied**, but the **object’s attributes are not**.
1. A **return statement** immediately transfers control back to **the point of call in the calling procedure**.
1. The boolean operators `and` and `or` are **short circuiting**.
1. The keyword `error` indicates that an error occurred because conditions were wrong for the procedure to have been called.

##II.Analyzing algorithms
**Analyzing** an algorithm has come to mean **predicting the resources** that the algorithm requires.
###Random-access Machine (RAM) Model
In the RAM model, instructions are **executed one after another**,
with no **concurrent operations**.

The RAM model contains instructions commonly found in real computers:**arithmetic** (such as add, subtract, multiply, divide, remainder, floor, ceiling), **data movement** (load, store, copy), and **control** (conditional and unconditional branch, subroutine call and return). Each such instruction takes **a constant amount of time**.

For example, when working with inputs of size n, we typically assume that integers are represented by **$c\lg n$ bits** for some constant `c >= 1`. We require `c >= 1` so that each word can hold **the value of n**.

We will endeavor to void such **gray areas** in the RAM model, but we will treat computation of $2^k$ as **a constant-time operation** when `k` is a **small enough positive integer**.

In the RAM model, we **do not attempt to model the memory hierarchy** that is common in contemporary computers. That is, we **do not model caches or virtual memory**.

Analyzing even a simple algorithm in the RAM model can be a challenge. The mathematical tools required may include **combinatorics, probability theory, algebraic dexterity, and the ability to identify the most significant terms in a formula**. Because the behavior of an algorithm may be different for each possible input, we need a means for summarizing that behavior in **simple, easily understood formulas**.

We would like a way that is **simple to write and manipulate**, shows the important characteristics of **an algorithm’s resource requirements**, and **suppresses tedious details**.
###Analysis of insertion sort
In general, the time taken by an algorithm **grows with the size of the input**, so it is traditional to describe the running time of a program as **a function of the size of its input**. To do so, we need to define the terms **“running time”** and **“size of input”** more carefully.
####Size of Input
The best notion for input size **depends on the problem being studied**.For many problems, the most natural measure is **the number of items in the input**. For many other problems, such as multiplying two integers, the best measure of input size is **the total number of bits needed to represent the input in ordinary binary notation**. Sometimes, it is more appropriate to **describe the size of the input with two numbers** rather than one.
####Running Time
The running time of an algorithm on a particular input is **the number of primitive operations or “steps” executed**. One line may take a different amount of time than another line, but we shall assume that each execution of the **ith line takes time $c_i$**, where **$c_i$ is a constant**. This viewpoint is in keeping with the RAM model, and it also reflects how the pseudocode would be **implemented on most actual computers**.
####Analysis of insertion sort
For each `j = 2; 3; ... ; n`, where `n = A.length`, we let **$t_j$** denote **the number of times the while loop test** in line 5 is executed for that value of `j` .  When a `for` or `while` loop exits in the usual way (i.e., due to the test in the loop header), the test is executed **one time more** than the loop body.
\[\begin{array}{clcc}
n & INSERTION-SORT(A) & cost & times
\\1&\text{for}j=2\text{to} A.length&c_1&n
\\2&\quad key=A[j]&c_2&n-1
\\3&\quad //\text{Insert A[j] to the sorted sequence A[1 .. j-1]}&0&n-1
\\4&\quad i=j-1&c_4&n-1
\\5&\quad\text{while}i>0\,and\,A[i] > key&c_5&\sum^n_{j=2}t_j
\\6&\quad\quad A[i+1]=A[i]&c_6&\sum^n_{j=2}(t_j)
\\7&\quad\quad i=i-1&c_7&\sum^n_{j=2}(t_j-1)
\\8&\quad A[i+1]=key&c_8&n-1
\end{array}\]
Even for inputs of a given size, an algorithm’s running time may depend on **which input of that size** is given.
\[T(n)=c_1n+c_2(n-1)+c_4(n-1)+c_5+\sum^n_{j=2}t_j+c_6\sum^n_{j=2}(t_j-1)+c_7\sum^n_{j=2}(t_j-1)+c_8(n-1)\]
######The best-case running time is
\[T(n)=c_1n+c_2(n-1)+c_4(n-1)+c_5(n-1)+c_8(n-1)=\\(c_1+c_2+c_4+c_5+c_8)n-(c_2+c_4+c_5+c_8)\]
We can express this running time as `an + b` for constants `a` and `b` that depend on the statement costs $c_i$; it is thus a **linear function** of n.
######The worst case
\[T(n)=c_1n+c_2(n-1)+c_4(n-1)+c_5\Big(\frac{n(n+1)}2-1\Big)+c_6\Big(\frac{n(n-1)}2\Big)+c_7\Big(\frac{n(n-1)}2\Big)+c_8(n-1)\\=(\frac{c_5}2+\frac{c_6}2+\frac{c_7}2)n^2+(c_1+c_2+c_4+\frac{c_5}2-\frac{c_6}2-\frac{c_7}2+c_8)n-(c_2+c_4+c_5+c_8)\]
We can express this worst-case running time as $an^2+bn+c$ for constants `a`, `b`, and `c` that again depend on the statement costs $c_i$; it is thus a **quadratic function** of n.
####Worst-case and average-case analysis
For the remainder of this book, though, we shall usually concentrate on finding only **the worst-case running time**, that is, the **longest running time** for any input of size n.
1. The worst-case running time of an algorithm gives us **an upper bound** on the running time for any input.
1. For some algorithms, the worst case **occurs fairly often**. For example, in searching a database for a particular piece of information, the searching algorithm’s worst case will often occur when the information is **not present in the database**. In some applications, **searches for absent information** may be frequent.
1. The “average case” is often roughly **as bad as** the worst case. The resulting average-case running time turns out to be a quadratic function of the input size, **just like** the worst-case running time.

In some particular cases, we shall be interested in **the average-case running time** of an algorithm; we shall see the technique of **probabilistic analysis** applied to various algorithms throughout this book. The scope of average-case analysis is limited, because it **may not be apparent** what constitutes an “average” input for a particular problem. Often, we shall assume that all inputs of a given size **are equally likely**. In practice, this assumption may be violated, but we can sometimes use a **randomized algorithm**, which makes random choices, to allow a probabilistic analysis and yield an **expected** running time. We explore randomized algorithms more in Chapter 5 and in several other subsequent chapters.
####Order of growth
We shall now make one more simplifying abstraction: it is the **rate of growth**, or **order of growth**, of the running time that really interests us. We therefore consider **only the leading term** of a formula (e.g., $an^2$), since the lower-order terms are relatively insignificant for large values of `n`. For insertion sort, when we ignore the lower-order terms and the leading term’s constant coefficient, we are left with **the factor of n2 from the leading term**. We write that insertion sort has **a worst-case running time** of $\Theta(n^2)$ (pronounced “theta of n-squared”). We shall use $\Theta$-notation informally in this chapter, and we will define it precisely in Chapter 3.
##III.Designing algorithms
###The divide-and-conquer approach
We’ll use divideand-conquer to design a sorting algorithm whose worst-case running time is much less than that of insertion sort. One advantage of divide-and-conquer algorithms is that **their running times are often easily determined** using techniques that we will see in Chapter 4.

Many useful algorithms are **recursive** in structure: to solve a given problem, they call themselves recursively **one or more times to deal with closely related subproblems**.They **break the problem into several subproblems** that are **similar to the original problem** but smaller in size, solve the subproblems recursively, and then **combine these solutions to create a solution to the original problem**.

The divide-and-conquer paradigm involves **three steps** at each level of the recursion:
1. **Divide** the problem into **a number of subproblems** that are smaller instances of the same problem.
1. **Conquer** the subproblems by solving them recursively. If the subproblem sizes are small enough, however, just **solve the subproblems in a straightforward manner**.
1. **Combine** the solutions to the subproblems into the solution for the original problem.

The key operation of the merge sort algorithm is the **merging of two sorted sequences** in the “combine” step. We merge by calling an auxiliary procedure `MERGE(A,p,q,r)`, where `A` is an array and `p, q,` and `r` are indices into the array such that $p\leq q<r$. The procedure assumes that the subarrays `A[p ... q]` and `A[q+1 ... r]` are in **sorted order**. It merges them to form a single sorted subarray that replaces the current subarray `A[p ... r]`.Our MERGE procedure takes time **$\Theta(n)$**.

The following pseudocode implements the above idea, but with an additional twist that **avoids having to check whether either pile is empty** in each basic step. We place on the bottom of each pile **a sentinel card**, which contains **a special value** that we use to simplify our code. Here, we use $\infty$ as the sentinel value, so that whenever a card with $\infty$ is exposed, it **cannot be the smaller** card unless both piles have their sentinel cards exposed. But **once that happens**, all the **nonsentinel cards have already been placed onto the output pile**. Since we know in advance that exactly `r-p+1` cards will be placed onto the output pile, we **can stop once we have performed that many basic steps**.
\[\begin{array}{cl}
n & MERGE(A,p,q,r)
\\1&n_1=q-p+1
\\2&n_2=r-q
\\3&\text{let}\,L[1..n_1+1]\,\text{and}\,R[1..n_2+1]\,\text{be new arrays}
\\4&\text{for}\,i=1\text{to}\,n_1
\\5&\quad L[i]=A[p+i-1]
\\6&\text{for}\,j=1\text{to}\,n_2
\\7&\quad R[j]=A[q+j]
\\8&L[n_1+1]=\infty
\\9&R[n_2+1]=\infty
\\10&i=1
\\11&j=1
\\12&\text{for}\,k=p\,\text{to}\,r
\\13&\quad\text{if}\,L[i]\leq R[j]
\\14&\quad\quad A[k]=L[i]
\\15&\quad\quad i=i+1
\\16&\quad\text{else}\,A[k]=R[j]
\\17&\quad\quad j=j+1
\end{array}\]
