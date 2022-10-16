# Lab 1: Set Covering

Given a number _N_ and some lists of integers _P_ = (L<sub>0</sub> , L<sub>1</sub>, L<sub>2</sub>,... L<sub>N </sub>), determine is possible _S_ = (L<sub>s0</sub>, L<sub>s1</sub>, L<sub>s2</sub>,... L<sub>sN</sub>) such that each number between 0 and (N-1) appears in at least one list and that the total numbers of elements in all _L<sub>si</sub>_ is minimum.


Report the the total numbers of elements in _L<sub>si</sub>_  for problem with N = [5, 10, 20, 100, 500, 1000] and the total number of nodes visited during the search (using seed=42).

# My approach


There is a greedy algorithm for polynomial time approximation of set covering that chooses sets according to one rule: 
at each stage, choose the set that contains the largest number of uncovered elements. Inapproximability results show that the greedy algorithm is essentially the best-possible polynomial time approximation algorithm for set cover up to lower order terms

https://en.wikipedia.org/wiki/Set_cover_problem


# My results with Greedy Algorithm

N = 5

    weigth =  5
    time:  0.1 s
    nodes:  4

N = 10

    weigth =  11
    time:  0.2 s
    nodes:  4

N = 20

    weigth =  24
    time:  0.3 s
    nodes:  4

N = 100

    weigth =  182
    time:  0.5 s
    nodes:  8
 
N = 500

    weigth =  1262
    time:  0.5 s
    nodes:  11

N = 1000

    weigth =  2878
    time:  2.2 s
    nodes:  13