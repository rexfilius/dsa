<u>Stack</u>
A Stack is a LIFO data structure. Stacks are crucial to problems that search trees and graphs

A stack stores data in the same way arrays do - it’s simply a list of elements. The one catch is that stacks have the following three constraints:
1. Data can be inserted only at the end of a stack.
2. Data can be deleted only from the end of a stack.
3. Only the last element of a stack can be read.

Stacks are ideal for processing any data that should be handled last in, first out. 

<u>Implementing a Stack</u>
The ArrayList is an obvious storage choice since it offers constant time insertions and deletions at one end via 'add' & 'removeAt' with the last index as a parameter.

<u>Operations on a Stack</u>
1. push : adds a value at the top of the stack (or end of the array list). O(1) time.
2. pop : removes a value at the top of the stack. O(1) time.
3. peek : returns the value at the top of the stack without removing it.

The “undo” function in a word processor, for example, is a great use case for a stack. As the user types, we keep track of each keystroke by pushing the keystroke onto the stack. Then, when the user hits the “undo” key, we pop the most recent keystroke from the stack and eliminate it from the document. At this point, their next-to-most recent keystroke is now sitting at the top of the stack, ready to be undone if need be.