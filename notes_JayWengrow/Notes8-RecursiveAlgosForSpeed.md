<u>QuickSort</u>
Quicksort is an extremely fast sorting algorithm that is particularly efficient for average scenarios. 

While in worst-case scenarios (that is, inversely sorted arrays), it performs similarly to Insertion Sort and Selection Sort, it is much faster for average scenarios - which are what occur most of the time.

Quicksort relies on a concept called partitioning.

The Quicksort algorithm is a combination of partitions and recursion. It works as follows:
1. Partition the array. The pivot is now in its proper place.
2. Treat the subarrays to the left and right of the pivot as their own arrays, and recursively repeat Steps 1 and 2. That means we'll partition each subarray and end up with even smaller sub-subarrays to the left and right of each subarray’s pivot. We then partition those subsubarrays, and so on and so forth.
3. When we have a subarray that has zero or one elements, that is our base case and we do nothing.

Quicksort is O(nlogN) time. In a worst-case scenario, Quicksort has an efficiency of O(N^2).

MergeSort is another recursive algorithm that has O(nlogN) time.