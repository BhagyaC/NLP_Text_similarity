# Principal component analysis
- It is a way to identify the key information carrying parts of your embedding. It is trying to find out what is different and unique about each embedding.
- And will discard anything they have in common 
- PCA is a dimensionality reduction techinique which is used to highlight the important information in an embedding
```# Import the libraries
import numpy as np
import matplotlib.pyplot as plt
from sklearn.decomposition import PCA

# Use PCA to reduce the dimensions of the embedding
def pca_transform(arr1, arr2, arr3, arr4, dim):
    vectors = np.vstack((arr1, arr2, arr3, arr4))
    # Set the number of dimensions PCA will reduce to
    pca = PCA(n_components=dim)
    pca.fit(vectors)
    new_pca = pca.transform(vectors)
    print("original shape:   ", vectors.shape)
    print("transformed shape:", new_pca.shape)
    return(new_pca)

# Draw a 2d graph with the new dimensions
def two_d_graph(reduced_dims):
    colors = ("red", "green", "blue", "orange")
    groups = ("King", "Queen", "Man", "Woman") 
 
    # Create plot
    fig = plt.figure()
    ax = fig.gca()
 
    for data, color, group in zip(reduced_dims, colors, groups):
        x, y = data
        ax.scatter(x, y, alpha=0.8, c=color, edgecolors='none', s=30, label=group)
 
    plt.title('Reduced vocab set')
    plt.legend(loc=1)
    plt.show()

# Transform the 4 dimensions to 2 via PCA
def vectors(a, b, c, d):
    emba = np.array(a)
    embb = np.array(b)
    embc = np.array(c)
    embd = np.array(d)
    new_dim = pca_transform(emba, embb, embc, embd, 2)
    two_d_graph(new_dim)

vectors([1,0,0,0], [0,1,0,0], [0,0,1,0], [0,0,0,1])
