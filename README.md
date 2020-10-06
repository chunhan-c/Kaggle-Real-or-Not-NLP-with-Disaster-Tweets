# Kaggle-Real-or-Not-NLP-with-Disaster-Tweets

此項目為Kaggle於2019年12月20號所舉辦之NLP分類比賽，目標為應用機器學習，讓模型能正確分辨人類寫的推特內容，是否是關於"真實的"災害。
比賽網址與數據來源: https://www.kaggle.com/c/nlp-getting-started


此github展示了EDA, Text prepocessing, Google Pretrained W2V之應用,不同的LSTM(Multiple input LSTM, One Directional LSTM, BIdirectional LSTM)。      
最後以3層 Birectional LSTM 得到了 F1 score: 0.81673, 排名373/ 1315。

![image](https://github.com/chunhan-c/Kaggle-Real-or-Not-NLP-with-Disaster-Tweets/blob/master/Rank%20of%20Real%20or%20Not.png)

以下為各模型之Accuracy, Val loss, Training Time:  

Multiple Inputs(30 epochs):  
Multiple Inputs 是指額外新增除了文字的variables, 例如: 文字字數。
![image](https://github.com/chunhan-c/Kaggle-Real-or-Not-NLP-with-Disaster-Tweets/blob/master/multiple_inputs_30e.png)

LSTM (one layer):  
![image](https://github.com/chunhan-c/Kaggle-Real-or-Not-NLP-with-Disaster-Tweets/blob/master/one_d_lstm_1y_10e.png)

Birectional LSTM (one layer):  
![image](https://github.com/chunhan-c/Kaggle-Real-or-Not-NLP-with-Disaster-Tweets/blob/master/bi_1y_15e.png)

Birectional LSTM (two layer):  
![image](https://github.com/chunhan-c/Kaggle-Real-or-Not-NLP-with-Disaster-Tweets/blob/master/bi_2y_15e.png)

Birectional LSTM (three layer):  
![image](https://github.com/chunhan-c/Kaggle-Real-or-Not-NLP-with-Disaster-Tweets/blob/master/bi_3y_20e.png)  
  
  
以下為各模型之 Kaggle Score(F1 score):
![image](https://github.com/chunhan-c/Kaggle-Real-or-Not-NLP-with-Disaster-Tweets/blob/master/models_scores.png)  
  
  
以下為各模型之 Training Time (單位: 秒):
![image](https://github.com/chunhan-c/Kaggle-Real-or-Not-NLP-with-Disaster-Tweets/blob/master/trainings_times.png)


總結:
可以從上兩張圖看出三層的Birectional LSTM模型對於這個dataset來說 Kaggle F1最高，其次為單層的Birectional LSTM模型。
但是也因為三層的Birectional LSTM模型相比之下較深，所需訓練時間為 3.0396秒/epoch，為單層Birectional LSTM訓練時間(0.684秒/epoch)的4倍以上。  
考量到兩模型之F1 score相差僅小於0.001，時間成本相差4倍以上，且較深的模型通常訓練時間較久，時間限制高的情況下，單層Bidirectional LSTM會是較為合適之模型。



