<u>Linked List</u>
A Linked List is a collection of values arranged in a linear, unidirectional sequence.

Like an array, a linked list is a data structure that represents a list of items. While on the surface, arrays and linked lists look and act quite similarly, there are big differences under the hood.

Instead of being a contiguous block of memory, the data from linked lists can be scattered across different cells throughout the computer's memory.

Connected data that is dispersed throughout memory are known as nodes. In a linked list, each node represents one item in the list. 

The big question is: if the nodes are not next to each other in memory, how does the computer know which nodes are part of the same linked list?

This is the key to the linked list: each node also comes with a little extra information, namely, the memory address of the next node in the list.
This extra piece of data - this pointer to the next node’s memory address - is known as a link.

A linked list's first node can also be referred to as its head, and
its final node as its tail.

The fact that a linked list's data can be spread throughout the computer’s memory is a potential advantage it has over the array. An array, by contrast, needs to find an entire block of contiguous cells to store its data, which can get increasingly difficult as the array size grows.

<u>Operations on a Linked List</u>
1. Read - O(N) time.
2. Search - O(N) time
3. Insert - Insertion is one operation in which linked lists have a distinct advantage over arrays in certain situations. Insertion at the beginning takes O(1) time. Worst case is inserting at the end which is O(N) time.
4. Delete - deleting from the beginning or end of a linked list is straightforward, O(1)time. Deleting from anywhere in the middle is slightly more involved, O(N) time.

SIDE NOTE - Arrays favor insertions at the end, while Linked Lists favor insertions at the beginning.

SIDE NOTE - Whenever we delete a node from our linked list, the node still exists in memory somewhere. We're just removing the node from our list by ensuring that no other node from the list links to it. This has the effect of deleting the node from our list, even if the node still exists in memory.
(Different programming languages handle these deleted nodes in various ways. Some will automatically detect that they’re not being used and will "garbage collect" them, freeing up memory.)

ON THE BRIGHT SIDE - Linked Lists are an amazing data structure for moving through an entire list while making insertions or deletions, as we never have to worry about shifting other data (like in Arrays) as we make an insertion or deletion.

***
<u>Doubly Linked List (DLL)</u>
A doubly linked list is like a linked list except where each node has two links - one that points to the next node, and another that points to the previous node.

In addition, the doubly linked list always keeps track of both the first and last nodes, instead of just the first node.

Since a doubly linked list always knows where both its first and last nodes are, we can access each of them in a single step, or O(1). So, just as we can read, insert, or delete from the beginning of the list in O(1), we can do the same from the end of the list in O(1) as well.

With a 'classic' linked list, we can only move forward through the list. That is, we can access the first node and follow the links to find all the other nodes of the list. But we’re not able to move backward, as no node is aware of what the previous node is.

A doubly linked list allows for a lot more flexibility, as we can move both forward and backward through the list. In fact, we can even start with the last node and work our way backward to the first node.

SIDE NOTE - Because doubly linked lists have immediate access to both the front and end of the list, they can insert data on either side at O(1) as well as delete data on either side at O(1). This makes DLL a perfect underlying data structure for a queue.
