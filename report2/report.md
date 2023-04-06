# Report 2

## Pros/Cons

### ESGS Summarizer
- Pros
  - Will give a comprehensive dive into several aspects of NLP
  - Github code is publicly available (including the datasets on the repo)
  - Would be fun to see what kinds of summaries are generated
- Cons
  - Consists of four non-trivial components, might be a big undertaking to implement completely
  - Usefulness is a little questionable: Procedures are already written to be pretty concise, and it might not be desirable to only focus on a few of the entities in the procedure
  - Authors of the paper are from China, so it would be hard to reach out for help if needed
  - Codebase has minimal documentation, so difficult to understand what is going on code-wise

### K-means Translator
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

### Logical Fallacy Detection
Pros:
- Codebase with some of the saved models (particularly the ones that performed the best) and datasets
- Logical fallacy detection seems useful to the world, especially in the context of combating climate change misinformation (which the paper has a focus on)
- The NLP task described in the paper doesn’t seem extremely complicated/extremely difficult to understand.

Cons:
- Codebase doesn’t have all of the saved models
  - Some of the models not saved are large language models that may be difficult to access/finetune
  - Some of the current stretch goals involve models such as GPT-4 that also may be difficult to access/finetune
-	Codebase not super-well-documented (there’s a little bit of documentation)

### Entigen Summarizer
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

This repo has two unclosed issues, one regarding the reproducability and the other one regarding accessibility to the models. However, we should be able to contact the authors of the paper to get more details on resolving these if they come up.

The documentation for the codebase is not super detailed as well, however most of the other codebases suffer this same issue.

## Lecture Topic Ideas
- Fine tuning of large language models
- NLI based Models

