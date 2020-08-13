# Kaggle-TweetSentimentExtraction
 

#### Intro: 
This project was done in response to the [Tweet Sentiment Extraction](https://www.kaggle.com/c/tweet-sentiment-extraction) dataset. 
Sadly, I came across this contest too late and it was already closed. Since it is closed they will not grade my submission, but I still went through the excercise because I thought this was an interesting problem.

#### Summary:
We used the Fastai software and the ULMFiT method popularized by Jeremy Howard, et al. We used the [AWD_LSTM model](https://arxiv.org/abs/1708.02182) as a starting point and then trained our language model on our tweet text data. From there we built out a sentiment classifier to predict the sentiment of the text. We used intrinsic attention to find the weights of each word produced by the output tensor of the classifier and then established a minimum threshold of weights. Whatever consecutive string of words that were above that threshold were then deemed our extracted text.

## Google Colab
Since my local machine's GPU does not have CUDA capability I completed this project in Google Colab. Due to all of the model's being quite large (100 MB+) I was unable to upload them to GitHub. The models (language model, language encoder, and classification model) can easily be reproduced by opening the notebook in Colab, uploading both CSVs located in the data folder of this GitHub repository, and then run the notebook in full.



