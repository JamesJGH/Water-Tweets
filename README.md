# Water-Tweets
**Sentiment analysis on tweets using Tweepy and TextBlob**

**Scraping Tweets and Sentiment Analysis**

The task was to analyse tweets around a specific topic and undertake sentiment analysis to categorise the tweets into either, positive, neutral, or negative around the topic.

**Dependencies**

Tweepy was used to retrieve the tweets from Twitter. Tweepy uses the Twitter developer API to scrape tweets allowing the use of filters such as topic and language. Using the twitter API does however add limitation in that only a maximum of 500 tweets from the last 7 days can be accessed. On a future project it would be worth exploring ways of obtaining more tweets from further back in time using a library such as GetOldTweets.

WordCloud was used to produce a word cloud graphic to visualise the frequency of words used and understand the main topics which appear in the tweets. NLTK was also used in the word cloud to generate stopwords from its standard library. 

Due to the limitation set by the twitter API it was not possible to collect enough data to train a model using the standard ‘train, test, split’ methods therefore TextBlob was used. TextBlob uses the pattern library analyser which overcomes the limitations of the data size and removes the need to train a model.

Pandas and Numpy were used to manage the data in dataframes.

The final output is a barplot showing number of positive, neutral and negative tweets, which seaborn and matplotlib were used to produce.

**Word Cloud**

Below is a copy of the word cloud created and identifies common words appearing in tweets and common topic areas. The stopwords appear to of done well in removing common words, however in further work more could be done to remove other words not relevant to the study such as ‘JHardacre’ and grouping of similar words including their slang such as ‘shooting’ and ‘shootin’. 

![alt text](https://raw.githubusercontent.com/JamesJGH/Water-Tweets/WordCloud.png)

**Frequency Distribution of Sentiment**

The dataframe was then fed into the TextBlob sentiment analyser, a new data frame was produced with the output including a label column (>1 for positive, =0 neutral and <1 for negative).
A percentage of each sentiment category was then calculated. 

- Neutral Percentage of responses: 44.06047516198704
- Positive Percentage of responses: 41.03671706263499
- Negative Percentage of responses: 14.902807775377969

Finally a barplot was created displaying the frequency of the sentiment categories.

 

**Areas for Further Study**

**Data Limits**
This study is only a snap shot in time with the limitation of the Twitter API. In future studies it would be worth exploring ways to overcome the limitation of the Twitter API or collect the data periodically. This would allow mapping changes in sentiment over time.
The data collected could also be improved by changes in the key words used for different commonly used labels on twitter.

**Common Words for Each Sentiment Category**
Further study should also build on the work done here by analysing common words for each sentiment category over time. This would identify common themes in tweet sentiment around the subject of the data.
This would be possible by applying the bag of words technique and tokenizing the tweets. This would provide lists of words for each sentiment category.

**Possible Limit on Sentiment Analyser**
It is possible that the sentiment analyser used had limited success on this data as it has a high amount of neutral results. While it could be possible the tweets were mainly neutral, further study using different sentiment models including newly trained models, should be explored to determine if the results are correct and improve upon them.
