# Notes

## Hill Climbing

```
function HILL-CIMB(problem):
    current = initial state of problem
    repeat:
        neighbor = highest valued neighbor of current
        if neighbor not better then current:
            return current
        current = neighbor
```

## Simulated Annealing

```
function SIMULATED-ANNEALING(problem, max):
    current = initial state of problem
    for t = 1 to max:
        T = TEMPERATURE(t)
        neighbor = random neighbor of current
        ΔE = how much better neighbor is than current
        if ΔE > 0:
            current = neighbor
        with probability e^(ΔE/T) set current = neighbor
    return current
```

## Arc Consistency

```
function REVISE(csp, X, Y):
    revised = false
    for x in X.domain:
        if no y in Y.domain satisfies constraint for (X, Y):
            delete x from X.domain
            revised = true
    return revised
```

```
function AC-3(csp):
    queue = all arcs in csp
    while queue non-empty:
        (X, Y) = DEQUEUE(queue)
        if REVISE(csp, X, Y):
            if size of X.domain == 0:
                return false
            for each Z in X.neighbors - {Y}:
                ENQUEUE(queue, (Z, X))
    return true
```

## Backtracking Search

```
function BACKTRACK(assigment, csp):
    if assigment complete: return assigment
    var = SELECT-UNASSIGNED-VAR(assigment, csp)
    for value in DOMAIN-VALUES(var, assigment, csp):
        if value consistent with assigment:
            add {var = value} to assigment
            result = BACKTRACK(assigment, csp)
            if result != failure: return result
        remove {var = value} from assigment
    return failure
```
