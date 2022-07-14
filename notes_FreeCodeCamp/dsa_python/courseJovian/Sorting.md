The problem of sorting a list of objects comes up over and over in computer science and software development, and it's important to understand common appproaches for sorting , and the trade-offs they offer. 

Sorting usually refers to  'sorting in ascending order', unless specified otherwise.

<u>Bubble Sort</u>
1. Iterate over the list of numbers, starting from the left.
2. Compare each number with the number that follows it.
3. If the number is greater than the one that follows it, swap the two elements.
4. Repeat steps 1 to 3 till the list is sorted.

Step 1 to 3 will be repeated at most 'n-1' times to ensure the array/list is sorted.

Time complexity of bubble sort is O(n^2)

the ineffiency in a bubble sort comes from the fact that we're shifting elements by at most one position at a time

<u>Insertion Sort</u>
In insertion sort, we keep the initial portion of the array sorted and insert the remaining elements one by one at the right position.

<u>Divide-n-Conquer</u>
To perform sorting more efficiently, you can apply a strategy called 'Divide-n-Conquer', which has the following general steps
1. Divide the inputs into two roughly equal parts
2. Recursively solve the problem individually for each of the two parts
3. Combine the results to solve the problem for the original inputs 
4. Include terminating conditions for small or indivisible inputs

<u>Merge Sort</u>
Merge Sort is the classic application of Divide-n-Conquer, and here is a step-by-step description
1. if the input is empty or contains just one element, it is already sorted, return it
2. if not, divide the list into two roughly equal parts
3. sort each part recursively, using the merge sort algorithm. You'll get back two sorted lists
4. merge the two sorted lists to get a single sorted list

Time complexity of Merge Sort is O(n logN).
Space complexity of Merge Sort is O(n).

The fact that merge sort requires allocating additional space as large as the input itself makes it somewhat slow in practice because memory allocation is far more expensive than comparisons or swapping.

<u>Extensions of Merge Sort</u>
1. K-way merge sort [Wikipedia](https://en.wikipedia.org/wiki/K-way_merge_algorithm)
2. Merge sort and insertion sort hybrid [Wikipedia](https://en.wikipedia.org/wiki/Timsort)
3. Counting inversions in an array [geeksforgeeks](https://www.geeksforgeeks.org/counting-inversions/)

<u>Quick Sort</u>
Quick Sort is another divide-n-conquer based algorithm. It overcomes the space inefficiencies of merge sort.

QuickSort sorts the list in place i.e it does not create a copy of the list internally for sorting inside each operation

It works as follows:
1. if the list is empty or has just one element, return it. It's already sorted
2. pick a random element from the list. this element is called a 'Pivot'
3. reorder the list so that all elements with values less than or equal to the pivot come before the pivot, while all elements with values greater than the pivot come after it. This operation is called 'Partitioning'
4. the pivot element divides the array/list into two parts which can be sorted independently by making a recursive call to quickSort.

Quick Sort is faster than merge sort for larger lists because it is not allocating a new space.

Time complexity of quick sort is O(n logN) - average case - if you are able to partition the list into two nearly equal parts. 
Worst case time for quick sort is O(n^2).

Despite the quadratic worst case time complexity of QuickSort, it is preferred in many situations because its running time is closer to O(n logN) in practice, especially with a good strategy for picking a pivot. Some of these are:
1. picking a random pivot
2. picking median of medians

...
