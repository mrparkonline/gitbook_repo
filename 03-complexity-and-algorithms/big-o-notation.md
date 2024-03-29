# Big-O Notation

{% embed url="https://www.youtube.com/watch?index=11&list=PL96C35uN7xGLLeET0dOWaKHkAlPsrkcha&v=RGuJga2Gl_k" %}

## Algorithm Complexity of Time & Space <a href="#algorithm-complexity-of-time--space" id="algorithm-complexity-of-time--space"></a>

As computer scientists started to develop various algorithms for a solutions, they needed a way to classify the effectiveness of their algorithms, and they also required a way to prove that a new algorithm is better than the old by mathematical proof & analysis.

<figure><img src="https://cdn.programiz.com/sites/tutorial2program/files/big0.png" alt=""><figcaption><p><a href="https://www.programiz.com/dsa/asymptotic-notations">Image Source</a></p></figcaption></figure>

Due to this, three notations methods were developed:

1. Big - O Notation (the worst case scenario)
2. Big - Theta Notation (the average case scenario)
3. Big- Omega Notation (the best case scenario)

When we analyze an algorithm we can look at all three scenarios and see their effectiveness. The main notation that we will focus will be the Big-O Notation. We focus on the Big-O because it shows us that at worst our algorithm will perform at X, and if X is better than our previous algorithm, it is _**definitely**_ better.

### Big - O Notation <a href="#big---o-notation" id="big---o-notation"></a>

**Big O Notation:** a mathematical notation that describes the limiting behaviour of a function as its input/parameter/argument approaches infinity.

* Consider the Big-O to tell us the “Worst case scenario performance” of our algorithm

We use Big-O Notation for:

1. **Algorithm Proof**: To prove that our algorithm A is better than algorithm B, we must have a proof that our Big-O notation is better
2. **Measure Performance, Run-time, or Disk Usage**: Our algorithms are designed to solve problems; however, reaching the solutions must not be feasible due to time or disk-space constraints
3. **Mathematically Formalizing our Algorithms**: Different hardware will output different runtimes; therefore, we needed a formal mathematical analysis

Big-O is Classified with a Notation of:

```
O(f(x))

-- where f(x) can be various mathematical functions that describes behaviour of our algorithm's effectiveness.
```

The following is a common list of complexities from best to worst performance:

```
- O(1) → Constant Complexity
- O(log n) → Logarithmic Complexity
- O(n) → Linear Complexity
- O(n log n) → Linearithmic Complexity
- O(n^2) → Quadratic Complexity
- O(2^n)→ Exponential Complexity
- O(n!)→ Factorial Complexity
```

Time & Space Complexity

* **Time**: the measure of how long an algorithm takes
* **Space**: the measure of how much disk space that the algorithm requires from the computer

### Python 3 Data Structure and Big-O Notations <a href="#python-3-data-structure-and-big-o-notations" id="python-3-data-structure-and-big-o-notations"></a>

