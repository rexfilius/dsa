A Queue is a FIFO data structure.

`Implementation`
1. Using an array based list
2. Using a doubly linked list
3. Using a ring buffer
4. Using two stacks

`Common Operations in a Queue`
1. enqueue : inserts a value at the back of the queue 
2. dequeue : removes a value at the front of the queue 
3. peek : returns the value at the front of the queue without removing it

`Complexity with operations on Queue`
1. For array list queue:
enqueue - O(1) time. O(n) space 
dequeue - O(n) time and space 
peek - O(1) time 
2. For doubly linked list queue:
enqueue, dequeue - O(1) time and O(n) space
3. For ring buffer queue:
enqueue, dequeue - O(1) time and space
4. For stack based queue:
enqueue - O(1) time. O(n) space 
dequeue, peek - amortized O(1) time. O(n) space

`Coding Problems`
Finding the next player in a board game
Reverse the content of a queue