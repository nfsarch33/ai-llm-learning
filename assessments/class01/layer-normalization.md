
# Layer Normalization
- Definition
    - A technique used to standardize the inputs to a layer in a neural network[^1^]
    - Improves the speed and stability of training[^1^]
- How it works
    - Computes the mean and variance for normalization from all of the summed inputs to the neurons in a layer on a single training case[^1^]
    - Normalizes the inputs to a layer such that they have a mean of 0 and a standard deviation of 1[^4^]
- Differences from Batch Normalization
    - LN is independent of batch size, making it useful in cases where the batch size is small or varies a lot[^1^]
    - BN computes the mean and variance for normalization over a mini-batch of training cases[^1^]
