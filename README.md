# Tie-decay-network-embedding
This repository provides the codes for the publication "Embedding and trajectories of temporal networks" on IEEE Access(2023) by Chanon Thongprayoon, Lorenzo Livi, and Naoki Masuda.

## Python packages in "File's name".py/ipynb
- `import pandas as pd`
- `import numpy as np`
- `import numpy.linalg as LA`
- `math`
- `import matplotlib.pyplot as plt`
## Functions in "File's name".py/ipynb
- `Adjacency`: to create an adjacency matrix at each time step, where at least one event occurs between a pair of nodes.
- `ComputeBk`: use the tie-decay matrix at from the previous time step to compute the tie-decay matrix of the current time step.
- `Tie_decay_matrices`: by using `ComputeBk`, this function computes tie-decay matrices of multiple time steps. Note that the index starts at $1$.
- `Find_eigenpair`: compute eigenvalues and eigenvectors of a matrix.
- `Centered_Distance_matrix`: apply double mean-centering matrices, each to the left and the right side of the (squared) distance matrix.
- `Squared_Frobenius_Distance_matrix`: compute the squared Frobenius distance matrix of tie-decay matrices.
- `Degree_matrix`: compute the degree matrix of the input matrix.
- `Laplacian_matrix`: compute the Laplacian matrix of the input matrix.
- `aux_delta`: reindex the output from `Tie_decay_matrices`, return a list of time steps, and the Laplacian eigenvalues of each tie-decay matrix.
- `delta`: compute the vector of squared distance between a point and each of the landmarks.
- `Col_sum`: compute the average column of a squared distance matrix.
- `Classical_MDS`: perform Multidimensional scaling.
- `Landmark_MDS`: perform Landmark Multidimensional scaling.
- `Information_Loss`: compute the ratio of the first $k$ eigenvalues to the sum of all eigenvalues, in terms of modulus (the function "g" in the paper).
