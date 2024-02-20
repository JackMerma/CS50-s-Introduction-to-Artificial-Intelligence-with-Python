# Notes

## Neural Networks

+ Neurons are connected to and receive electrical signals from other neurons.
+ Neurons process input signals and can be activated

```
h(x1, x2) = w0 + w1*x1 + w2*x2

To

h(x1, x2) = g(w0 + w1*x1 + w2*x2)
```

where:
    + h(x1, ..., xn) => hypothesis function
    + g(...) => activation function

## Gradient descent

Algorithm for minimizing loss when training neural network

Steps:

+ Start with a random choice of weights
+ Repeat:
    + Calculate the gradient based on all data points: direction that will lead to decreasing loss.
    + Update weights according to the gradient.

## Backpropagation

Steps:

+ Start with a random choise of weights
+ Repeat:
    + For each layer, starting with output layer, and moving inwards towards earliest hidden layer:
        + Propagate error back one layer
        + Update weights

## Image convolution

+ Applaying a filter that adds each pixel value of an image to its neighbors, weighted according to a kernel matrix

## Bibliography
Lecture: https://cs50.harvard.edu/ai/2024/notes/5/
Slide: https://cdn.cs50.net/ai/2020/spring/lectures/5/lecture5.pdf
