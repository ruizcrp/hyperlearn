# HyperLearn

WORK IN PROGRESS! :small_red_triangle::small_red_triangle::small_red_triangle:

This space is for the project for the SDSC Hackathon on Gen AI 2023. HyperLearn stands for Hyper-Personalized Learn Optimization Tool. It is a working title - any better name suggestions are very welcome :wink:

You can contact me under the gmail-address: ruiz.crp

See the link https://sdsc-hackathons.ch/projectPage?projectRef=DHepetK0DLQ6cRMVcvPb|rt0UoB2tZng7d5TSUtti for the project proposal and a description of the idea.

There is a number of issues in this project, which is going to be elaborated here as a preparation for the hackathon:
1) How to tackle the Hyper-Personalization.
2) Data: Open Educational Resources for fine-tuning?
3) Quality of data and of answer: Knowledge-Graph solution?
4) What would be the plan for the hackathon?

# Discussion / Research

### 1) How to tackle Hyper-Personalization

### 2) Data: Open Educational Resource for fine-tuning?

The question generally is, whether OER can be used at all for this task as they usually are unstructured and the quality is of all sorts. Note also that there might be licensing issues when using data - I'm trying to always state the license. I will try to structure here in several different kinds of data sources:

1. Grammatical Error Corrections
2. Exercises: Text. Structured.
3. Exercises: Text. Unstructured. 
4. Exercises: Audio and Video
5. Other probably useful sources
6. Maybe unusuable but interesting nevertheless

#### 2.1 Grammatical Error Corrections (GEC)

GEC are structured datasets that are often created by universities. They contain sentences and some sort of error coding. Unfortunately, it seems that the methods are not congruent among them.

- NUS Corpus of Learner English (NUCLE). I filled out the requested form and am waiting for the reply. Also a non-commercial license.
- [CoNLL-2014 Shared task](https://www.comp.nus.edu.sg/~nlp/sw/10gec_annotations.zip). [Data can be downloaded here](https://www.comp.nus.edu.sg/~nlp/sw/10gec_annotations.zip). There is also an [interesting paper on that here](https://www.comp.nus.edu.sg/~nlp/conll14st/CoNLLST01.pdf).
- There is [here a nice list with currently 14 GEC datasets](https://paperswithcode.com/datasets?task=grammatical-error-correction&page=1). Among them [JFLEG](https://paperswithcode.com/dataset/jfleg) also [WI-LOCNESS](https://paperswithcode.com/dataset/locness-corpus) were often cited in the literature.
- [The C4_200M Synthetic Dataset for GEC](https://blog.research.google/2021/08/the-c4200m-synthetic-dataset-for.html) was published by Google. [Github repo is here](https://github.com/google-research-datasets/C4_200M-synthetic-dataset-for-grammatical-error-correction), and [data is on kaggle](https://www.kaggle.com/felixstahlberg/the-c4-200m-dataset-for-gec) (approx 10 GB). But [Google's C4 dataset](https://www.tensorflow.org/datasets/catalog/c4) is also required to make the match with the hashes in it (806 GB).
- Russian grammatical error correction [RULEC-GEC](https://github.com/arozovskaya/RULEC-GEC). I filled out the requested form and asked the responsible person for obtaining the dataset. CC 4.0 by-sa.
- For Russian there is also [ReLco which is openly available under MIT license](https://github.com/Askinkaty/Russian_learner_corpus_ReLCo)

There is [here also a tutorial on how-to fine-tune a transformer model on GEC](https://www.vennify.ai/fine-tune-grammar-correction/).



#### 2.5 Other sources that could be useful

- [English word frequency](https://www.kaggle.com/datasets/rtatman/english-word-frequency)
- [List of Russian idioms](https://www.kaggle.com/datasets/lpshkn/russin-idioms-phraseologisms)


#### 2.6 Maybe unusable but interesting nevertheless

- Junyi Academy: Kaggle dataset for the optimization of math excercises. However, the actual math-questions are not published (only the titles), and thus it does not seem useful if we really want to fine-tune: https://www.kaggle.com/datasets/junyiacademy/learning-activity-public-dataset-by-junyi-academy?select=Log_Problem.csv. CC4.0by-nc-sa.





### 3) Quality of data and of answer: Knowledge-Graph solution?

An important issue are wrong answers. As mentioned in the proposal, I tried llama2 to ask for simple Russian exercises to learn. I now also tried to tell him that he is an English teacher and is here to teach me. The conversation was quite interesting. It started then indeed with some exercises to spot for example the difference between "its" and "it's". But when I asked him to make more difficult exercises, he quickly started to hallucinate and created many wrong exercises and confusing answers.

The bottomline is: How to make sure that the questions and answers are correct?



### 4) Plan for hackathon

Please add here your thoughts. This is just a flexible proposal.

- Thinking and discussing together which solutions to use/try
- Download OER(?)-Data on S3 or other place
- Preparation of data to have it in a usable format
- Preparation of language model (llama2, mirage,...?)
- Fine-tuning of the model
- Exploration of the solution
- Back to new exploration loops.. :-)
- Preparation of a demo-UI for the final presentation

There are many things still missing here. 



[![CC BY-SA 4.0][cc-by-sa-shield]][cc-by-sa]

This work is licensed under a
[Creative Commons Attribution-ShareAlike 4.0 International License][cc-by-sa].

[![CC BY-SA 4.0][cc-by-sa-image]][cc-by-sa]

[cc-by-sa]: http://creativecommons.org/licenses/by-sa/4.0/
[cc-by-sa-image]: https://licensebuttons.net/l/by-sa/4.0/88x31.png
[cc-by-sa-shield]: https://img.shields.io/badge/License-CC%20BY--SA%204.0-lightgrey.svg