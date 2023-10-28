# HyperLearn

This space is for the project for the SDSC Hackathon on Gen AI 2023. HyperLearn stands for Hyper-Personalized Learn Optimization Tool. It is a working title - any better name suggestions are very welcome ;-)

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

GEC are structured datasets that are often created by universities. They contain sentences and some sort of error coding. For example on position 3 you have

- Russian grammatical error correction [RULEC-GEC](https://github.com/arozovskaya/RULEC-GEC). I filled out the requested form and asked the responsible person for obtaining the dataset.


### 2.5 Other probably useful sources

- [English word frequency](https://www.kaggle.com/datasets/rtatman/english-word-frequency)


### 2.6 Maybe unusable but interesting nevertheless

- Junyi Academy: Kaggle dataset for the optimization of math excercises in CC4 license. However, the actual math-questions are not published (only the titles), and thus it does not seem useful if we really want to fine-tune: https://www.kaggle.com/datasets/junyiacademy/learning-activity-public-dataset-by-junyi-academy?select=Log_Problem.csv





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