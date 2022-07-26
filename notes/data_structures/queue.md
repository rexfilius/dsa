<u>Queue</u>
A queue is another data structure designed to process temporary data. It’s like a stack in many ways, except that it processes data in a different order. 

Like a stack, a queue is also an abstract data type.
You can think of a queue as a line of people at the movie theater.
The first one in the line is the first one to leave the line and enter
the theater. 

With queues, the first item added to the queue is the first item to be removed. That’s why computer scientists apply the acronym “FIFO” to queues: First In, First Out.

Like stacks, queues are arrays with three restrictions:
1. Data can be inserted only at the end of a queue.
2. Data can be deleted only from the front of a queue.
3. Only the element at the front of a queue can be read.

<u>Implementing a Queue</u>
1. Using an array based list
2. Using a doubly linked list
3. Using a ring buffer
4. Using two stacks

<u>Operations on a Queue</u>
1. enqueue : inserts a value at the back of the queue 
2. dequeue : removes a value at the front of the queue 
3. peek : returns the value at the front of the queue without removing it

Queues are common in many applications, ranging from printing jobs to background workers in web applications.

Queues are also the perfect tool for handling asynchronous requests - they ensure that the requests are processed in the order in which they were received. They are also commonly used to model real-world scenarios where events need to occur in a certain order, such as airplanes waiting for takeoff and patients waiting for their doctor.

***
<u>Priority Queue</u>
A Priority Queue does not use FIFO ordering, instead, elements are dequeued in priority order.

A priority queue can be used, when you need to identify the maximum or minimum value  within a list of elements. It is also used in Dijkstra's algorithm, Heap Sorting and Huffman coding.

A Priority Queue is a list whose deletions and access are just like a classic queue, but whose insertions are like an ordered array. That is, we only delete and access data from the front of the priority queue, but when we insert data, we always make sure the data remains sorted in a specific order.

On Array-based priority queue; deletions are O(1) - end of array, is front of priority queue -  and insertions are O(N). If we expect there to be many items in our priority queue, the O(N) insertions may cause some real unwanted drag in an application.

A heap is a better structure for implementing a Priority Queue.

<u>Implementing a PriorityQueue</u>
1. using a heap (natural choice)
2. using a sorted array
3. using a balanced binary search tree

<u>Operations on a Priority Queue</u>
1. enqueue - inserts a value to the queue 
2. dequeue - removes the value with the highest priority 
3. peek - returns the value with the highest priority without removing it