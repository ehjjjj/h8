# HW08 grading policy

`- If you did not submit a functional makefile (produce executable "output file" with name pe10), you will lose 15% of your grade.` <br>
`- If you did not submit main.c, you will get zero` <br>
`- If you did not use the proper flags (i.e forgetting to use -Werror) while compiling may lead to compile error. Regrade is not possible for such cases`
`- If you print new line in josephus() not in print as mentioned in the instruction this will lead to extra line for each print, you may lose points because of it`

## print() function (10 points)
- To test your function we compiled your code with -DJOSEPHUS flag. Your print() function with our josephus() solution in pe10.obj2.
The command used for compiling is : 
`gcc -std=c99 -g -Wall -Wshadow --pedantic -Wvla -Werror -DJOSEPHUS pe10.obj2 main.c pe10.c -o pe10`
Then run the following command:
`./pe10 10 2 1 > sptest.txt`
- The correct output of this case is in ptest, your answer in sptest.txt, you can `diff` to find the error if there is any.


	
## createVID() function (50 points)
- To test this function we used three commands which are : 
<pre>
./pa08 -VID a a B B 3 3 4 | sort > svtest1.txt #(20 points) #right output in vtest1
./pa08 -VID a z A Z 1 9 1 | sort > svtest2.txt #(10 points) #right output in vtest2
./pa08 -VID g h M N 5 6 3 | sort > svtest3.txt #(20 points) #right output in vtest3
</pre>

The grade for each command is calculated similar to the createDouble() function.

# Testing your code

To test your code you have two options: <br>
1- run each command and `diff`. <br>
2- run the following command in the grading directory `python p.py`, which will create `yourGrade.txt` file that has detailed explanation of your grade. But you need to deduct 2 points per hour late yourself.



