# Notes

## Sentence

An assertion about the world in a knowlegde representation language

## Propositional Logic

### Propositional Symbols

P, Q or R, represent **sentences**

### Logical Connectives

+ not ~
+ and ^
+ or v
+ implication ->
+ biconditional <->

### Model

The initial values for each sentence: {P = true, Q = False} where P: It's raining and Q: It's a Tuesday

## Model Checking

To determinate if **KB** |= a:
    + Enumerate all possible models
    + If in every model where **KB** is true, **a** is true, then **KB** entails **a**.

## Inference Rules

### Modus Ponens

    ```
    a -> b
    a
    ------
    b
    ```

### And Elimination
    
    ```
    a ^ b
    ------
    a     (or b)
    ```

### Double Negation Elimination

    ```
    ~(~a)
    ------
    a
    ```

### Implication Elimination

    ```
    a -> b
    ------
    ~a v b
    ```

### Biconditional Elimination

    ```
    a <-> b
    ------
    (a -> b) ^ (b -> a)
    ```

### De Morgan's Law

    ```
    ~(a ^ b)
    ------
    ~a v ~b
    ```

    ```
    ~(a v b)
    ------
    ~a ^ ~b
    ```

### Ditributive Property

    ```
    (a ^ (b v y))
    ------
    (a ^ b) v (a ^ y)
    ```
    
    ```
    (a v (b ^ y))
    ------
    (a v b) ^ (a v y)
    ```

## Bibliography
Lecture: https://cs50.harvard.edu/ai/2024/notes/1/
Slide: https://cdn.cs50.net/ai/2020/spring/lectures/1/lecture1.pdf
