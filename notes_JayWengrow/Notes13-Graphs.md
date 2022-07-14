A graph is a data structure that specializes in relationships, as it
easily conveys how data is connected.

<u>Graphs vs Trees</u>
Trees are a type of graph. Both data structures consist of nodes connected to each other.

So, what's the difference between a graph and a tree?
- while all trees are graphs, not all graphs are trees.
- Specifically, for a graph to be considered a tree, it cannot have cycles (nodes that reference each other circularly), and all nodes must be connected.

<u>Graph Jargon</u>
1. Vertex -  a node in a graph
2. Edges - lines between vertices
3. Path - the specific sequence of edges to get from one vertex to another.
4. Adjacents - vertices that are connected by an edge are said to be adjacent to each other. Some also refer to adjacent vertices as neighbors.
5. Connected Graph - a graph where all the vertices are connected in some way.

A Graph can be implemented using Adjacency List or Adjacency Matrix.

<u>Graph Search</u>
The term "search" can have several connotations. In the simplest sense, to "search" a graph means to find a particular vertex somewhere within the graph. This would be similar to searching for a value within an array or a key-value pair inside a hash table.

However, when applied to graphs, the term search usually has a more specific connotation, and that is: if we have access to one vertex in the graph, we must find another particular vertex that is somehow connected to this vertex.

in simple terms - searching is finding a way from A to B.

Applications of Graph search
1. Searching for a particular vertex within a connected graph
2. Discover whether two vertices are connected
3. To merely traverse a graph, which can be useful if you want to perform an operation on every vertex in the graph

There are two well-known approaches for graph search:
1. Depth-First search (DFS) and 
2. Breadth-First search (BFS)

The key to any graph search algorithm is keeping track of the vertices visited so far.

DFS traversal Algorithm
1. Start at any random vertex within the graph.
2. Add the current vertex to the hash table to mark it as having been visited.
3. Iterate through the current vertex's adjacent vertices.
4. For each adjacent vertex, if the adjacent vertex has already been visited, ignore it.
5. If the adjacent vertex has not yet been visited, recursively perform depth-first search on that vertex.

BFS traversal Algorithm
1. Start at any vertex within the graph. Call this the “starting vertex.”
2. Add the starting vertex to the hash table to mark it as having been visited.
3. Add the starting vertex to a queue.
4. Start a loop that runs while the queue isn't empty.
5. Within this loop, remove the first vertex from the queue. We’ll call this the "current vertex".
6. Iterate over all the adjacent vertices of current vertex.
7. If the adjacent vertex was already visited, ignore it.
8. If the adjacent vertex has not yet been visited, mark it as visited by adding it to a hash table, and add it to the queue.
9. Repeat this loop (starting from Step 4) until the queue is empty.

NOTE - BFS traverses all the vertices closest to the starting vertex before moving farther away. DFS, on the other hand, immediately moves as far away from the starting vertex as it can. Only when the search hits a dead end does it return back to the starting vertex.

Efficiency of a Graph Search is O(V+E)
- V is the number of vertices in the graph
- E is the number of edges in the graph

<u>Weighted Graphs</u>
Another useful type of graph, known as a weighted graph, adds additional information to the edges of the graph.

Shortest Path Problem::
Numerous algorithms can solve the shortest path problem, one of the famous one is - Dijkstra's Algorithm

Dijkstra's Algorithm steps:: (in terms of cities and flight costs)
- We visit the starting city, making it our "current city".
- We check the prices from the current city to each of its adjacent cities.
- If the price to an adjacent city from the starting city is cheaper than the price currently in cheapest_prices_table (or the adjacent city isn't yet in the cheapest_prices_table at all):
  1. We update the cheapest_prices_table to reflect this cheaper price.
  2. We update the cheapest_previous_stopover_city_table, making the adjacent city the key and the current city the value.
- We then visit whichever unvisited city has the cheapest price from the starting city, making it the current city.
- We repeat the Steps 2 through 4 until we've visited every known city.

