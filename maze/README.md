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
