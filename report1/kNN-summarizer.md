# ESGS Summarizer


Paper:Towards Robust k-Nearest-Neighbor Machine Translation
https://aclanthology.org/2022.emnlp-main.367.pdf 


## Summary


This paper proposes an algorithm for incorporating a K nearest neighbors approach into a machine translation model and compares its experimental performance with other implementations. The basic kNN approach is to store a datastore dictionary with vector representation keys and ground truth token values, we use this to generate an alternative distribution over tokens from the base model, then take a linear combination of them. The authors argue that this algorithm is sensitive to noisy datastores and doesn’t utilize all the information it should. They propose a number of changes, including some perturbations on representations to improve robustness, and learned calculations of confidence to properly weigh the distribution and proportion of the kNN model. The paper contains a large code repository.


## MVP
Replicating the paper would start with examining the paper’s code and written description of the algorithms. The paper contains a number of different descriptions of algorithms or modifications of algorithms, it would be important to have a comprehensive understanding of what exactly is being done in each instance. Additionally the paper uses datasets and pretrained models that we would also want to understand and know how to use.


The existing code base seems quite extensive, with example invocations and installation details given. In addition their code builds upon preexisting kNN-MT code which is also publicly available which similarly seems quite usable. This will be beneficial in understanding the algorithm, and may be possible to use directly to replicate their experiments. In the event we write our own code this would also be a significant portion of the project. We would have to know how to use the pretrained models and datasets referenced in the paper. We would have to implement the various algorithms the author’s describe and verify that they are functioning the same as the author’s. 


Once we are able to train and invoke the models described in the paper, we will collect data in order to generate the tables included in the paper. If our results match closely with the paper’s, then we can move on to extending their work. If we fail to replicate the experimental results, then we would examine the features of the algorithm to try to identify where things are going wrong. Since the author’s make a few different alterations to the base kNN-MT algorithm, it is possible that some of them have effects that replicate and some don’t. 


Overall the amount of work required to get working code will be a large factor in how difficult the project will end up being. 


## Stretch Goals


        The paper leaves a lot of room for exploration of other ways of implementing the kNN component of the models. For example we could test other types of perturbations with the goal of improving robustness, or other architectures for generating the distribution over the kNN tokens. Alternatively the same approach could be tested on different training/testing sets or using different base NMT models