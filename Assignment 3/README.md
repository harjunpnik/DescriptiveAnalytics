# Introduction to NLP: Assignment 3

## Assignment on Unsupervised Learning in NLP

### Description of Assignment 3

This assignment relates to Theme 3 of the Introduction to NLP course and will focus on topics of unsupervised learning in NLP.
The data set to be used in the assignment is abstracts,zip file. Use  the files in the subdirectory "awards_2002" as the corpus in the exercises. Follow the code examples in the lecture notebook and adapt them to work with this data, and perform the following steps described in the assignment steps/Questions section.

**Assignment steps/Questions:**

1. **Topic Analysis**
   * There are quantitative measures for evaluating various aspects of clustering results and topic models intrinsically, and they can also be evaluated extrinsically by how well the clusters/topics serve some supervised task as features. In this exercise, however, we will focus on qualitative evaluation of the results in terms of their descriptiveness. As in the example code, you may limit yourself to the 1000 first documents of the corpus when performing clustering, in order to simplify the task and speed up experimentation, but use the whole corpus to calculate tf-idf features.
   * **a.** Experiment with different setups of the tf-idf feature extraction and clustering (k-means or hierarchical), in order to obtain meaningful results. When you arrive at a good configuration, describe it and motivate your chosen setup/parameters.
   * **b.** Inspect the keywords of the clusters. List the 10 first clusters out of all (i.e., not cherry picked examples) and provide an as descriptive label as possible for each of them. 
   * **c.** Select one or two good clusters (that can be clearly interpreted) and one or two bad clusters (that might be difficult to interpret or distinguish). Motivate your choise (clusters may, for instance, be overlapping, too broad/narrow or incoherent). 
   * **d.** Repeat the experiment in (a) with LDA topic modeling instead (on the whole corpus), and explain briefly how the results compare to your previously chosen clustering setup. A few concrete examples may be helpful. Do your best to make sure the list of topic keywords are informative through appropriate post-processing.

2. **Word Vectors**
   * **a.** Choose about 5 words (arbitrarily) to use as seed words in the following experiment. Train word2vec vectors on the corpus while trying out variations on the parameters. Evaluate the vector models by inspecting the most similar words for each of the seed words, and try to identify qualitative differences between different parameter choices. Which parameters seem to have the most interesting effect? At what values? Motivate. Finally study the qualitative effect of increasing the training data, by similarly comparing vectors trained with the best setup on the texts from the awards_2002 directory against vectors trained on the whole set of abstracts (1990-2002).
   * **b.** Repeat the experiment with ELMo from the lecture, with a different target word and different sentences. Choose a word that can have multiple senses, and construct 10 sentences that express 2-3 different senses of the word. Produce ELMo embeddins for the target word in each sentence and measure the similarity between the vectors. Evaluate in how many cases the measured similarities can be used to successfully distinguish between the different senses. Comment on the results, e.g., are you able to identify a particular way in which the model fails?
   