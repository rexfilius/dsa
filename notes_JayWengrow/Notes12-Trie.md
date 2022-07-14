The Trie (-try-) is a kind of tree that is ideal for text-based features such as autocomplete. Trie is also known as Prefix Tree or Digital Tree.

Like most other trees, the trie is a collection of nodes that point to other nodes. However, the trie is not a binary tree. Whereas a binary tree doesn't allow any node to have more than two child nodes, a trie node can have any number of child nodes.

Implementing Tries = each trie node contains a hash table, where the keys are English characters and the values are other nodes of the trie. These children also contain hash tables, which will in turn point to their children.

<u>Trie Search</u>
The most classic trie operation is search, namely, determining whether a string is found in the trie. There are two flavors of search: 
1. we can search to see whether the string is a complete word, or
2. we can search to see whether the string is at least a word prefix i.e. the beginning of a word.

The algorithm for prefix search performs the following steps:
1. We establish a variable called currentNode. At the beginning of our algorithm, this points to the root node.
2. We iterate over each character of our search string.
3. As we point to each character of our search string, we look to see if the currentNode has a child with that character as a key.
4. If it does not, we return None, as it means our search string does not exist in the trie.
5. If the currentNode does have a child with the current character as the key, we update the currentNode to become that child. We then go back to Step 2, continuing to iterate over each character in our search string.
6. If we get to the end of our search string, it means we've found our search string.

<u>Efficiency of a Trie Search</u>
Expressing trie search in terms of Big O is slightly tricky. We
can't quite call it O(1), since the number of steps isn’t constant, as it all depends on the search string’s length. 

And O(N) can be misleading, since N normally refers to the amount of data in the data structure. This would be the number of nodes in our trie, which is a much greater number than the number of characters in our search string.

Most references have decided to call this O(K), where K is the number of characters in our search string.

Even though O(K) isn't constant, as the size of the search string can vary, O(K) is similar to constant time in one important
sense. 

Most non-constant algorithms are tied to the amount of data at hand. That is, as N data increases, the algorithm slows down. With an O(K) algorithm, though, our trie can grow tremendously, but that will have no affect on the speed of our search. 

An O(K) algorithm on a string of three characters will always take three steps, no matter how large the trie is. The only factor that affects our algorithm’s speed is the size of our input, rather than all the available data. This makes our O(K) algorithm extremely efficient.

<u>Trie Insertion</u>
Inserting a new word into a trie is similar to searching for an existing word. Here's how the algorithm goes:
1. We establish a variable called currentNode. At the beginning of our algorithm, this points to the root node.
2. We iterate over each character of our search string.
3. As we point to each character of our search string, we look to see if the currentNode has a child with that character as a key.
4. If it does, we update the currentNode to become that child node and we go back to Step 2, moving on to the next character of our search string.
5. If the currentNode does not have a child node that matches the current character, we create such a child node and update the currentNode to be this new node. We then go back to Step 2, moving on to the next character of our search string.
6. After we insert the final character of our new word, we add a (asterisk*) child to the last node to indicate the word is complete.

Like search, trie insertion takes about O(K) steps. If we count
the adding of the (asterisk*) at the end, it’s technically K + 1 steps, but because we drop the constants, we express the speed as O(K).

