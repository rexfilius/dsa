Big O Notation - if there are N data elements, how many steps will the algorithm take?

The soul of Big O is what Big O is truly concerned about: how
will an algorithm’s performance change as the data increases?

While Big O effectively describes both the best- and worst-case
scenarios of a given algorithm, Big O Notation generally refers
to the worst-case scenario unless specified otherwise. 

This is why most references will describe linear search as being O(N) even though it can be O(1) in a best-case scenario.

This is because a “pessimistic” approach can be a useful tool:
knowing exactly how inefficient an algorithm can get in a worstcase scenario prepares us for the worst and may have a strong impact on our choices.

O(log N) is the Big O way of describing an algorithm that increases one step each time the data is doubled. Binary Search does just that.

O(log N) means the algorithm takes as many steps as it takes to keep halving the data elements until we remain with 1.
side-note = log is the inverse of exponent; 2^3=8, so log2 8=3.

Very often (but not always), when an algorithm nests one loop
inside another, the algorithm is O(N^2). So, whenever you see a
nested loop, O(N^2) alarm bells should go off in your head.

while Big O is perfect for contrasting algorithms that fall under different classifications of Big O, when two algorithms fall under the same classification, further analysis is required to determine which algorithm is faster.

also, Big O Notation only takes into account the highest order of N when we have multiple orders added together.




