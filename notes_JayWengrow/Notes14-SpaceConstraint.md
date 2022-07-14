Space complexity - how much memory an algorithm consumes.

Space complexity becomes an important factor when memory is limited. If you have an enormous amount of data, or are programming for a small device with limited memory, space complexity can matter a lot.

In a perfect world, we’d always use algorithms that are both fast and memory-efficient. However, there are times where we can’t have both, and we need to choose between the two. Each situation requires a careful analysis to know when we need to prioritize speed over memory, and memory over speed.

For time complexity, the key question is: 
- if there are N data elements, how many steps will the algorithm take?

For space complecity, the key question is:
- if there are N data elements, how many units of memory will the algorithm consume?

note := A recursive function takes up a unit of space for each recursive call it makes. This is the sneaky way recursion can gobble up memory; even if our function does not explicitly create new data, the recursion itself adds data to the call stack.

