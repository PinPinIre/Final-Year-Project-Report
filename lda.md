##LDA Outline

1. Present in Gensim
 * Well documented
 * Multicore version
  * Was unable to get running
2. [(2003), Blei, Ngg, Jordan](http://machinelearning.wustl.edu/mlpapers/paper_files/BleiNJ03.pdf)
 * 3 level Bayesian model where each document in the corpus is modeled as a 'finite' mixture of topics.
 Each topic is then modeled as 'infinite' mixture over a set of topic probabilities.
4. [Layman explanation of LDA](http://blog.echen.me/2011/08/22/introduction-to-latent-dirichlet-allocation/)
 * Documents are a mixture of topics
 * Topics are mixtures of word probabilities
 * Iterate through each document in the corpus and randomly assign each word to topic
 * To improve the topics, iterate through each document and for each word calculate
  1. p(topic|document)
  2. p(word|topic)
  3. Reassign the word to a new topic where we choose a topic with probability p(topic|document) * p(word|topic)
  4. Repeat until convergence
