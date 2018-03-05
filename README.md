# HW10. Josephus problem using array.
## This is an Exercise, and it is related to HW11 and HW12.

<strong>Please read the entire file before you ask any question.</strong><br>

In this Exercise you will solve a theoretical problem related to a certain counting-out game (Josephus problem).


# Learning Goals
* Solve Josephus problem.
* Understand permutation.
* Deepen your understanding of the use of loops.

## Josephus problem
 Josephus Problem (or Josephus permutation) is a theoretical problem. Following is the problem statement:
 
There are n numbers in a array to be counted out (one per step). The counting out begins at index zero and proceeds through the array in a fixed direction. In each step, a certain number of numbers are skipped and the next number is ruled out. The elimination proceeds through the array (which is becoming smaller and smaller as numbers are counted out), until only the last number remains, who wins the game. Given the total number of numbers n and a number k which indicates that k-1 numbers are skipped and kth number is out.

`NOTE: the number you start counting from will no be included in counting`

For example, let assume that the array size(n) is 5, and k=2. `ruled out numbers will be marked by (X)`
<pre>
0 1 2 3 4 5 // at the begining, start from index 0, counting k, you will stop at 2, then 2 will be out.
0 1 X 3 4 5 // after counting out a number, the n 



</pre>




# TO DO


# Testing your code
Following are the files we provide:
1. `pe10.c` 
2. `pe10.h` 
3. `main.c`

To test your code. You have to first compile it and then run one of the following commands. <br>


`Note: There is a 15% penalty of your final grade, if you do not submit a Makefile`

Type the following command to zip your file.
```bash
	zip pe10.zip pe10.c main.c Makefile
```
<strong>You will not get any credits if the submitted file is not zipped</strong>

The **only** way to submit homework is through Blackboard.

The instructor will **never** accept any requestion for exception "*my
submission is only one minute late*".  It is your responsibility to
meet the deadline.  You are strongly encouraged to submit at least ten
minutes before the deadline because submission may take time.

If there is a campus-wide problem (such as network outage or the
Blackboard server is down), the deadline will be extended for the
entire class. If the problem is specific to yourself (for example,
your computer crashes), the deadline will not be extended for
you.

**DO NOT** send your code by email. Your code will not be graded
  if it is sent by email.

The teaching staff is strictly prohibited to look at files on your
computer (or your Purdue account) for grading. Thus, **NEVER** say "I
finished before the deadline but I forgot to submit".  **NEVER** say "I have
not made any change after the submission deadline." because the
teaching staff is not allowed to look at your files that have not been
submitted through Blackboard.

# Grading
If your program has any compilation error or warning (remember to use
`gcc -std=c99 -g -Wall -Wshadow --pedantic -Wvla -Werror`), you will
receive zero in this assignment.

In absolutely no circumstance can the teaching staff modify your
program for grading.  You cannot say, "If you change this, my program
works." If your program misses a semicolon and cannot compile, you
will receive zero.  Your score depends on what is submitted, nothing
else.



**All Test cases will be released later.


