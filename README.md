# SMS spam detection using Bidirectional Encoder Representations from Transformers[BERT]

[![GitHub license](https://img.shields.io/badge/license-MIT-blue.svg)](https://github.com/ekramasif/SMS-Spam-Prediction-Using-BERT/blob/main/LICENSE)

## Objective
> To develop an efficient translation-free recurrent neural architecture using BERT to perform SMS spam detection which actually remembers the context of SMS.

This is based on the context of message rather than the contact numbers, from where SMS is arrived.

## Plan of Attack

1. Data Aquisition
2. Text Preprocessing
3. Model
4. Results

### 1. Data Aquisition

Collected dataset from [kaggle](https://www.kaggle.com/uciml/sms-spam-collection-dataset), that contains only english messages.
We also added our own dataset, collected from real world messages that is of three languages English, Hindi, Telugu. We manually labelled the data into SPAM or HAM.

Dataset consists of three columns index, sms, label. label = { SPAM, HAM}

Total dataset contains around 5214 records. Its an unbalanced dataset, because we have 50% of them as HAM messages and remaining 50% SPAM messages.

```
942	spam	How about getting in touch with folks waiting ...
2278	ham	Hmm...Bad news...Hype park plaza $700 studio t...	
15	spam	XXXMobileMovieClub: To use your credit, click ...	
2327	spam	URGENT! Your mobile number *************** WON...	
5214	spam	Natalja (25/F) is inviting you to be her frien...	
```


### 2. Text Preprocessing

I use [BERT Preprocessed](https://tfhub.dev/tensorflow/bert_en_uncased_preprocess/3) and [BERT Encodin](https://tfhub.dev/tensorflow/bert_en_uncased_L-12_H-768_A-12/4) for Processed text.


### 3. Model

      Activation = 'sigmoid'
      Accuracy = 'accuracy'
      optimizer = 'adam'
      loss = 'binary_crossentropy'
      Precision = 'precision'
      Recall = 'recall'
      
      
      
 ### 4.Result
 
 
                        precision    recall  f1-score   support

                 0       0.95      0.91      0.93       187
                 1       0.92      0.95      0.93       187

          accuracy                           0.93       374
         macro avg       0.93      0.93      0.93       374
      weighted avg       0.93      0.93      0.93       374
      
      
      
<p align="center">
  <h2 align="center">All credit goes to</h2>
</p>

<p align="center">
  <a href="https://ekramasif.me">
    <img align="center" src="https://raw.githubusercontent.com/ekramasif/ekramasif/main/EkramAsif.gif" width="15%">
  </a>
</p>
 
 
> Note: This is open source.

