Radix Sort is a non-comparative algorithm for sorting integers in linear time. 

There are many implementations of radix sort that focus on different problems. A particluar implementation focuses on sorting base 10 integers while investigating the least significant digit (LSD) variant of radix sort. 

Radix sort is one of the fastest sorting algorithms. The average time complexity is O(k × n), where k is the number of significant digits of the largest number, and n is the number of integers in the list. 

Radix sort works best when k is constant, which occurs when all numbers in the list have the same count of significant digits. Its time complexity then becomes O(n). 

Radix sort also incurs an O(n) space complexity, as you need space to store each bucket. 

`Coding problem` 
1. Lexicographical sorting - most significant digit (MSD) radix sort