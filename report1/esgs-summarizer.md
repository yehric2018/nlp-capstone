# ESGS Summarizer

Paper: [Summarizing Procedural Text: Data and Approach](https://aclanthology.org/2022.findings-emnlp.162.pdf)

## Summary

Gao et al uses an Entity State Graph-based Summarizer (ESGS) to take procedural texts and produce a condensed summary. The core idea is to identify the salient entity within the procedure and generate a graph representing the transformations that the salient entity undergoes throughout the procedure. Two datasets are used in evaluation: WikiHow_{proc}, which is based on the WikiHow dataset, and PsyStory, which translates stories into changes in characters’ mental states. A ROUGE metric is used to compare the reference summary with the one generated from the model, and the evaluation shows that ESGS outperforms the baseline methods.

## MVP
We will implement the four main components of the procedural text summarization pipeline:
1.	Construct the procedural graph using ProcGPT: In this heterogeneous graph, consecutive steps are connected by an entity whose before/after states are marked by edges.
2.	Encode the graph representation into a vector form using a method similar to a Heterogeneous graph Attention Network (HAN)
3.	Identify the salient entity from the procedure by training a model that will utilize prior and posterior information from the text
4.	Generate a summary that incorporates the salient entity with BART

Overall, this project could potentially be a large undertaking due to having four chunks of work, but the source code being available should help speed things up. Afterwards we plan to run the same evaluation metrics on the WikiHow and PsyStory datasets to see if we can match/exceed them.

## Stretch Goals
-	Fine tune the performance of the model to exceed the results in the paper
-	Test summarization on procedures outside the WikiHow and PsyStory datasets
-	See if we can get different results if we allow for a larger number of salient entities

