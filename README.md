# HW8. Recursion (Regular Expression) Assignment
## This is an Assignment.

<strong>Please read the entire file before you ask any question.</strong><br>

In this assignment you will deepen your understanding of recursion and regular expressions(RegEx). RegEx is used mainly for pattern-matching, parsing, and filtering. Most importantly it is used by compilers such as gcc (C compiler) to translate the high level language to machine language. https://www.tutorialspoint.com/compiler_design/compiler_design_lexical_analysis.htm

More about RegEx : https://www.tutorialspoint.com/java/java_regular_expressions.htm


# Learning Goals
* Use recursion to solve complex problems.
* Understanding the concept of pipe (|) and the command sort.
* Test the coverage of your program using gcov.

## SORT command
Command sort which is a  linux command for sorting lines of text files. It supports sorting alphabetically, in reverse order, by number, by month and can also remove duplicates. The sort command can also sort by items not at the beginning of the line, ignore case sensitivity and return whether a file is sorted or not. By default sort command will sort lines alphabetically.

For example, suppose a file exists with the following list of car brands that needs to be sorted in alphabetical order. The file is saved as cars.txt

The following command `cat` will print out cars.txt content on the terminal screen.
<pre>
user@bash:~$ cat cars.txt
Ford
Mercedes
Dodge 
Chrysler
Hyundai
</pre>
The `sort` command will print out cars.txt content on the terminal screen alphabetically ordered.
<pre>
user@bash:~$ sort cars.txt
Chrysler
Dodge
Ford
Hyundai
Mercedes
</pre>

## PIPE(|)
Every standard process in Unix has at least three file descriptors:<br/>
1\- Standard output (STDOUT), which is the place where the process prints its data (i.e terminal screen or specific file).<br/>
2\- Standard input  (STDIN),  which is the place it gets its data from (i.e keyboard).<br/>
3\- Standard error  (STDERR), which is the place where errors and sometimes other out-of-band data goes.<br/><br/>

A Unix pipe (|) connects the STDOUT file descriptor of the first process to the STDIN of the second. So, when the first process writes to its STDOUT, that output can be immediately read (from STDIN) by the second process. In other words, the output of the first process will be sent as an input to the second process.

For example, suppose Desktop has four files pa08.c cars.txt toDo.txt assignment.md

The `ls` command will list all the files in the Desktop directory
<pre>
user@bash:~/Desktop$ ls 
pa08.c cars.txt toDo.txt assignment.md
</pre>

The `sort` in the following command will take the output of `ls` command as input and sort it alphabetically.
<pre>
user@bash:~/Desktop$ ls | sort
assignment.md
cars.txt
pa08.c
toDo.txt
</pre>

## Test Coverage (GCOV)

gcov is a test coverage program. Use it in concert with GCC to analyze your programs to help create more efficient, faster running code and to discover untested parts of your program. You can use gcov as a profiling tool to help discover where your optimization efforts will best affect your code. You can also use gcov along with the other profiling tool, gprof, to assess which parts of your code use the greatest amount of computing time.

Profiling tools help you analyze your code’s performance. Using a profiler such as gcov or gprof, you can find out some basic performance statistics, such as:
1-how often each line of code executes.
2-what lines of code are actually executed.
3-how much computing time each section of code uses.

Once you know these things about how your code works when compiled, you can look at each module to see which modules should be optimized. gcov helps you determine where to work on optimization.






# Implementation
In this exercise you will implement three functions, for three different regex formulas (A,B, and C from the Rules To Implement). IsInteger(), IsDouble(), and IsValidIdentifier().


1. `IsInteger()` - This function will return true if the passed string is an integer and false otherwise.
2. `IsDouble()` - This function will return true if the passed string is a double and false otherwise.
3. `IsValidIdentifier()` - This function will return true if the passed string is a vaild identifier and false otherwise.
4. `main()` - in the main file you will read the test file which has 'n' number of strings, and you will print on a file for each of the strings in the file 'Integer', 'Double', 'Identifier', or 'None' if the string does not match any of the rules. 

`HINT : You can use isdigit() to check if the passed character is a decimal digit character. And, isalpha() to check if the passed character is alphabetic`<br/> 

# Testing your code
Following are the files we provide:
1. `pe07.c` 
2. `pe07.h` 
3. `main.c`
4. `test.txt` - This file has n strings to match.

`NOTE : Each line in any test file is a single string`<br/> 

To test your code. You have to first compile it and then run one of the following commands. <br>

./pe07 testAll.txt <br/>
Match all strings in test.txt with all rules. Print "Integer".'Double', 'Identifier', or 'None' if the string does not match any of the rules. Expected output for this command in expOutAll.txt

./pe07 testInt.txt -I <br/>
"-I" To match all strings in test.txt with Integer rule. If it is integer, print "Integer". Otherwise,print "Not integer". Expected output for this command in expOutInt.txt

./pe07 testDbl.txt -D <br/>
"-D" To match all strings in test.txt with Double rule. If it is double, print "Double". Otherwise,print "Not double". Expected output for this command in expOutDbl.txt

./pe07 testVID.txt -VID <br/>
"-VID" To match all strings in test.txt with Vaild Identifier rule. If it is Identifier, print "Identifier". Otherwise, print "Not identifier". Expected output for this command in expOutVID.txt

# Submitting Your code
** This is a programming exercise, so you would have to submit the code on Blackboard.**

You have to submit the following file in a <strong>zip</strong> folder on the blackboard:
* `pe07.c` - This file should have `IsInteger()`, `IsDouble()`, and `IsValidIdentifier()`. functions implemented.
* `main.c` - This file should have `main()` function implemented.<br/>
* `cases.txt` - This file has at least 50 lines as a test input that you have to create.
* `OutCases.txt` - This file has the corresponding output for your cases. By running the following command <br>  `./pe07 cases.txt`

Type the following command to zip your file.
```bash
	zip pe07.zip pe07.c main.c cases.txt OutCases.txt
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

Your code will be tested as following : <br/>
1- 40 test cases using ./pe07 testAll.txt command line. 1 point for each test case.<br/>
2- 15 test cases ./pe07 testInt.txt -I/-D/-VID  each, sums up to 45 cases. 1 point for each test case.<br/>
3- 5 test cases for the main.c and Makefile. 1 point for each test case.<br/>
4- If you do not submit a test input, you will lose 10 points. If your expected output is wrong, you will lose at most 5 points.<br/>
**All Test cases will be released later.


