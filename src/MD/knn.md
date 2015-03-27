##KNN Outline
1. Not implemented directly in Gensim but the creator has conducted experiments analysing the performance of ANN libraries to eventually add to Gensim.
 * Main contenders are
  * Spotify/Annoy
  * FLANN
2. Skikit-learn has functionality for supervised and unsupervised KNN.
Uses three different algorithms; ball tree, KD tree, or a bruteforce algorithm.
3. KNN is one of the [top 10 data-mining algorithms](http://www.cs.umd.edu/~samir/498/10Algorithms-08.pdf)
4. 1-NN - If given x and y is the nearest neighbour to x then x and y are the same.
This assumption doesn't really hold when the number of datapoints is small but is a reasonable assumption when they are large/dense.
5. K-NN is an extension of 1-NN where the k-nearest neighbours are found and do majority voting.
Typically k is odd to avoid ties.
Obvious extension is to do weighted KNN where vote is weighted based on the distance from X.
