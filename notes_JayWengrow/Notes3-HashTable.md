<u>Hash Table</u>
Most programming languages include a data structure called a
hash table, and it has an amazing superpower: fast reading.

Note that hash tables are called by different names in various
programming languages. Other names include hashes, maps,
hash maps, dictionaries, and associative arrays.

Looking up a value in a hash table has an efficiency of O(1) on
average, as it usually takes just one step.

This process of taking characters and converting them to numbers is known as hashing. And the code that is used to convert those letters into particular numbers is called a hash function.

a hash function needs to meet only one criterion to be valid: a hash function must convert the same string to the same number every single time it’s applied. If the hash function can return inconsistent results for a given string, it’s not valid.

Real-world hash functions are quite complex.

It’s important to point out that the ability to find any value within the hash table in a single step only works if we know the value’s key. 
If we tried to find a particular value without knowing its key, we’d still have to resort to searching each and every key-value pair within the hash table, which is O(N).

Similarly, we can only do O(1) lookups when using a key to find
the value. If, on the other hand, we want to use a value to find its associated key, we cannot take advantage of the hash table’s fast lookup ability.

This is because the whole premise of the hash table is that the key determines the value’s location. But this premise only works in one direction: we use the key to find the value. 
The value does not determine the key’s location, so we have no way to easily find any key without combing through all of them.

Trying to add data to a cell that is already filled is known as a COLLISION.

One classic approach for handling collisions is known as SEPARATE CHAINING. When a collision occurs, instead of placing a single value in the cell, it places in it a reference to an array.

In a scenario where the computer hits upon a cell that references an array, its search can take some extra steps, as it needs to conduct a linear search within an array of multiple values. If somehow all of our data ended up within a single cell of our hash table, our hash table would be no better than an array. So, it actually turns out that the worst-case performance for a hash
table lookup is O(N).

Because of this, it is critical that a hash table is designed in such a way that it will have few collisions, and therefore, typically perform lookups in O(1) time rather than O(N) time.

Ultimately, a hash table’s efficiency depends on three factors:
1. How much data we’re storing in the hash table
2. How many cells are available in the hash table
3. Which hash function we’re using

A good hash table strikes a balance of avoiding collisions while not consuming lots of memory.

To accomplish this, computer scientists have developed the following rule of thumb: 
- for every 7 data elements stored in a hash table, it should have 10 cells.
So, if you’re planning on storing 14 elements, you’d want to have
20 available cells, and so on.

This ratio of data to cells is called the LOAD FACTOR. 
Using this terminology, we’d say that the ideal load factor is 0.7 (7 elements / 10 cells).

