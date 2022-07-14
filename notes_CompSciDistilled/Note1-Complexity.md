whenever you are dealing with things that assume one of two possibilities, remember they can be modeled as LOGIC VARIABLES.

a method is a list of unambiguous instructions for achieving a goal. A method that always requires a finite series of operations is called an algorithm.

time complexity is written - T(n)
it gives the number of operations the algoirithm performs when processing an inpit of size n.
an algorithm's T(n) is also its running cost

input size is not the only characteristic that impacts the number of operations required by an algo. when an algo can have different values of T(n) for the same value of n, we resort to cases.

best case: when the input requires the minimum number of operations for any input of that size. in sorting, it hapens when the input is already sorted

worst case: when the input requires the maximum number of operations for any input of that size. in many sorting algo, that is when the input was given in reverse order

average case: refers to the average number of operations required for typical inputs of that size. for sorting, an input in random order is usually considered

in general, the most important is the worst case. from there, you get a guaranteed baseline you can always count on.

say the input size of an algo is very large, and we increase it even more. to predict how the execution time will grow, we do not need to know all terms of T(n). We can approximate T(n)  by its fastest growing term, called the dominant term.

Big O notation - used for expressing the dominant term of an algo's cost functions in the worst case - that is the standard way of expressing time complexity

you need time complexity analysis when you design systems that handle very large inputs

when designing a computational system, it is important to anticipate the most frequent operations. then you can compare the Big-O costs of different algos that do these operations

most algos only work with specific input structures. if you choose your algos in advance, you can structure your input data accordingly

not-so-amazing time complexities:
1. exponential time O(2^n)
2. factorial time O(n!)
they are both horrible, but also needed for the hardest computational problems e.g the famous NP-complete problems

the measure for the working storage an algo needs is called space complexity

space complexity is similar to time complexity analysis. the difference is that we count computer memory, and not computing operations

computer memory limitations sometimes force a trade-off between space and time complexity

