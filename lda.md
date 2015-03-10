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
5. [Blei's overview of topic modeling](http://www.cs.princeton.edu/~blei/papers/Blei2012.pdf)
 * Model assumes that the topics are generated first and then the documents are generated from the topics.
 * Inferring the topics is a reversing of the generation process. Finding the hidden structure in the documents.
 * LDA can aid in information retrieval and corpus exploration
 *"In this way, topic modeling provides an algorithmic solution to managing, organizing, and annotating large archives of texts."*
 * LDA is a probabilistic model
  
