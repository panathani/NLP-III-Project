# Question Answering System
## Introduction
Motivation: 
Question Answering 




Why is this task interesting or important?
What other people have done? What model have previous work have used? What did they miss? (1-2 paragraphs)
Summarize your idea
Summarize your results

# Our Approach/Methodology/Model
We use wanchan berta  

Explain your model here how it works.

Input is ...
Output is ...
Model description
Equation as necessary e.g. 

# Dataset
In this project, I will use thaiqa_squad dataset to build a QA model. The thaiqa_squad is an open-domain, extractive question answering dataset (4,000 questions in train and 74 questions in dev) in SQuAD format, originally created by NECTEC from Wikipedia articles and adapted to SQuAD format by PyThaiNLP. For further experiment, I created others 2 dataset for this project.
### Annotation guidelines
I created a test dataset based on Thai Wikipedia and Chulalongkorn University Rules. The topics were choosen randomly and selected interesting paragrahp. For each selected paragraph, I defined question and answer 1-2 questions on the content of the paragraph. I used Haystack Annotation Tool which provided a text field to type their question, and it could highlight the answers in the paragraph as well as export the data in SQUAD format. 

As a result, there are 3 datasets in this project
  
  1. QA Thai Wikipedia : Total 50 
  2. QA Chulalongkorn University Rules : Total 50 
  

#Experiment setup
I used Wangchan berta as a pretrain
Which pre-trained model? How did you pretrain embeddings?
Computer. How long?
Hyperparameter tuning? Dropout? How many epochs?

# Results
How did it go? + Interpret results.

Model comparison
Model	Accuracy
Logistic regression	67%
BERT	75%

# Conclusion
What task? What did we do?
Summary of results.
