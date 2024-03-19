# Ex.No: 6   Logic Programming – Tower of Hanoi 
### DATE:                                                                            
### REGISTER NUMBER : 212221040109
### AIM: 
To  write  a logic program  to solve Towers of Hanoi problem  using SWI-PROLOG. 
### Algorithm:
1. Start the program
2.  Write a rules for finding solution of Towers of Hanoi in SWI-PROLOG.
3.  a )	If only one disk  => Move disk from X to Y.
4.  b)	If Number of disk greater than 0 then
5.        i)	Move  N-1 disks from X to Z.
6.        ii)	Move  Nth disk from X to Y
7.        iii)	Move  N-1 disks from Y to X.
8. Run the program  to find answer of  query.

### Program:
```py

hanoi(1, Source, _, Target) :-
    format('Move disk from ~w to ~w~n', [Source, Target]).

hanoi(N, Source, Auxiliary, Target) :-
    N > 1,
    M is N - 1,
    hanoi(M, Source, Target, Auxiliary),
    hanoi(1, Source, _, Target),
    hanoi(M, Auxiliary, Source, Target).
```


### Output:

![image](https://github.com/nagaraj6618/AI_Lab_2023-24/assets/127173574/6cee3331-a593-4562-864d-2c43ed451f6a)


### Result:
Thus the solution of Towers of Hanoi problem was found by logic programming.
