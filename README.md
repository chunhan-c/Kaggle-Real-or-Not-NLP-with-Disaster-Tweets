# Kaggle-Real-or-Not-NLP-with-Disaster-Tweets


This project is from a Kaggle Natural Language Processing (NLP) classification competition held on December 20, 2019. The goal is to apply machine learning to enable a model to accurately classify Twitter content written by humans as either being related to 'real' disasters or not. You can find more details about the competition and the data source here.

GitHub Showcase:

EDA (Exploratory Data Analysis)
Text Preprocessing
Application of Google Pretrained Word2Vec (W2V)
Different LSTM Models (Multiple Inputs LSTM, One Directional LSTM, Bidirectional LSTM)

The final model, using a 3-layer Bidirectional LSTM, achieved an F1 score of 0.81673, ranking 373rd out of 1315 participants (in the top 29%).

![image](https://github.com/chunhan-c/Kaggle-Real-or-Not-NLP-with-Disaster-Tweets/blob/master/Rank%20of%20Real%20or%20Not.png)

Below are details for each model, including Accuracy, Validation Loss, and Training Time:

Multiple Inputs (30 epochs):

Multiple Inputs refer to the inclusion of additional variables apart from text, such as the length of the text.
![image](https://github.com/chunhan-c/Kaggle-Real-or-Not-NLP-with-Disaster-Tweets/blob/master/multiple_inputs_30e.png)

LSTM (one layer):  
![image](https://github.com/chunhan-c/Kaggle-Real-or-Not-NLP-with-Disaster-Tweets/blob/master/one_d_lstm_1y_10e.png)

Birectional LSTM (one layer):  
![image](https://github.com/chunhan-c/Kaggle-Real-or-Not-NLP-with-Disaster-Tweets/blob/master/bi_1y_15e.png)

Birectional LSTM (two layer):  
![image](https://github.com/chunhan-c/Kaggle-Real-or-Not-NLP-with-Disaster-Tweets/blob/master/bi_2y_15e.png)

Birectional LSTM (three layer):  
![image](https://github.com/chunhan-c/Kaggle-Real-or-Not-NLP-with-Disaster-Tweets/blob/master/bi_3y_20e.png)  
  
  
Here are the Kaggle Scores (F1 score) for each model:
![image](https://github.com/chunhan-c/Kaggle-Real-or-Not-NLP-with-Disaster-Tweets/blob/master/models_scores.png)  
  
  
And here are the Training Times for each model (in seconds):
![image](https://github.com/chunhan-c/Kaggle-Real-or-Not-NLP-with-Disaster-Tweets/blob/master/trainings_times.png)


In summary, the three-layer Bidirectional LSTM model achieved the highest Kaggle F1 score for this dataset. However, it also required significantly more training time compared to the one-layer Bidirectional LSTM model. Considering the marginal difference in F1 scores and the much longer training time of deeper models, the one-layer Bidirectional LSTM appears to be a more suitable choice, especially when time constraints are a factor.



