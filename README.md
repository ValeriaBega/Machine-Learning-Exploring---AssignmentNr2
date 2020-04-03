# Machine-Learning-Exploring
## Used Datasets:
**MNIST dataset:**
You can get the MNIST dataset in one of the following ways.
1. Link to Data in csv format:
https://www.openml.org/data/get_csv/52667/mnist_784.arff
2. Data using Scikit-learn:
`from sklearn.datasets import fetch_openml`

`mnist = fetch_openml(’mnist_784’, version=1)`

**Olivetti faces dataset:**
You can get the Olivetti faces dataset in one of the following ways.
1. Data:
https://cs.nyu.edu/~roweis/data/olivettifaces.mat
Images:
https://cs.nyu.edu/~roweis/data/olivettifaces.gif
2. Data using Scikit-learn:
`from sklearn.datasets import fetch_olivetti_faces`

`olivetti = fetch_olivetti_faces()`

### Question 1: Grid search, KNN, SVM and Ensembles
1. Using grid search and your selected metric, find the best hyperparameters for two models: SVM and
KNN. Briefly describe how you selected the hyperparameters and their values for grid search.
2. Combine the SVM, KNN with the best parameters, and a decision tree model with default parameters,
into a voting classifier. Evaluate its performance.
3. Train a random forest model and evaluate its performance

### Question 2: Clustering [Optional]
1. Select a continuous variable in the dataset and cluster its values. Use any two clustering methods (k-
means, agglomerative, DBSCAN etc.). For each method, explain how you chose clustering parameters
(e.g., the number of clusters, linkage type etc. as appropriate for the algorithm).
2. Train two additional voting classifier models. In each of the two models the values of the continuous
variable should be clustered using one of the clustering methods you implemented in q. 2a. Is the
performance of these models different from the original model?

### Question 4: PCA
1. Load the MNIST dataset and split it into a training set and a test set (take the first 60,000 instances for
training, and the remaining 10,000 for testing). Train a Random Forest classifier on the dataset and
time how long it takes, then evaluate the resulting model on the test set.
Next, use PCA to reduce the dataset’s dimensionality, with an explained variance ratio of 95%. Train
a new Random Forest classifier on the reduced dataset and see how long it takes. Was training much
faster? Next, evaluate the classifier on the test set. How does it compare to the previous classifier?
2. Some dimensionality reduction techniques can also be used for anomaly detection. For example, take
the Olivetti faces dataset and reduce it with PCA, preserving 99% of the variance. Then compute
the reconstruction error for each image. Next, take some of the images you built and modify some
images using techniques such as rotate, flip, darken, and look at their reconstruction error: notice how
much larger the reconstruction error is. If you plot a reconstructed image, you will see why: it tries to
reconstruct a normal face.
