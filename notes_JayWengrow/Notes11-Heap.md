Heap; a type of tree data structure that has special powers that can be leveraged for specific scenarios, in particular when we want to constantly keep tabs on the greatest or least data element in a dataset.

A Priority Queue is a list whose deletions and access are just like
a classic queue, but whose insertions are like an ordered array. That is, we only delete and access data from the front of the priority queue, but when we insert data, we always make sure the data remains sorted in a specific order.

On Array-based priority queue deletions are O(1) - end of array, is front of priority queue -  and insertions are O(N). If we expect there to be many items in our priority queue, the O(N) insertions may cause some real unwanted drag in an application.

Heap is a better structure for implementing a Priority Queue.

There are several different kinds of heaps, of which Binary Heap is a type.

The binary heap is a specific kind of binary tree. As a reminder,a binary tree is a tree where each node has a maximum of two
child nodes.

Binary heaps come in two flavors: the max-heap and
the min-heap.

The heap is a binary tree that maintains the following
conditions:
1. The value of each node must be greater than each of its descendant nodes. (otherwise for a min-heap)
2. The tree must be complete.

A complete tree is a tree that is completely filled with nodes; no nodes are missing. So, if you read each level of the tree from left
to right, all of the nodes are there. However, the bottom row can have empty positions, as long as there aren’t any nodes to the
right of these empty positions.

Heaps are said to be weakly ordered as compared to BSTs. While heaps have some order, as descendants cannot be greater than their ancestors, this isn't enough order to make heaps worth searching through.

In a heap, the root node will always have the greatest value. (In a min-heap, the root will contain the smallest value.)

The heap has two primary operations: inserting and deleting. 

Searching within a heap would require us to inspect each node, so search is not an operation usually implemented in the context of heaps. (A heap can also have an optional "read" operation, which would simply look at the value of the root node.)

A heap's last node is the rightmost node in its bottom level.

Heap insertion algorithm:
1. We create a node containing the new value and insert it at the next available rightmost spot in the bottom level. Thus, this value becomes the heap's last node.
2. Next, we compare this new node with its parent node.
3. If the new node is greater than its parent node, we swap the new node with the parent node.
4. We repeat Step 3, effectively moving the new node up through the heap, until it has a parent whose value is greater than it.

This process of moving the new node up the heap, is called
TRICKLING the node up through the heap. Sometimes it moves up to the right, and sometimes it moves up to the left, but it always moves up until it settles into the correct position.

The efficiency of inserting into a heap is O(log N).

The first thing to know about deleting a value from a heap is that we ONLY ever delete the root node. This is right in line with the way a priority queue works, in that we only access and remove the highest-priority item.

Heap Deletion Algorithm:
1. Move the last node into where the root node was, effectively removing the original root node.
2. Trickle the root node down into its proper place.

The algorithm for trickling down a node after a Heap Deletion:
1. We check both children of the trickle node and see which one is larger.
2. If the trickle node is smaller than the larger of the two child nodes, we swap the trickle node with that larger child.
3. Repeat Steps 1 and 2 until the trickle node has no children who are greater than it.

NOTE = The reason why we always swap the trickle node with the greater of its two children is because if we swap it the with the smaller one, we'd end up violating the heap condition immediately.

The efficiency of deletion in a heap is O(log N).

Because finding the last node is so critical to the heap's operations, and we want to make sure that finding the last node is efficient, heaps are usually implemented using arrays.

It turns out that the heap's weak ordering is its very advantage.
The fact that it doesn't have to be perfectly ordered allows us to
insert new values in O(log N) time. At the same time, the heap is
ordered just enough so that we can always access the one item
we need at any given time - the heap’s greatest value.

<u>Heap Sort</u>
Heapsort is a sorting algorithm that inserts all the values into a heap, and then pops each one; which makes the values end up in sorted order. Heapsort is O(nlogN).









