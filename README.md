# Kaggle-TweetSentimentExtraction
 

## Intro: 
This project was done in response to the [Tweet Sentiment Extraction](https://www.kaggle.com/c/tweet-sentiment-extraction) dataset. 
Sadly, I came across this contest too late and it was already closed. Since it is closed they will not grade my submission, but I still went through the excercise because I thought this was an interesting problem.

Analyzing social media posts is always challenging due to the dialect of the internet not being very consistent. There are a lot of typos, shorthand, and slang words. English is a living language. 

Extracting sentiment can be a very useful tool for people who have to sift through a lot of pages of text daily. It may highlight the important words for a doctor or lawyer to help them choose the best course of action. It can help you understand the voices of your customers and employees. [According to *Fortune Business Insights* the NLP market is said to be growing at about ~30% CAGR according](https://www.globenewswire.com/news-release/2020/06/08/2045035/0/en/Natural-Language-Processing-NLP-Market-to-Exhibit-32-4-CAGR-Increasing-Technological-Advancement-to-Drive-Growth-Fortune-Business-Insights.html)

## Summary:
We used the Fastai software and the ULMFiT method popularized by Jeremy Howard, et al. We used the [AWD_LSTM model](https://arxiv.org/abs/1708.02182) as a starting point and then trained our language model on our tweet text data. From there we built out a sentiment classifier to predict the sentiment of the text. We used intrinsic attention to find the weights of each word produced by the output tensor of the classifier and then established a minimum threshold of weights. Whatever consecutive string of words that were above that threshold were then deemed our extracted text.

[Please check out a brief non-technical presentation on this project.](https://github.com/bsamaha/Kaggle-Tweet-Sentiment-Extraction/blob/master/Non_technical_pres.pptx)

## Google Colab
Since my local machine's GPU does not have CUDA capability I completed this project in Google Colab. Due to all of the model's being quite large (100 MB+) I was unable to upload them to GitHub. The models (language model, language encoder, and classification model) can easily be reproduced by opening the notebook in Colab, uploading both CSVs located in the data folder of this GitHub repository, and then run the notebook in full.

Watch the gif below to learn how to quickly access a GitHub notebook in Google Colab. 

Copy and paste: **bsamaha/Kaggle-Tweet-Sentiment-Extraction**

![How to load a Notebook in Google Colab](https://github.com/bsamaha/Kaggle-Tweet-Sentiment-Extraction/blob/master/How_to_upload_notebook.gif)





