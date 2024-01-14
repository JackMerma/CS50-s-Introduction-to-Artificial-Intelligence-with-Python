# Notes

## DFS

We use a StackFrontier that uses a List for nodes.


## BFS

We use a QueueFrontier that uses a StackFrontier for nodes but redefining the remove method.


## Greedy best-first search

We use a HeapFrontier thar uses a StackFrontier for nodes but redefining the add and remove method.
Now this is a search algorithm that expands the node that is closest to the goal, as estimated by a heuristic function h(n)


## A\* Search

Search algorithm that expands node with lowest value of g(n) + h(n) where:
+ g(n) = cost to reach node
+ h(n) = estimated cost to goal

So, this algorithm is optimal if:
- h(n) is adminisble (never overstimates the true cost), and
- h(n) is consistent (for every node n and successor n' with step cost C, h(n) <= h(n') +c)


## Adversarial Search 

### MiniMax

Is used where there is a game for 2 players (one tries to minimize and the another one to maximize the state). Now there is part or functions:

+ **s0:** initial state
+ **Player(s):** retuns whith player to move in state **s**
+ **Actions(s):** returns legal moves in state **s**
+ **Result(s, a):** returns state after action **a** taken in state **s**
+ **Terminal(s):** chacks if state **s** is a terminal state
+ **Utility(s):** final numerical value for terminal state **s**

Now, pseudocode:

+ Given a state **s**:
    + **MAX** picks action **a** in **ACTIONS(S)** that produces highest value of **MIN-VALUE(RESULT(s, a))**
    + **MIN** picks action **a** in **ACTIONS(S)** that produces smallest value of **MAX-VALUE(RESULT(s, a))**

For MAX-VALUE
```
function MAX-VALUE(state):
    if TERMINAL(state):
        return UTILITY(state)
    v = -INF # negative inf
    for action in ACTIONS(state):
        v = MAX(v, MIN-VALUE(RESULT(state, action)))
    return v
```

For MIN-VALUE
```
function MIN-VALUE(state):
    if TERMINAL(state):
        return UTILITY(state)
    v = INF # positive inf
    for action in ACTIONS(state):
        v = MIN(v, MAX-VALUE(RESULT(state, action)))
    return v
```

So, a little bit intelligent?, that's the **Alpha-Beta Prunning** where if you have at the moment a value **K** of some node and another node secures you a **K'** result where **K>K'** (for **MAX-VAL**) or **K<K'** (for **MIN-VAL**), then you don't have to visit that state.

## Bibliography
Lecture: https://cs50.harvard.edu/ai/2024/notes/0/
Slide: https://cdn.cs50.net/ai/2020/spring/lectures/0/lecture0.pdf
