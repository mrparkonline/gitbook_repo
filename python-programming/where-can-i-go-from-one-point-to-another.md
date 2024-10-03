# Where can I go from one point to another?

<figure><img src="../.gitbook/assets/image (3).png" alt=""><figcaption></figcaption></figure>

## What is a Graph?

asd

## How to represent a Graph with a Dictionary

<pre class="language-python"><code class="lang-python"><strong># Key = Nodes
</strong><strong># Value = List containing possible edges from the key
</strong><strong>connections = {
</strong>    1 : [4, 8],
    2 : [3, 7],
    3 : [2, 4, 9],
    4 : [1, 3, 9],
    5 : [7],
    6 : [7, 8, 9],
    7 : [2, 5, 6, 8],
    8 : [1, 6, 7, 9],
    9 : [3, 4, 6, 8]
}
</code></pre>

asd

```python
connections = {
    1 : [8, 4],
    2 : [3, 7],
    3 : [2, 4, 9],
    4 : [1, 3, 9],
    5 : [7],
    6 : [7, 8, 9],
    7 : [2, 5, 6, 8],
    8 : [1, 6, 7, 9],
    9 : [3, 4, 6, 8]
}

def possibleDestinations(graph, start, goal):
    visited = set()

    queue = []
    queue.append([start])
    i = 0

    while i < len(queue):
        history = queue[i]
        current_city = history[-1]
        i += 1

        if current_city not in visited:
            current_neighbors = graph[current_city]

            for n in current_neighbors:
                new_path = history.copy()
                new_path.append(n)
                queue.append(new_path)

                if n == goal:
                    return new_path
            # end of for
            visited.add(current_city)

print(f"1 to 3 : {possibleDestinations(connections, 1, 3)}")
```
