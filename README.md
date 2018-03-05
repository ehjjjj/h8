# HW10. Josephus problem using array.
## This is an Exercise, and it related to HW11 and HW12.

<strong>Please read the entire file before you ask any question.</strong><br>

In this Exercise you will solve a theoretical problem related to a certain counting-out game (Josephus problem).


# Learning Goals
* Solve Josephus problem.
* Understand permutation.
* Deepen your understanding of the use of loops.

## Josephus problem




# TO DO
In this assignment you will implement a function `createDouble()` that will generate all possible matchings for a double within a given length and digit range. The Regex of double is `"^\d+[.]\d+$"`. This function will generate all possible matchings for `"^[DS-DE]+[.][DS-DE]+$"`. DS and DE are digit start and end boundaries.<br/>

For example, the following command will print out all possible double with DS='0', DE='1', and max length of 4. <br/>
`./pa08 -D 0 1 4` <br/> 
Outputs (separated by comma): <br/>
`0.0, 0.1, 1.0, 1.1, 0.00, 0.01, 0.10, 0.11, 1.00, 1.01, 1.10, 1.11, 00.0, 00.1, 01.0, 01.1, 10.0, 10.1, 11.0, 11.1`
<br/><br/>


<strong> Bonus function to implement (Optional) </strong> <br/>
The bonus function `createVID` will generate all possible matchings for a valid identifier within a given length ,and alphabet and digit range. The Regex of valid identifier is `"^[ [a-zA-Z] | _ ] [ [a-zA-Z] | \d| _ ]*$"`. This function will generate all possible matchings for `"^[ [LCS-LCE]|[UCS-UCE] | _ ] [ [LCS-LCE]|[UCS-UCE] | [DS-DE]| _ ]*$"`. LCS and LCE are lower case start and end boundaries. UCS and UCE are upper case start and end boundaries. DS and DE are digit start and end boundaries.<br/>

For example, the following command will print out all possible identifers with LCS='a', LCE='b', UCS='C',UCE='D', DS='0', DE='1', and max length of 2. <br/>
`./pa08 -VID a b C D 0 1 2`<br/>
Outputs (separated by comma):<br/>
`a, b, C, D, _, aa, ab, aC, aD, a_, a0, a1, ba, bb, bC, bD, b_, b0,b1, ...., _a,_b,_C,_D,__,_0,_1`
<br/><br/>


`Note: DS and DE can take values from '0' to '9', but DS<=DE. LCS and LCE can take values from 'a' to 'z', but LCS<=LCE. UCS and UCE can take values from 'A' to 'Z', but UCS<=UCE.`

`Length Note: the minimum length of double is 3, while the minimum length of identifier is 1.`


# Testing your code
Following are the files we provide:
1. `pa08.c` 
2. `pa08.h` 
3. `main.c`

To test your code. You have to first compile it and then run one of the following commands. <br>

./pa08 -D 0 2 3 > outDouble.txt<br/>
Print out all possible identifers with max length 3, DS=0, DE=2. The Expected output for this case is in outDouble.txt<br/>

./pa08 -D 0 2 3 | sort > outSortedDouble.txt<br/>
Sort Print out all possible identifers with max length 3, DS=0, DE=2. The Expected output for this case is in outSortedDouble.txt<br/>

./pa08 -D 4 9 5 > outDouble2.txt<br/>
Print out all possible identifers with max length 5, DS=4, DE=9. The Expected output for this case is in outDouble2.txt<br/>

./pa08 -D 4 9 5 | sort > outSortedDouble2.txt<br/>
Print out all possible identifers with max length 5, DS=4, DE=9. The Expected output for this case is in outSortedDouble2.txt<br/>

./pa08 -VID a b C D 1 3 2 > outVID.txt<br/>
Print out all possible identifers with max length 2, LCS=a, LCE=b, UCS=C, UCE=D, DS=1, DE=3. The Expected output for this case is in outVID.txt<br/>

./pa08 -VID a b C D 1 3 2 | sort > outSortedVID.txt<br/>
Sort and Print out all possible identifers with max length 2, LCS=a, LCE=b, UCS=C, UCE=D, DS=1, DE=3. The Expected output for this case is in outSortedVID.txt<br/>

`Note: Since your code may print the output in a different order; you should only compare your sorted output with the sorted expected output to verify the correctness of your output`

# Submitting Your code
** This is a programming exercise, so you would have to submit the code on Blackboard.**

You have to submit the following file in a <strong>zip</strong> folder on the blackboard:
* `pa08.c` - This file should have `createDouble()` and `createVID()` functions implemented.
* `main.c` - This file should have `main()` function implemented.<br/>
* `Makefile` - This file should have 10 different test cases commands (All Sorted i.e | sort), and test coverage command at the end. The output of each command should be in file named test_case_name.txt, i.e if the test case name is testVID then the filename will be testVID.txt 

`Note: There is a 15% penalty of your final grade, if you do not submit a Makefile`

Type the following command to zip your file.
```bash
	zip pa08.zip pa08.c main.c Makefile
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


