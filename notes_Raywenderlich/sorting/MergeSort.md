**Merge sort** is one of the most efficient sorting algorithms. With a time complexity of O(n log n), it's one of the fastest of all general-purpose sorting algorithms. It is also a comaparison based algorithm. 

The idea behind merge sort is divide and conquer - to break a big problem into several smaller, easier-to-solve problems, and then combine those solutions into a final result. The merge sort mantra is to split first and merge after. 

Bubble, Selection and Insertion sort algorithms are in-place and use "swap" to move elements around. Merge sort, by contrast, allocates additional memory to do its work. Merge sort implementation requires O(n log n) of space.

`Coding Problem` 
1. Write a function that takes two sorted iterables and merges them into a single iterable.