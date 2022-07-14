Recursion is the term for a function calling itself. Indeed, infinite recursion, is utterly useless. When harnessed correctly, though, recursion can be a powerful tool.

In almost any case in which you can use a loop, you can also use recursion. Now, just because you can use recursion doesn't mean that you should use recursion. Recursion is a tool that allows for writing elegant code.

In recursion terminology, the case in which our function will
not recurse is known as the BASE CASE. Again, every recursive function needs at least one base case to prevent it from calling itself indefinitely.

The recursive process:
1. Identify the base case.
2. Walk through the function for the base case.
3. Identify the "next-to-last" case. This is the case just before the base case.
4. Walk through the function for the "next-to-last" case.
5. Repeat this process by identifying the case before the one you just analyzed, and walking through the function for that case.

Techniques to Recursion
1. Recursive Category: Repeatedly Execute - the goal of the algorithm is to repeatedly execute a task. Also to note - the "trick" of using extra function parameters is a common technique in writing recursive functions, and a handy one.
2. Recursive Category: Calculations - the algorithm performs a calculation based on a subproblem. A subproblem is a version of the very same problem applied to a smaller input.

When writing a function that makes a calculation, there are two potential approaches: 
1. we can try to build the solution from the "bottom up" or 
2. we can attack the problem going "top down" by making the calculation based on the problem's subproblem. 
Indeed, computer science literature refers to the terms bottom-up and top-down in regard to recursion strategies.

bottom-up: like using a loop to begin, and walking your way up.
top-down: using recursion.

Recursion shines when implementing a top-down approach because going top down offers a new mental strategy for tackling a problem. That is, a recursive top-down approach allows one to think about a problem in a completely different way.

Specifically, when we go top down, we get to mentally "kick the
problem down the road." We can free our mind from some of the nitty-gritty details we normally have to think about when going bottom up.

The Top-Down Thought Process
1. Imagine the function you're writing has already been implemented by someone else.
2. Identify the subproblem of the problem.
3. See what happens when you call the function on the subproblem and go from there.

