# Twitter-Sentiment

Sentiment Analysis of Tweets

*TwitterSentimentAnalysis.ipynd*
Models trained on Kaggle Twitter Sentiment Analysis data set (https://www.kaggle.com/c/twitter-sentiment-analysis2/data)

Implements a few different models on a subset of training data to evaluate their accuracy:
  - Naive Bayes with term frequency inverse document frequency (TfIdf): Precision = 73%, Recall = 73%, F1 = 72%
  - Support Vector Classification with term frequency inverse document frequency (TfIdf): Precision = 32%, Recall = 56%, F1 = 40%
  - Naive Bayes without term frequency inverse document frequency (TfIdf): Precision = 76%, Recall = 76%, F1 = 76%
  - Support Vector Classification without term frequency inverse document frequency (TfIdf): Precision = 32%, Recall = 56%, F1 = 40%

*Twitter API*
Integrates with Twitter API using python-twitter library to get trends and individual tweets of the trends (https://github.com/bear/python-twitter)

Employs Naive Bayes model on trending tweets to perform sentiment analysis and identify positive and negative tweets

Utilises schedule library to automate scripts https://schedule.readthedocs.io/en/stable/

Tweet and Trend responses saved to CSV and sent from EC2 instance to S3 using boto library https://boto3.amazonaws.com/v1/documentation/api/latest/index.html

*Deployment*
Scripts are deployed on Amazon EC2 instance, automated using schedule library, outputs are saved as CSV's in the instance and also copied to Amazon S3 instance for retention

Data visualization of Twitter Trends implemented in ClicData, https://clicdata.com dashboard available here: https://ciarancarroll.clicdata.com/v/xVPFUAtNVmCT
