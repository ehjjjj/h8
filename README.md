
# HW12 grading policy
<strong>  &nbsp; &nbsp; &nbsp;   &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;  &nbsp;  &nbsp; \*\*\*ATTENTION : Read it to the last line before sending any email\*\*\* </strong> </br> <br>
`- If you did not use the proper flags (i.e forgetting to use -Werror -Wvla) while compiling may lead to compile error. Regrade is not possible for such cases`

<br/>

<strong>Please copy the main.c and pa12.c you submitted to this directory</strong>

## init() function (10 points)
\- To test your function we compiled your code based on your implementation using one of the following commands:</br>

<strong>Non-circular single linkedlist "tail->next=NULL"</strong> </br>
`gcc -std=c99 -g -Wall -Wshadow --pedantic -Wvla -Werror -DPRINT -DINITII -DPRINTII -DJOSPI -DJOSPII main.c pa12.c ./cases/testINT.obj -o pa12`</br> 

<strong>Circular single linkedlist "tail->next=head"</strong> </br>
`gcc -std=c99 -g -Wall -Wshadow --pedantic -Wvla -Werror -DPRINT -DINITII -DPRINTII -DJOSPI -DJOSPII main.c pa12.c ./cases/testINITC.obj -o pa12`</br> 

\- Then run the following command:</br>
`./pa12 -J 10 5 1 > scase1.txt`</br>
\- The correct output of this case is in `./cases/case1`. <br>
\- To calculate your grade: count the number of different lines (x). your grade=10-(x/9)\*10. </br>

	
## print() function (10 points)
\- To test your function we compiled your code based on your implementation using one of the following commands:</br>

<strong>Non-circular single linkedlist "tail->next=NULL"</strong> </br>
`gcc -std=c99 -g -Wall -Wshadow --pedantic -Wvla -Werror -DINIT -DINITII -DPRINTII -DJOSPI -DJOSPII main.c pa12.c ./cases/testPRINT.obj -o pa12`</br> 

<strong>Circular single linkedlist "tail->next=head"</strong> </br>
`gcc -std=c99 -g -Wall -Wshadow --pedantic -Wvla -Werror -DINIT -DINITII -DPRINTII -DJOSPI -DJOSPII main.c pa12.c ./cases/testPRINTC.obj -o pa12`</br> 

\- Then run the following command:</br>
`./pa12 -J 10 5 1 > scase1.txt`</br>
\- The correct output of this case is in `./cases/case1`. <br>
\- To calculate your grade: count the number of different lines (x). your grade=10-(x/9)\*10. </br>

## josp() function (80 points)
\- To test your function we compiled your code based on your implementation using one of the following commands:</br>

<strong>Non-circular single linkedlist "tail->next=NULL"</strong> </br>
`gcc -std=c99 -g -Wall -Wshadow --pedantic -Wvla -Werror -DINIT -DPRINT -DINITII -DPRINTII -DJOSPII main.c pa12.c ./cases/testJOSPC.obj -o pa12`</br> 

<strong>Circular single linkedlist "tail->next=head"</strong> </br>
`gcc -std=c99 -g -Wall -Wshadow --pedantic -Wvla -Werror -DINIT -DPRINT -DINITII -DPRINTII -DJOSPII main.c pa12.c ./cases/testJOSP.obj -o pa12`</br> 

\-This function has four test cases 20 each.
- case1:  "./pa12 -J 10 5 1 > scase1.txt". The correct output of this case is in `./cases/case1`. Grade_Case1=20-(x/9)\*20. </br>
- case2:  "./pa12 -J 20 2 2 > scase2.txt". The correct output of this case is in `./cases/case2`. Grade_Case2=20-(x/9)\*20.</br>
- case3:  "./pa12 -J 40 10 3 > scase3.txt". The correct output of this case is in `./cases/case3`. Grade_Case2=20-(x/13)\*20.</br>
- case4:  "./pa12 -J 60 30 3 > scase4.txt". The correct output of this case is in `./cases/case4`. Grade_Case2=20-(x/19)\*20.</br>


## Late penalty
- You will lose 2 points per hour late.




