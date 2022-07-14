A binary tree is called a tree because it vaguely looks like an inverted tree trunk with branches
1. the word binary indicates that each node in the tree can have at most 2 children (left or right)
2. nodes can have 0, 1, or 2 children. Nodes that do not have any children are sometimes also called 'leaves'
3. the single node at the top is called the 'root' node, and it's typically where operations like search, insertion etc. begin

A binary tree can have additional properties to make it more efficient:
1. keys and values - each node of the tree stores a key and a value. A binary tree where nodes have both a key and a value is often referred to as a map or treemap.
2. binary search tree - the left subtree of any node only contains nodes with keys that are lexicographically smaller than the node's key, and the right subtree of any node only contains nodes with keys that are lexicographically larger than the node's key. A tree that satisfies this property is called a BST, and it is easy to locate a specific key by traversing a single path down from the root node
3. Balanced Tree - by balanced, we mean, it does not skew too heavily to one side or the other. The left and right subtrees of any node should not differ in height/depth by more than 1 level.

Height of a binary tree - the number of levels in a tree.
The height/depth of a binary tree is defined as the length of the longest path from its root node to a leaf.

To store N records, we require a balanced binary search tree of height no larger than 'log(N) + 1' this is a very useful property, in combination with the fact that nodes are arranged in a way that makes it easy to find a specific key by following a single path down the root.

Also, the insert, find, and update operations in a balanced BST have time complexity O(logN) since they all involve traversing a single path down from the root of the tree.

Binary trees form the basis of many modern programming language features (maps in C++ and Java) and data storage systems (filesystem indexes, relational databases like MySQL).

<u>Traversing A Binary Tree</u>
A Traversal refers to the processs of visiting each node of a tree exactly once. Visiting a node generally refers to adding the node's key to a list. 3 ways to traverse - inorder, preorder, postorder.

In-order Traversal
1. traverse the left subtree recursively inorder
2. traverse the current node
3. traverse the right subtree recursively inorder

Pre-order traversal
1. traverse the current node
2. traverse the left subtree recursively preorder
3. traverse the right subtree recursively preorder

Post-order traversal (My understanding)
1. traverse the left subtree resursively postorder
2. traverse the right subtree recursively postorder
3. traverse the current node

<u>Binary Search Tree</u>
A BST is a binary tree that satisfies the following conditions
1. the left subtree of any node only contains nodes with keys less than the node's key
2. the right subtree of any node only contains nodes with keys greater than the node's key

It follows that every subtree of a BST must also be a BST.

Inserting a node in a BST - The order of insertion of nodes affects the structure of the tree, which could result in an unbalanced tree.

Finding a node in a BST -  the length of the path followed by 'find' is equal to the height of the tree (in the worst case). Thus it has a similar time complexity as 'insert'.

Update a node in a BST - time complexity of this is same as 'find'.

Case: write a function to retrieve all the key-value pairs stored in a BST in the sorted order of keys. (Just another way to write inorder traversal)

Complexity of the various operations is a balanced BST:
1. Insert - O(N)
2. Find - O(logN)
3. Update - O(logN)
4. List all - O(N)

To speed up insertions in a BST, we may choose to perform the balancing periodically (e.g. once every 1000 insertions). This way, most insertions will be O(logN), but every 1000th insertion will take a few seconds

<u>Self Balancing Binary Tree</u>
A self-balancing binary tree remains balanced after every insertion or deletion.

There have been lots of approaches to a self-balancing binary tree, some are; B-Trees, Red Black Trees and AVL trees (Adelson-Velsky Landis)

<u>AVL Tree</u>
Balance Factor - the difference between the height of the left subtree and right subtree

Self-balancing in an AVL tree is achieved by tracking the balance factor for each node and rotating unbalanced subtrees along the path of insertion/deletion to balance them.

In a balanced BST, the balance factor of each node is either 0, -1, or 1. When we perform an insertion, then the balance factor of certain nodes along the path of insertion may change to 2 or -2. These nodes can be 'rotated' one-by-one to bring the balance factor to 1, 0 or -1.

The balance factor in an AVL tree has 4 cases:
1. Left right case
2. Right left case
3. Left Left case
4. Right Right case

Since each rotation takes constant time, and at most 'logN' rotations may be required, this operation is far more efficient than creating balanced binary tree from scratch, allowing insertion and deletion to be performed in 'O logN' time

<u>Common Coding challenge on Binary Trees</u>
1. Implement rotations and self-balancing insertion
2. Implement deletion of a node from  a binary search tree
3. Implement deletion of a node from a BST (with balancing)
4. Find the lowest common ancestor of two nodes in a tree (hint: use the parent property)
5. Find the next node in lexicographic order for a given node.
6. Given a number k, find the k-th node in a BST.