[Source](https://www.ics.uci.edu/\~brgallar/week8\_2.html)

#### Lists and Tuples: <a href="#lists-and-tuples" id="lists-and-tuples"></a>

| Operation     | Example         | Class      | Notes                                |
| ------------- | --------------- | ---------- | ------------------------------------ |
| Index         | l\[i]           | O(1)       |                                      |
| Store         | l\[i] = 0       | O(1)       |                                      |
| Length        | len(l)          | O(1)       |                                      |
| Append        | l.append(5)     | O(1)       |                                      |
| Pop           | l.pop()         | O(1)       | same as l.pop(-1), popping at end    |
| Clear         | l.clear()       | O(1)       | similar to l = \[]                   |
| Slice         | l\[a:b]         | O(b-a)     | l\[1:5]:O(l)/l\[:]:O(len(l)-0)=O(N)  |
| Extend        | l.extend(…)     | O(len(…))  | depends only on len of extension     |
| Construction  | list(…)         | O(len(…))  | depends on length of argument        |
| —–            | —–              | —–         | —–                                   |
| check ==, !=  | l1 == l2        | O(N)       |                                      |
| Insert        | l\[a:b] = …     | O(N)       |                                      |
| Delete        | del l\[i]       | O(N)       |                                      |
| Remove        | l.remove(…)     | O(N)       |                                      |
| Containment   | x in / not in l | O(N)       | searches list                        |
| Copy          | l.copy()        | O(N)       | Same as l\[:] which is O(N)          |
| Pop           | l.pop(0)        | O(N)       |                                      |
| Extreme value | min(l)/max(l)   | O(N)       |                                      |
| Reverse       | l.reverse()     | O(N)       |                                      |
| Iteration     | for v in l:     | O(N)       |                                      |
| —–            | —–              | —–         | —–                                   |
| Sort          | l.sort()        | O(N Log N) | key/reverse doesn’t change this      |
| Multiply      | k\*l            | O(k N)     | 5\*l is O(N): len(l)\*l is O(N\*\*2) |

Tuples support all operations that do not mutate the data structure (and with the same complexity classes).

#### Sets: <a href="#sets" id="sets"></a>

| Operation            | Example       | Class                 | Notes                        |
| -------------------- | ------------- | --------------------- | ---------------------------- |
| Length               | len(s)        | O(1)                  |                              |
| Add                  | s.add(5)      | O(1)                  |                              |
| Containment          | x in/not in s | O(1)                  | compare to list/tuple - O(N) |
| Remove               | s.remove(5)   | O(1)                  | compare to list/tuple - O(N) |
| Discard              | s.discard(5)  | O(1)                  |                              |
| Pop                  | s.pop()       | O(1)                  | compare to list - O(N)       |
| Clear                | s.clear()     | O(1)                  | similar to s = set()         |
| —–                   | —–            | —–                    | —–                           |
| Construction         | set(…)        | len(…)                |                              |
| check ==, !=         | s != t        | O(min(len(s),lent(t)) |                              |
| <=/<                 | s <= t        | O(len(s1))            | issubset                     |
| >=/>                 | s >= t        | O(len(s2))            | issuperset s <= t == t >= s  |
| Union                | s             | t                     | O(len(s)+len(t))             |
| Intersection         | s & t         | O(min(len(s),lent(t)) |                              |
| Difference           | s - t         | O(len(t))             |                              |
| Symmetric Difference | s ^ t         | O(len(s))             |                              |
| —–                   | —–            | —–                    | —–                           |
| Iteration            | for v in s:   | O(N)                  |                              |
| Copy                 | s.copy()      | O(N)                  |                              |

#### Dictionary: <a href="#dictionary" id="dictionary"></a>

| Operation      | Example     | Class  | Notes                          |
| -------------- | ----------- | ------ | ------------------------------ |
| Index          | d\[k]       | O(1)   |                                |
| Store          | d\[k] = v   | O(1)   |                                |
| Length         | len(d)      | O(1)   |                                |
| Delete         | del d\[k]   | O(1)   |                                |
| get/setdefault | d.method    | O(1)   |                                |
| Pop            | d.pop(k)    | O(1)   |                                |
| Pop item       | d.popitem() | O(1)   |                                |
| Clear          | d.clear()   | O(1)   | similar to s = {} or = dict()  |
| Views          | d.keys()    | O(1)   |                                |
| —–             | —–          | —–     | —–                             |
| Construction   | dict(…)     | len(…) |                                |
| —–             | —–          | —–     | —–                             |
| Iteration      | for k in d: | O(N)   | all forms: keys, values, items |

### Example Big O Classification <a href="#example-big-o-classification" id="example-big-o-classification"></a>

```python
def factor_counter(n):
    """ factor_counter() determines the number of factors N has """

    ctr = 0
    for divisor in range(1,n+1):
        if n % divisor == 0:
            ctr += 1

    return ctr
# end of factor_counter
```

We look at every value of N from 1 to N; therefore, this is O(n).

* Minor computations such as: `+= 1` and `n % divisor` does not affect the overall classification

```python
def factor_counter(n):
    """ factor_counter() determines the number of factors N has """

    ctr = 0
    if n < 9:
        # difference of speed between the optimized and non-optimized is very minimial on small numbers
        for divisor in range(1,n+1):
            if n % divisor == 0:
                ctr += 1

        return ctr
    else:
        end_point = int(n**0.5) + 1

        for divisor in range(1, end_point):
            if n % divisor == 0 and (n // divisor) != divisor:
                ctr += 2
            elif n % divisor == 0 and (n // divisor) == divisor:
                ctr += 1

    return ctr
```

The refactored version only analyzes value from 1 to SquareRoot(n); therefore, the refactored version is:

$$
O(n) =  \sqrt{n}
$$
