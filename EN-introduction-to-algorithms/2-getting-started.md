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
At the start of each iteration of the for loop of lines 1–8, the subarray A[1 .. j-1] **consists of the elements originally in** A[1 .. j-1] , but in **sorted order**.

We use loop invariants to help us understand why an algorithm is correct. We must show three things about a loop invariant:
1. Initialization: It is **true** prior to the **first iteration** of the loop.
1. Maintenance: If it is **true before an iteration** of the loop, it **remains true before the next iteration**.
1. Termination: When the loop terminates, the invariant gives us a **useful property** that **helps show that the algorithm is correct**.

When the first two properties hold, the loop invariant is true prior to every iteration of the loop. (Of course, we are free to use established facts other than the loop invariant itself to prove that the loop invariant remains true before each iteration.) Note the similarity to **mathematical induction**, where to prove that a property holds, you prove a base case and an inductive step.

The third property is perhaps **the most important one**, since we are using the loop invariant to show correctness. Typically, we use **the loop invariant along with the condition** that **caused the loop to terminate**. The termination property **differs** from how we usually use mathematical induction, in which we **apply the inductive step infinitely**; here, we **stop the "induction"** when the loop **terminates**.
