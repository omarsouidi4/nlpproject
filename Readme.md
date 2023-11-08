# Football Match Event Prediction

## Project Overview
This project focuses on the analysis of football match commentary to predict whether a particular action will result in a goal. Using a dataset from Kaggle, the goal is to preprocess the text data and develop a model capable of making accurate predictions.

## Dataset
The datasat used in this project is comprised of detailed commentary from soccer matches and can be found here https://www.kaggle.com/datasets/secareanualin/football-events/data

## Models and Performance
We began this projct by creating a pre-processing pipeline to clean and prepare the textual comments from football matches. This involved removin special characters, converting to lower case, removin empty words, and lemmatisin to reduce words to their basic form.

Followin this, we built a basic model, a logistic regression, to establish an initial baseline of the model's ability to predict the outcome of the actions described in the comments, namely whether they ended in a goal. The performans of this initial model revaled perfect accuracy, leadin us to suspect a significant imbalance in the distribution of classes.

To address this, the SMOTE technik was implemented, increasing the diversity of minority class examples in our training set. Although this methode slightly reduced the accuracy from 1 to 0.99, it contributed to a more generalisable and less biased model.

The next step was to adopt a more sophisticated approach by exploiting the power of recurrent neural networks. To this end, TensorFlow was used to train an LSTM model, chosen for its ability to capture long-term dependencies in textual data. This sequential model provides a deep understanding of word sequences and their context, which is essential for accurate comment-based event prediction.

The LSTM model was evaluated and showed an accuracy close to 0.98, confirming its competence and reliability in predicting goals from text data. It should be noted that the majority of comments do not lead to a goal, which justifies the use of SMOTE to balance the data set and thus improve the reliability of the system.
## Installation
To run this project, follow these steps:

1. Clone the repository: https://github.com/omarsouidi4/nlpproject

2. Install the required libraries: pip install -r requirements.txt


## Usage
To execute the project code, navigate to the project notebook called "notebook" and run cell by cell.

