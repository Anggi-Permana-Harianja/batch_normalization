# batch_normalization


Batch Normalization is a method to reduce internal covariate shift in neural networks, first described in (1), leading to the possible usage of higher learning rates. In principle, the method adds an additional step between the layers, in which the output of the layer before is normalized.

 

Batch normalization (BN) consists of two algorithms.  Algorithm 1 is the transformation of the original input of a layer x to the shifted and normalized value y

.  Algorithm 2 is the overall training of a batch-normalized network.

In both algorithms, the value ε is inserted to avoid dividing by 0 and is selected to be insignificant small (e.g.~10(-8)) on purpose.

Algortihm 1 uses the following simplification:

    The scalar features are normalized independently, making their means 0 and the variance 1. This means in case of a d-dimensional input x = {x(1)…x(d)}, each dimension of the input x is normalized independently, thus every variable x, y, μ, σ becomes x(k), y(k), μ (k), σ(k).
    Each mini-batch produces estimates of the mean and variance of each activation. This ensures that a batch-normalized network retains its ability to fully use backpropagation.
