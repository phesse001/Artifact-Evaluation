# Artifact-Evaluation
A repository containing artifact checklists and papers to experiment with different artifact evaluation methods
# Links to Checklists
Below are links to google sheets templating the cTuning, AAAI, and NeurIPS artifact evaluation checklists:
* [cTuning](https://docs.google.com/spreadsheets/d/1wEZPmnEjxzoPHyXC8pxvdrPdjtP_ek3rX5gu5sxbkps/edit?usp=sharing)
* [AAAI](https://docs.google.com/spreadsheets/d/1F5w-P3W9TkMXlU77WhkLY3tXrgoIB__bjD8ZD5PCZp4/edit?usp=sharing)
* [NeurIPS](https://docs.google.com/spreadsheets/d/178LMK6wNu7a7frdwJE3SJDrWffHDdgcScYk5jiepaTI/edit?usp=sharing)
# Experience
## Overview
There are many artifact checklists that have been developed in order to improve the reprodicibility of computational results. Reproducibility has adopted many similar definitions, but to make sure we are on the same page, I will use the basic definition from the paper *Improving Reproducibility in Machine Learning Research*, that is "obtaining similar results as presented in a paper or talk, using the same code and data (when available)" (Pineau et al. 1). Before comparing checklists that have already been used, it is important to understand what the goal of these checklists are. For authors, it is most useful to look at these checklists in order to conduct good empirical evaluation. For those using checklists to review the work of others, it is helpful in organizing a reviewers thoughts about what important pieces of information are and avoiding the common pitfall of overlooking information that is required of reliable, repeateable, and valid results. These checklists are meant to be used by authors while writing their papers and reviewers while judging a paper (Berger et al.).
## What I found useful across all 3 checklists
In the [SIGPLAN](https://www.sigarch.org/a-checklist-manifesto-for-empirical-evaluation-a-preemptive-strike-against-a-replication-crisis-in-computer-science/#undefined) checklist, the authors pointed out that proper use of a checklist requires nuance. In this light, I found it helpful to not have a hard-coded checklist, but rather have a list of items with the ability to turn off/on different criteria. Similarly, I found the checklists that used high level questions before the more fine-grain criteria to be more user-friendly. Another important feature of a checklist is well defined definitions. I found this out by initially using checklists with more ambiguous definitions, and having a hard time being able to decide whether a givern criterion should deserve x points or y points. This leads me to the point system. This was something new that I tried that these checklists didn't natively have. It was beneficial to be able to look at a criterion, like "dataset" for example and be able to give almost full credit, but maybe -1 for not describing how to obtain the dataset or whether it was private. It is hard to say whether this is better than marking a criterion as "partial" and commenting on what it is missing. I will comment on what I didn't like about the point system in the section below.
## What I didn't find useful across all 3 checklists
While I mentioned the point system provided utility in explicitly subtracting a point for a criterion missing a vital piece of information, I'm not sure that the positives necessarily outweigh the negatives (at least for me, an undergrad student inexperienced with artifact evaluation). The first negative is noise. A lot of the times a paper either does a really good job in a given area or completely misses it. In the case where the paper is inbetween, I felt like my evaluations were noisy. Without clear definitions for the points, (1 pt = algorithm described fully, 2 pts = algorithm contains complexity analysis, 3 pts = algorithm has proof or reference to proof, ...) it was hard to decipher whether to give the criterion a 1, 2, 3, or 4 (hardest between 2 and 3). This noise would diminish the use of ranking by "reproducibility score" or some other point based system. I will note that this noise could very well just be an artifact of my experience level but that was just my experience with using the points. In the SIGPLAN checklist, the authors noted that their checklist doesn't require a binary (yes/no) answer, but instead they will often leave a box half marked as their form of nuance. This is less nuanced than the points but also less noisy. Another contribution to this noise is the lack of examples/counterexamples. Most of the checklists I felt could have provided a better suite of examples. There were also some criteria I didn't find particularily useful from a few of the checklists. From the cTuning checklist, these were the required workflow preparation time criterion and maybe the transformations criterion. I also wasn't sure about how important random seeding was as it's own cirerion in the AAAI checklist.
## Looking at the score system
I used three different checklists for three different papers (minus one for not using the NeurIPS checklist on the ck paper), for a total of 8 different evaluations. Since I used a point system for these checklists, below is a table showing "how well" a paper did for a particular checklist. Since I added the ability to turn off/on criteria, there may be differences in total points for the same checklists across papers.

| Paper | Checklist | Score |
|-------|-----------|-------|
| Collective Knowledge Workflow | cTuning | 85/85 (100%) |
| Collective Knowledge Workflow | AAAI | 60/65 (92%) |
| Playing Atari with Deep Reinforcement Learning | cTuning | 29/60 (48%) |
| Playing Atari with Deep Reinforcement Learning | AAAI | 34/55 (62%) |
| Playing Atari with Deep Reinforcement Learning | NeurIPS | 32/60 (53%) |
| ImageNet Classification with Deep Convolutional Neural Networks | cTuning | 50/70 (77%) |
| ImageNet Classification with Deep Convolutional Neural Networks | AAAI | 60/70 (85%) |
| ImageNet Classification with Deep Convolutional Neural Networks | NeurIPS | 68/80 (85%) |

As you can see, there are similarities of how well a given paper did from checklist to checklist but also some noise. Some of this noise is to be expected just from the different questions and framing of questions across checklists.
