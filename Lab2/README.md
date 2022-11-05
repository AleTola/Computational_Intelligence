# Lab 2: Set Covering Problem

Given a number _N_ and some lists of integers _P_ = (L<sub>0</sub> , L<sub>1</sub>, L<sub>2</sub>,... L<sub>N </sub>), determine is possible _S_ = (L<sub>s0</sub>, L<sub>s1</sub>, L<sub>s2</sub>,... L<sub>sN</sub>) such that each number between 0 and (N-1) appears in at least one list and that the total numbers of elements in all _L<sub>si</sub>_ is minimum.


Report the the total numbers of elements in _L<sub>si</sub>_  for problem with N = [5, 10, 20, 100, 500, 1000] and the total number of nodes visited during the search (using seed=42).

# My approach

In my approach I have implemeneted a function _create_population_ that taken the number N create:
- the initial population with all the initial subsets, each one associated with its fitness
- the "simple" list of all the the subsets in the population
- the number of subset in the initial population

Then we have to choose the mutation rate (after testing with my implementation and N = (5, 10, 20, 100, 500, 1000) the best mutation rate is 0.55).

After that we start the GA algorithm with mutation and cross-over on the initial population. We redo the same algorithm for a number of generation that we can choose at the beginning. Bigger this number is better the results should be but for time reasons I have tried at maximum with _NUM_GENERATIONS_ = 500.

A mutation consists in replacing one subset in the list of subsets that is the genome of the individual taken into account with one subset from the _all_lists_ list of subsets. 

I have implemented cross-over in a way that we take the first part of the genome from _PARENT1_ and the second part of the genome of _PARENT2_. In my implementation the length of the offspring just created can be sligthly different from the length of the parents due to the randomness of the cuts in the parents genomes.

# TESTS

### NUM_GENERATIONS = 500

### mutation_rate = 0.55


        Solution for N=5: w=5 (bloat=0%)
        Solution for N=10: w=10 (bloat=0%)
        Solution for N=20: w=24 (bloat=20%)
        Solution for N=100: w=163 (bloat=63%)
        Solution for N=500: w=1362 (bloat=172%)
        Solution for N=1,000: w=3059 (bloat=206%)

time = 2m55s

------------------------------------------------------
### NUM_GENERATIONS = 250
### mutation_rate = 0.55

        Solution for N=5: w=5 (bloat=0%)
        Solution for N=10: w=10 (bloat=0%)
        Solution for N=20: w=24 (bloat=20%)
        Solution for N=100: w=163 (bloat=63%)
        Solution for N=500: w=1429 (bloat=186%)
        Solution for N=1,000: w=3115 (bloat=212%)

time = 1m34s

------------------------------------------------------
### NUM_GENERATIONS = 100
### mutation_rate = 0.55

        Solution for N=5: w=5 (bloat=0%)
        Solution for N=10: w=10 (bloat=0%)
        Solution for N=20: w=24 (bloat=20%)
        Solution for N=100: w=181 (bloat=81%)
        Solution for N=500: w=1431 (bloat=186%)
        Solution for N=1,000: w=3460 (bloat=246%)

time = 41s

------------------------------------------------------
### NUM_GENERATIONS = 100
### mutation_rate = 0.1

        Solution for N=5: w=5 (bloat=0%)
        Solution for N=10: w=10 (bloat=0%)
        Solution for N=20: w=28 (bloat=40%)
        Solution for N=100: w=204 (bloat=104%)
        Solution for N=500: w=1463 (bloat=193%)
        Solution for N=1,000: w=3596 (bloat=260%)

time = 37s

------------------------------------------------------
### NUM_GENERATIONS = 100
### mutation_rate = 0.2

        Solution for N=5: w=5 (bloat=0%)
        Solution for N=10: w=10 (bloat=0%)
        Solution for N=20: w=27 (bloat=35%)
        Solution for N=100: w=195 (bloat=95%)
        Solution for N=500: w=1390 (bloat=178%)
        Solution for N=1,000: w=3556 (bloat=256%)

time = 37s

------------------------------------------------------
### NUM_GENERATIONS = 100
### mutation_rate = 0.3

        Solution for N=5: w=5 (bloat=0%)
        Solution for N=10: w=11 (bloat=10%)
        Solution for N=20: w=24 (bloat=20%)
        Solution for N=100: w=181 (bloat=81%)
        Solution for N=500: w=1506 (bloat=201%)
        Solution for N=1,000: w=3596 (bloat=260%)

time = 37s

------------------------------------------------------
### NUM_GENERATIONS = 100
### mutation_rate = 0.4

        Solution for N=5: w=5 (bloat=0%)
        Solution for N=10: w=11 (bloat=10%)
        Solution for N=20: w=24 (bloat=20%)
        Solution for N=100: w=196 (bloat=96%)
        Solution for N=500: w=1527 (bloat=205%)
        Solution for N=1,000: w=3496 (bloat=250%)

time = 39s

------------------------------------------------------
### NUM_GENERATIONS = 100
### mutation_rate = 0.5

        Solution for N=5: w=5 (bloat=0%)
        Solution for N=10: w=10 (bloat=0%)
        Solution for N=20: w=28 (bloat=40%)
        Solution for N=100: w=188 (bloat=88%)
        Solution for N=500: w=1456 (bloat=191%)
        Solution for N=1,000: w=3416 (bloat=242%)

time = 40s

------------------------------------------------------
### NUM_GENERATIONS = 100
### mutation_rate = 0.6

        Solution for N=5: w=4 (bloat=-20%)
        Solution for N=10: w=10 (bloat=0%)
        Solution for N=20: w=24 (bloat=20%)
        Solution for N=100: w=183 (bloat=83%)
        Solution for N=500: w=1533 (bloat=207%)
        Solution for N=1,000: w=3619 (bloat=262%)

time = 40s