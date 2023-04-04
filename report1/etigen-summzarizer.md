# ENTIGEN Summarizer

Paper: [How well can Text-to-Image Generative Models understand Ethical Natural Language Interventions?]
(https://aclanthology.org/2022.emnlp-main.88/)
Github:https://github.com/Hritikbansal/entigen_emnlp

## Summary

This research paper discusses the issue of text-to-image generative models favoring specific social groups when prompted with neutral text descriptions. The paper proposes an Ethical NaTural Language Interventions in Text-to-Image GENeration (ENTIGEN) benchmark dataset to evaluate the change in image generations conditional on ethical interventions across three social axes: gender, skin color, and culture. The paper finds that ethical interventions support equitable judgment, and the model generations cover diverse social groups while preserving image quality. In some cases, the generations would be anti-stereotypical. 

## MVP

Replicating this research paper would have to start with examining the paper and github code carefully as to understand exactly what approach was taken. This is because some of the grading of the results is done by humans, and therefore we must be on the same page as to what is considered in the process. Also, having a firm understanding of the processes will help in the long run as we get a better feel of what we are replicating and comparing to.

Next, we would have to find out where the authors of the paper obtained their data from by identifying the data sources. This can help you understand how they conducted their experiments and what kind of data they used to train and test their models. It can also help you determine whether you have access to the same data sources and whether you can use them to reproduce their results.

Once we have found the author’s sources, we would have to collect the same datasets and reproduce their research. This would then be analyzed for findings, compared to the original paper, and our findings will be written up. 

Because this peper uses publicly available models, there isn't much to implement. We would have to: 

- Setup environments for each model usinc Conda
- Setup the original repository
- Import the publically available dataset

When it comes to data collection for analysis, we need human annotators to review the outputs of each respective model on the axis' of gender, skin tone, and ethnicity.

This project idea is simple to reproduce, but allows for insight on a socially important topic. All the sources and work are publically available as the authours seem to have taken great care in ensuring the ease of reproducability in their work. This also means that our stretch goals are more achievable. 

## Stretch Goals

Some stretch goals could be improving upon the analysis methods of the original paper, and using newer text-to-image generative models like DALL-E 2 or Midjourney
