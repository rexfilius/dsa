While recursion can certainly solve some problems, it can also create new ones if not used properly. In fact, recursion is often the culprit behind some of the slowest categories of Big O, such as O(2^N).

avoiding extra recursive calls is key to keeping recursion fast.

When a problem is solved by solving smaller versions of the same problem, the smaller problem is called a subproblem.

Dynamic programming is the process of optimizing recursive problems that have overlapping subproblems.

Optimizing an algorithm with dynamic programming is typically
accomplished with one of two techniques.
1. Memoization = it reduces recursive calls by remembering previously computed functions. With memoization, each time we make a new calculation, we store it in the hash table for future use. This way, we only make a calculation if it hadn’t ever been made before.
2. Going bottom-up = means to ditch recursion and use some other approach (like a loop) to solve the same problem.

The reason that going bottom-up is considered part of dynamic programming is because dynamic programming means taking a problem that could be solved recursively and ensure that it doesn't make duplicate calls for overlapping subproblems.

Using iteration (that is, loops) instead of recursion is, technically, a way to achieve this.

Going bottom-up becomes more of a "technique" when the problem is more naturally solved with recursion.

<u>Memoization vs Bottom-Up</u>
Is one technique better than the other?

Usually, it depends on the problem and why you're using recursion in the first place.

If recursion presents an elegant and intuitive solution to a given problem, you may want to stick with it and use memoization to deal with any overlapping subproblems.

However, if the iterative approach is equally intuitive, you
may want to go with that.

It’s important to point out that even with memoization, recursion does carry some extra overhead versus iteration. Specifically, with any recursion, the computer needs to keep track of all
the calls in a call stack, which consumes memory. 

The memoization itself also requires the use of a hash table, which will take up additional space on your computer as well.

Generally speaking, going bottom-up is often the better choice
unless the recursive solution is more intuitive. Where recursion is more intuitive, you can keep the recursion and keep it fast by using memoization.

