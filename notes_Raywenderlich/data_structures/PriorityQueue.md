A Priority Queue does not use FIFO ordering, instead, elements are dequeued in priority order.

`Relevance`
1. when you need to identify the maximum or minimum value  within a list of elements
2. Dijkstra's algorithm
3. Heap sort.
4. Huffman coding

`Implementation`
1. using a heap (natural choice). [see Heap](obsidian://open?vault=Data_Structures_And_Algorithms&file=notes_Raywenderlich%2Fdata_structures%2FHeap)
2. using a sorted array
3. using a balanced binary search tree

`Common operations in a Priority Queue`
1. enqueue - inserts a value to the queue 
2. dequeue - removes the value with the highest priority 
3. peek - returns the value with the highest priority without removing it

`Complexity with operations on Priority Queue`
1. For heap based priority queue
enqueue, dequeue - O(logn) time
2. For array list based priority queue
dequeue - O(n) time
