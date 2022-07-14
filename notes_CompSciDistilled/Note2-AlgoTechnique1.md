the iterative strategy consists in using loops to repeat a process until a condition is met. each step in a loop is called an iteration.

we say there's recursion when a function delegates work to clones of itself

recursive algos are generally simpler and shorter than iterative ones. recursion introduces computational overhead

to avoid overhead, recursive algos must be written in a purely iterative form. it's a trade, the iterative code generally runs faster  but it is also more complex and harder to understand

the brute force startegy solves problems by inspecting all of the problem's possible solution candidates. also known as exhaustive search, this strategy is usually naive and unskilled

power set - the collection of all subsets of S.

backtracking works best in problems where the solution is a sequence of choices and making a choice restrains subsequent choices.
it identifies as soon as possible the choices you've made cannot give you the solution you want, so you can sooner step back and try something else

heuristic -  a method that leads to a solution without guarateeing it is the best or optimal one

heristics can help when methods like brute force or backtracking are too slow. there are many heuristic approcahes aised backtarcking

greedy approach is a very common heuristics. it consists in never coming back to previous choices. it is the opposite of backtracking. try to make the best choice at each step, and don't question it later

problems with optimal sub0-structure can be cracked using divide and conquer strategy

problems with optimal sub-structure can be divided into smaller but smaller sub-problems. they can be divided over and over until sub-problems become easy. the subproblem solutions are combined for obtaining the original problem's solution

dynamic programming - identifying repeated subproblems in order to compute them only once.

memoization - the trick for reusing partial calculations.