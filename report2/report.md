# Report 2

Authors: Eric Yeh, Charles Immendorf, Alex Dundarov, Griffin Golias (Team 4)

## About/Pros/Cons

### ESGS Summarizer (Option R)
About: The problem the paper wants to solve is that procedural text (step-by-step instructions on how to perform a task) can get long an detailed, making it harder for the reader to understand. The proposed solution is to have a summary of each step and a summary of the whole procedure, which would give the reader the main gist of each. The paper implements this solution using an ESGS (Entity-State Graph-based Model) model that performs well on given datasets.

- Pros
  - Will give a comprehensive dive into several aspects of NLP
  - Github code is publicly available (including the datasets on the repo)
  - Would be fun to see what kinds of summaries are generated
- Cons
  - Consists of four non-trivial components, might be a big undertaking to implement completely
  - Usefulness is a little questionable: Procedures are already written to be pretty concise, and it might not be desirable to only focus on a few of the entities in the procedure
  - Authors of the paper are from China, so it would be hard to reach out for help if needed
  - Codebase has minimal documentation, so difficult to understand what is going on code-wise

### K-means Translator (Option R)
About: The problem the paper wants to solve is that kNN-MT (k-Nearest-Neighbor Machine Translation) is susceptible to its performance lowering, due to noisy key-value pairs in a datastore it uses. The proposed solution is to reduce the effects of this noise, using a kNN-MT model with some modifications. These include learned confidence to better model the kNN distribution and interpolation weight, as well as adding perturbations to the pairs to improve robustness. The new model shows performance improvements and robustness improvements over current kNN-MT models.

Pros:
- Large public codebase, as well as another public codebase for the algorithm the paper is building off of (in English, includes example invocations)
- Seems to be of a good scope, involves implementing differnt architectures, but they aren't too complicated
- Improvements to machine translation tasks are of use to the wider world, verifying such an improvement is usefull
- Lots of room for futher investigation, could propose our own architecture changes or tests

Cons:
- Amount of work required is highly contingent on the difficulty of getting a working codebase (from them or from ourselves)
- Requires understanding the technical details of a not easy to understand paper
- Could be difficult to identify cause if results fail to replicate
- requires a moderate amount of computational power, I think its within our constraints but is something to worry about a bit. 

### Logical Fallacy Detection (Option R)
About: The problem the paper wants to solve is the spread of (climate change) misinformation through logically fallacious arguments. The solution proposed is the automated task of logical fallacy detection, which takes a piece of text and outputs what logical fallacy it contains in its argument. The paper implements this solution using a structure-aware classifier that outperforms fine-tuned large language models that were tested.

Pros:
- Codebase with some of the saved models (particularly the ones that performed the best) and datasets
- Logical fallacy detection seems useful to the world, especially in the context of combating climate change misinformation (which the paper has a focus on)
- The NLP task described in the paper doesn’t seem extremely complicated/extremely difficult to understand.

Cons:
- Codebase doesn’t have all of the saved models
  - Some of the models not saved are large language models that may be difficult to access/finetune
  - Some of the current stretch goals involve models such as GPT-4 that also may be difficult to access/finetune
-	Codebase not super-well-documented (there’s a little bit of documentation)

### Entigen Summarizer (Option R)
About: The problem the paper wants to solve is that text-to-image generation models will favor certain social groups over others, when it's prompted with neutral text. The solution proposed is to add ethical intervention (text that creates a rule that supports equitable judgement) to the prompts inputted to these models. The ENTIGEN (Ethical NaTural Language Interventions in Text-to-Image GENeration) dataset, which evaluates image changes given ethical interventions, is also proposed. Through testing, the paper finds that ethical intervention helps the model's generations cover social groups more diversely.

Pros: 
- Authors made reproducabiity easy, and all resources are free and public
- socially important research, with real-world benefits. 
- easily implementable stretch goals
- existing public repository

Cons:
- might not be enough work
- repo lacking in comments and development documentation
- reliant on human visual analysis

## Deep Dive
We have chosen to look more closely at the Logical Fallacy Detection project. The github repo is located here: https://github.com/causalNLP/logical-fallacy

Question: Will using a structure aware model outperform other models in the task of detecting and classifying logical fallacies in climate change claims?

Hypothesis: Because logical fallacies often follow similar structures of reasoning, the paper predicts concludes that introducing structure awareness to the model should make such fallacies easier to classify, as opposed to relying solely on the content of a text, which may not convey the necessary information to make an accurate decision.

This repo has two unclosed issues, one regarding the reproducability and the other one regarding accessibility to the models. However, we should be able to contact the authors of the paper to get more details on resolving these if they come up.

The documentation for the codebase is not super detailed as well, however most of the other codebases suffer this same issue.

## Lecture Topic Ideas
- Fine tuning of large language models
- NLI based Models

