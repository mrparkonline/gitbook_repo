# Dijkstra’s Algorithm

<figure><img src="../../../../.gitbook/assets/image (1) (1).png" alt=""><figcaption><p>(GeeksforGeeks <a href="https://media.geeksforgeeks.org/wp-content/uploads/20240111182238/Working-of-Dijkstras-Algorithm-768.jpg">Source</a>)</p></figcaption></figure>

Dijkstra’s algorithm finds the shortest path from a location to every other location.

The above diagram is called a [graph](https://en.wikipedia.org/wiki/Graph_\(abstract_data_type\))

* In our example graph, we have locations from 0 to 8. Locations are referred to as `"Nodes"`
* Nodes are connected with line, which are called `"Edges"`
  * Each edge has a distance value, which are called `"Weights"`

## Dijkstra's algorithm follows these rules:

1. Every time we want to visit a new node, we will choose the node with the smallest known distance.
2. Once we’ve moved to the node, we check each of its neighbouring nodes.&#x20;
   1. We calculate the distance from the neighbouring nodes to the root nodes by summing the cost of the edges that lead to that new node.
3. If the distance to a node is less than a known distance, we’ll update the shortest distance
