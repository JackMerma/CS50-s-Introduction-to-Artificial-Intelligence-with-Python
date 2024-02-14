# Notes

## Probability

### Possible Worlds

Omega (w), then P(w) is defined as the probability of a possible world.

### Axiomes

* 0 <= P(w) <= 1 (obvious notation)
* SUM[wEO] P(w) = 1 (explicit notation where the sum of all possible worlds in a set of possible worlds is 1)
SUM: summation symbol for sigma representation
    w: (world) -> possible world
    O: (omega) -> set of possible worlds
    E: (symbol) -> <are in>

### Conditional probability

P(a|b) means 'what is the probability of 'a', given 'b' and thats equals to:

P(a^b) / P(b)

### Bayes' rule

Given:
    
    P(a^b) = P(a|b) * P(b)
    P(a^b) = P(b|a) * P(a)

Then:
    
    P(b|a) = (P(a|b) * P(b)) / P(a)

### Negation Rule

P(~a) = 1 - P(a)

### Inclusion-Exclusion

P(avb) = P(a) + P(b) - P(a^b)

### Marginalization

P(a) = P(a, b) + P(a, ~b)

### Conditioning

P(a) = P(a|b)P(b) + P(a|~b)P(~b)

## Bibliography
Lecture: https://cs50.harvard.edu/ai/2024/notes/2/
Slide: https://cdn.cs50.net/ai/2020/spring/lectures/2/lecture2.pdf
