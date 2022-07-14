Heap Sort is a comparison-based algorithm that sorts an array in ascending/descending order using a heap. [see Heap](obsidian://open?vault=Data_Structures_And_Algorithms&file=notes_Raywenderlich%2Fdata_structures%2FHeap)

Heap sort takes advantage of a heap being, by definition, a partially sorted binary tree with the following qualities:
1. In a max heap, all parent nodes are larger than their children.
2. In a min heap, all parent nodes are smaller than their children.

Even though you get the benefit of in-memory sorting, the performance of heap sort is O(n log n) for its best, worse and average cases. This is because you have to traverse the whole array once and, every time you swap elements, you must perform a sift down, which is an O(log n) operation. 

Heap sort is also not a stable sort because it depends on how the elements are laid out and put into the heap.

This sorting process of heap sort is very similar to selection sort. In a max-heap, the root node is the biggest number, so you move it to the end of the array. You sift the rest of the elements to obey the max-heap, then you move the new root node to the end of the array. And so on till there's no more elements.