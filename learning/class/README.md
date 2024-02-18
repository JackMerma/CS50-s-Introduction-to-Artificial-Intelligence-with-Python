# Notes

## Supervised Learning

Given a data set of input-output pairs, learn a function to map inputs to outputs

### nearest-neighbor classification

Algorithm that, given an input, chooses the class of the nearest data point to that input

### k-nearest-neighbor classification

Algorithm that, given an input, chooses the most common clas out of the k nearest data points to that input

### perceptron learning rule

Given data point (x, y), update each weight according to:

```
Wi = Wi + a(y - hw(x)) * xi
```

```
Wi = Wi + a(actual value - estimate) * xi
```

### regression

Supervised learning task of learning a function mapping an input point to a continuos value

### overfitting

A model  that fits too closely to a particular data set and therefor may fail to generalize to future data

### k-folds cross-validation

Splitting data into k sets, and experimenting k times, using each set as a test set once, and using remaining data as training set

### Markov Decision Process

Model for decision-making, representing states, actions, and their rewards

    + Set of states S
    + Set of actions Actions(S)
    + Transition model P(s´|s,a)
    + Reward function R(s, a, s´)

### Q-learning

Method for learning a function Q(s, a), estimate of the value of performing action **a** in state **s**

    + Start with Q(s, a) = 0 for all s,a
    + When we taken an action and receive a reward:
        + Estimate the value of Q(s, a) based on current reward and expected future rewards
        + Update Q(s, a) to take into account old estimate as well as our new estimate

    Especification

    + Start with Q(s, a) = 0 for all s,a
    + Every time we take an action a in state s and observe a reward r, we update:

    ```
    Q(s, a) <-- Q(s, a) + alpha * (new value estimate - old value estimate)

    Same to

    Q(s, a) <-- Q(s, a) + alpha * (new value estimate - Q(s, a))

    Same to

    Q(s, a) <-- Q(s, a) + alpha * ((r + future reward estimate) - Q(s, a))

    Same to

    Q(s, a) <-- Q(s, a) + alpha * ((r + MAXa'Q(s', a')) - Q(s, a))

    Finally adding a parameter for future rewards (betha)

    Q(s, a) <-- Q(s, a) + alpha * ((r + betha*MAXa'Q(s', a')) - Q(s, a))
    ```


## Bibliography
Lecture: https://cs50.harvard.edu/ai/2024/notes/4/
Slide: https://cdn.cs50.net/ai/2020/spring/lectures/4/lecture4.pdf
