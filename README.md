# EvoHDP

Evolutionnary Hierarchical Dirichlet Process for Multiple Correlated Time-Varying Corpora

Python implementation of EvoHDP following  Zhang, Song & al paper :
http://www.shixialiu.com/publications/evohdp/paper.pdf 

All the details and maths comments about the method used are in the notebook. 
The topic weight optimization was done by Cascaded Gibbs Sampling.

The algorithm is quiet expensive because of the optimization technique

The details in the notebook are in French. 

Experiments are done for synthetic data, similary to the paper. 

LIMITATION : 

- The synthetic data are simulated from multinomials in 2 dimensions. Even if the results found for the synthetic data is the same are the sames as the ones mentionned in the paper, when extending the number of dimensions (that actually represents the number of words contained in the corpus of texts), the algorithms converges to a single topic.
- Using lists to represent the data take more time than numpy arrays. The reason why it is not possible to use arrays is that the number of documents is varies according to the time and corpus we are interested in. Check the time comparison between List and Numpy array if needed. 




