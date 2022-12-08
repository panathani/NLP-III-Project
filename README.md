# Question Answering System
## Introduction
Question answering (QA) is a computer science discipline within the fields of information retrieval and natural language processing (NLP), which is concerned with building systems that automatically answer questions posed by humans in a natural language. Nowaday, QA system is needed in many business because it would reduce the workload of customer service staff as well as improve customer experience through fast and accurate answer given. Delightfully, the researchers could develop a QA system to the point that it archeived a super human performance with the help of pre-train model in nlp. However, people still doubt whether this system understand the complex and human like questions since the current datasets are too simple. 
Therefor, I decided to challenge the current QA system to answer a human-like question and try to apply QA system to do the task on different domain. 

# Our Approach/Methodology/Model
I will train QA model with pre-train model **"BERT"**. Correspondingly, the input and output of model are defined as the following variable

- Given: p = paragraph, q = question
- Input = [CLS] q1, q2, q3,... [SEP] p1, p2, p3...
- Output = Start & End position of the answers


# Dataset
In this project, I will use thaiqa_squad dataset to build a QA model. The thaiqa_squad is an open-domain, extractive question answering dataset (4,000 questions in train and 74 questions in dev) in SQuAD format, originally created by NECTEC from Wikipedia articles and adapted to SQuAD format by PyThaiNLP. For further experiment, I created others 2 dataset for model testing.
### Annotation guidelines
I created a test dataset based on Thai Wikipedia and Chulalongkorn University Rules. The topics were choosen randomly and selected interesting paragrahp. For each selected paragraph, I defined question and answer 1-2 questions on the content of the paragraph. I used Haystack Annotation Tool which provided a text field to type their question, and it could highlight the answers in the paragraph as well as export the data in SQUAD format. Each answer was partitioned into one of the following categories: “date”, “person”, “location”, “other entity”, “common noun phrase”, “adjective phrase”, “verb phrase”, “clause”, and “other”.
As a result, there are 2 test datasets
  1. QA Thai Wikipedia : Total 50 
  2. QA Chulalongkorn University Rules : Total 20 
  

# Experiment setup
I used wangchanberta as a pre-train model and create model pipeline for Question-Answer
I tuning and set parameter as follow
- learning_rate=2e-5,
- batch_size = 16
- epoch = 1
- weight_decay=0.01,
The computation take around 25 minutes

# Results
### Model	Accuracy
Dataset | Exactmatch | F1
| --- | --- | ---
thai_qa_squad  | 44.6 | 57
QA Thai Wikipedia  | 21.3 | 48
QA Chulalongkorn University Rules  | 0 | 0

# Conclusion
In summary this project create QA model and test on the challenge answer.
