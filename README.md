# Theorem-Prover-Logic-Programming
Theorem Prover for Propositional Logic

## Overview
------------------------------------------------------------------------
The submission code contains :-
1. A natural deduction theorem prover.
2. A resolution refutation theorem prover. 

A Report PDF is also attached in the submission

Natural deduction was based on priority tasks that need to be done before and extensive case handling,
along with BFS(We did not apply bind BFS, but we defined some priorities while doing s0)

Resolution Refutation was done using Resolution Algo discussed in class. First the KB is converted into CNFs, then using A* algo 2  best CNFs(decided by heuristic) 
and then resolution rule is applied over them. the resultant clause is added in the KB.
                                     

Note: for Handling of Brackets and representing Propositions and clauses Abstract Syntax Tree (ASTs) via Stacks 
were used


Libs Used/ Pre-requites of system:-
------------------------------------------------------------
python ,sys, re, heapq, collections

ensure all the relevant modules are present and if not install them using pip install <module name>


## Input Format
---------------------------------------------------------------------------
- The first line contains two integers, {`n` : number of formulas in the KB} and {m: number of propositions i.e. the number of literals or symbols}.
- Then in the next n lines contains n known premises (Knowledge base). format of each line S[num]: ------
- Last line is of the format Query: ------ which contains query to be proved

Run :
python <filename>.py


Some Sample Inputs with n={5,6,7,8} and m={5,6,7,8} as per the Tasks:-
One can run the code with these inputs , I have run them and pasted the results in the report.

Sample Inputs:-
----------------------------------------------------------------------------------

4 4			
S1: P|(Q&(R>T))
S2: P>R
S3: Q>T
S4: Q>(R=T)
Query: R

5 6
S1: A|(B&(C>D))
S2: A>B
S3: B>C
S4: C>D
S5: A>(E=F)
Query: D

6 7
S1: X|(Y&(Z>W))
S2: Y>X
S3: Z>W
S4: W>(X=Z)
S5: X>Y
S6: Y|(Z&X)
Query: X

5 5 
S1: P&Q>R
S2: S&T>Q
S3: P
S4: T
S5: S
Query: R



## For Analysis of the Implementations( for checking nodes explored, time taken)
------------------------------------------------------------------------------

-There are two main functions. The first one is for Analysis of Algorithm and 
the second one is for taking normal input as mentioned in the sample input/output of the question.

- So for Analysis of the implementation uncomment the first main function and comment-out the second.
The parts where to comment and uncomment are mentioned in code comments as well.

- Also Analysis is done on  number of queries written in a query list in the code for different values of n, m and Kbs.


@ Author:  Yashraj Chaturvedi (B22AI059)  (b22ai059@iitj.ac.in)
@ This work was done for AI course assignment in Autumn 2024, IIT-Jodhpur
