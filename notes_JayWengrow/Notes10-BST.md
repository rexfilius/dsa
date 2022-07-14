What do we do if we want a data structure that maintains order yet also has fast search, insertion, and deletion? Neither an ordered array nor a hash table is ideal - enter the binary search tree.

Trees come with their own unique nomenclature:
1. The uppermost node is called the root.
2. A node's descendants are all the nodes that stem from a node, while a node's ancestors are all the nodes that it stems from.
3. Trees are said to have levels. Each level is a row within the tree.
4. A tree is balanced when ts nodes' subtrees have the same number of nodes in it.

A BINARY TREE is a tree in which each node has zero, one, or two children.

A BINARY SEARCH TREE is a binary tree that also abides by the following rules:
1. Each node can have at most one 'left' child and one 'right' child.
2. A node's 'left' descendants can only contain values that are less than the node itself. Likewise, a node's 'right' descendants can only contain values that are greater than the node itself.

Efficiency of Search in a BST - O(logN) time, which is the apt description for any algorithm that eliminates half of the remaining values with each step. (this is only for a perfectly balanced binary search tree, which is a best-case scenario)

Another property about binary trees in general: if there are N nodes in a balanced binary tree, there will be about log N levels (that is, rows).

SIDE NOTE - searching a binary search tree has the same efficiency as binary search within an ordered array. Where binary search trees really shine over ordered arrays, though, is with insertion.

Insertion in a BST always takes just one extra step beyond a search, which means insertion takes (log N) + 1 steps. 
In Big O Notation, which ignores constants, this is O(log N).

It emerges that in a worst-case scenario, when a tree is completely imbalanced, search is O(N). In a best-case scenario, when it is perfectly balanced, search is O(log N). In the typical scenario, in which data is inserted in random order, a tree will
be pretty well balanced and search will take about O(log N).

Deletion algorithm for a BST:
1. if the node being deleted has no children, simple delete it
2. if the node being deleted has one child, delete the node and plug the child into the spot where the deleted node was
3. when deleting a node with two children, replace the deleted node with the successor node. The successor node is the child node whose value is the least of all values that are greater than the deleted node.
4. To find the successor node; visit the right child of the deleted value, and then keep on visiting the left child of each subsequent child until there are no more left children. The bottom value is the successor node.
5. if the successor node has a right child; after plugging the successor node into the spot of the deleted node, take the former right child of the successor node and turn it into the left child of the former parent of the successor node.

Efficiency of deletion in a BST is O(logN).

Visiting nodes is just another term for accessing them. The process of visiting every node in a data structure is known as traversing the data structure.

Inorder Traversal:
1. Call itself (traverse) recursively on the node’s left child. The function will keep getting called until we hit a node that does not have a left child.
2. “Visit” the node. (print the value of the node at this step.)
3. Call itself (traverse) recursively on the node’s right child. The function will keep getting called until we hit a node that does not have a right child.

