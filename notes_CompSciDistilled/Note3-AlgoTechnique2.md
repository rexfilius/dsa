many problems involve minimizing or maximizing a target value: find the shortest path, get the max profit etc. they are called optimization problems

when the solution is a sequence of choices, a strategy used is called branch and bound. its aim is to gain time by quickly detecting and discarding bad choices

to understand how bad choices are detected, there is the concept of upper and lower bounds

bounds refere to the range of a value
upper bound sets a limit on how high the value can be
lower bound is the least one can hope for, it guarantees the value is equal to it or greater

how branch and bound works:
1. divide the problems into subproblems
2. find the upper and lower bounds of each new subproblem
3. compare subproblem bounds of all branches
4. return to step 1 with the most promising subproblems

in backtracking, we remove paths after having explored them as as far as we can, and we stop when we are OK with a solution.
with branch and bound, we predict which paths are worst and we avoid wasting energy exploring them.

in software, procedural abstractions hide complexities of a process beneath a procedure call

we distinguish different types of data according to the operations that can be performed on the data