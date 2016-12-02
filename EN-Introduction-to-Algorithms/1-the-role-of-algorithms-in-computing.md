#The Role of Algorithms in Computing
## I. Algorithms
Informally, an algorithm is any well-defined **computational procedure** that takes some value, or set of values, as **input** and produces some value, or set of values, as **output**.

An algorithm is said to be **correct** if, for every input instance, it halts with the correct output. We say that a correct algorithm **solves** the given computational problem.

Contrary to what you might expect, **incorrect** algorithms can sometimes be useful, if we can **control their error rate**. We shall see an example of an algorithm with a controllable error rate in Chapter 31 when we study algorithms for finding large prime numbers.
###Data structures
A data structure is a way to **store and organize data** in order to facilitate **access and modifications**. No single data structure works well for all purposes, and so it is important to know the strengths and limitations of several of them.
###NP-complete
Our usual measure of efficiency is **speed**, i.e., how long an algorithm takes to produce its result. There are some problems, however, for which **no efficient solution is known**. NP-complete is an interesting subset of these problems.

Interesting NP-complete problems:
1. No one knows **whether or not** efficient algorithms exist for NP-complete problems.
1. If an efficient algorithm exists for **any one of them**, then efficient algorithms exist for **all of them**.
1. Several NP-complete problems are similar, but not identical, to problems for which we **do know of efficient algorithms**.

If you can show that the problem is NP-complete, you can instead spend your time developing an efficient algorithm that gives a good, but not the best possible, solution.
###Parallelism
In order to perform more computations per second, therefore, chips are being designed to contain not just one but several processing "cores." We can liken these **multi-core computers** to several **sequential computers on a single chip**; in other words, they are a type of "parallel computer." In order to elicit the best performance from multi-core computers, we need to design algorithms with parallelism in mind.
###Shortest-path and Traveling-salesman Problems
//TBD
##II. Algorithms as a technology
Of course, computers may be fast, but they are **not infinitely fast**. And memory may be inexpensive, but it is **not free**. Computing time is therefore **a bounded resource**, and so is space in memory. You should use these resources wisely, and algorithms that are efficient in terms of time or space will help you do so.
###Efficiency
**Different algorithms** devised to solve the same problem often differ dramatically in their efficiency. These differences can be much **more significant than differences due to hardware and software**.
###Algorithms and other technologies
The example above shows that we should consider algorithms, like computer hardware, **as a technology**. Total system performance depends on **choosing efficient algorithms** as much as on choosing fast hardware.
