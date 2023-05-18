# Sentimental-Analysis-of-SharkTank
### Research Question:
Sentiment Analysis on Twitter data on business reality television series “Shark Tank” . How is it the trending reality show on TV .Is it popular with positive reactions/ Negative reactions.

### Introduction:
If you ask any Indian middle-class family what type of investment they prefer, the answer would most likely fall somewhere between fixed deposits and mutual funds. Terms like equity, bull market, and gross margin would not be mentioned in the living room. However, that has changed. And it's all because of a single television show.
Nobody anticipated Shark Tank India to become such a surprise success. The reality television program has a straightforward idea that has proven successful in many nations across the globe. There are seven ‘sharks’, all of whom are accomplished entrepreneurs and industry titans, who watch aspiring entrepreneurs present their concepts for financing. The show involves a panel of "Sharks," or possible investors, who listen to entrepreneurs propose ideas for new businesses or products. These self- made multi-millionaires assess the business ideas and products presented before deciding whether or not to spend their own money in investing and mentoring each participant. Sixty-eight enterprises were chosen from among 62,000 applicants from India to present their concepts to the "sharks". It's become one of the most talked- about series on television. Its hashtags have gone viral on Twitter, and 'sharks' fan groups can't seem to stop posting parodies online. So, how did this business reality program spark the interest of the Indian audience and attract them? It's intriguing research to do sentiment analysis and observe people's reactions.
Apart from India, across the globe, there are 27 countries hosting this popular show including the United Kingdom, Ireland, Russia, Australia, Spain, Afghanistan, and Croatia.

### Citations:
• https://en.wikipedia.org/wiki/Shark_Tank_India • https://allsharktankproducts.com/about-this-site/

### Method:

### Data:
 For this study, 500 tweets from Twitter is collected. Access to a Twitter Developer Account will be used in this study to allow for more efficient Twitter data acquisition. The Tweepy python package will be used to obtain 500 Tweets via the Twitter API. When tweets are collected for this reality show with a location filter of “India” the drawback is there are not enough tweets collected that can be used for analysis. To collect appropriate threads, I have used the keyword “Shark Tank” and “shark tank Memes” to collect the tweets across the globe. This keywors are not case-sensitive. The tweets gathered from these keyword are merged into a single data frame. The libraries used in this process of collection of data are

### Packages:
1.os
2.pandas
3.csv
Another important concept used in the collection of data is snscrape.

### Snscrape:
Snscrape is a scraper for social media platforms (SNS). It scrapes information such as user profiles, hashtags, and searches and provides the results.
All Twitter APIs that return Tweets provide that data encoded using JavaScript Object Notation (JSON). JSON is based on key-value pairs, with named attributes and associated values. These attributes and their state are used to describe objects. At Twitter, we serve many objects as JSON, including Tweets and Users. This JSON file is then converted into a data frame.
The keywords to be searched are given into a text query. Then using the OS library to call CLI commands in Python data is gathered. Then it will read the JSON generated from the CLI command and creates a pandas data frame.
The data frame formed is used to perform analysis and get the sentiment of each tweet. The data frame is converted into a CSV file using the CSV library to form the dataset for this research question.
The number of tweets collected for “Shark Tank” is 380.
The number of tweets collected for “shark tank Memes” is 428. The total data collected for this study is 818 rows .

### Analysis:

### Sentiment Analysis:
 Sentiment analysis is a natural language processing (NLP) technique used to determine whether data is positive, negative, or neutral. Sentiment analysis is often performed on textual data to help businesses monitor brand and product sentiment in
 customer feedback, and understand customer needs.
 Why is it important?

### Interface and Packages used for this study :
 The purpose of sentiment analysis, regardless of the terminology, is the same: to determine a user's or audience's opinion on a target item by evaluating a large volume of text from numerous sources. You may examine text at varying degrees of depth,
 depending on your objectives.
  Jupyter notebook :
 The original web application for producing and sharing computational documents is Jupyter Notebook. It provides a straightforward, simplified, and document-focused
 environment.
 Advantages of using this platform:
 1. Language of choice
 2. Share notebooks
 3. Interactive output
 1.Textblob:
 TextBlob is a text processing library for Python 2 and 3. It offers a basic API for doing standard natural language processing (NLP) activities including part-of-speech tagging, noun phrase extraction, sentiment analysis, classification, and translation,
 among others.
 TextBlob is an emotion analyzer based on lexicon. It contains certain predetermined rules, or a word and weight dictionary, with some scores that assist compute the polarity of a statement. Lexicon-based sentiment analyzers are sometimes known as
 "Rule-based sentiment analyzers" for this reason.
 2.matplotlib.pyplot :
 This library is used for visualization and plotting.
3.re:
 Regular Expression, is a search pattern made up of a series of characters.
 4.WordCloud, STOPWORDS
 5.Image
 6.nltk.sentiment.vader -SentimentIntensityAnalyzer
 7.langdetect import detect
 8.nltk.stem import SnowballStemmer
 Code implemented to perform the analysis is implemented in python.
 Functions defined for Analysis of the dataset:
 Cleantweets:
 The next step in the analysis is to clean the tweet for punctuations, remove ‘@’,’#’,’:’,’_’ and hyperlinks. For this, the function “cleantweets” is defined using re package
 (Regular Expression).

 ### getSubjectivity:
 It is used for calculating the subjectivity of the tweet. Subjective statements usually refer to personal feelings, emotions, or judgments, whereas objective phrases refer to
 facts. Subjectivity is also a float with a value between 0 and 1.
 ### getPolarity:
 It is used for calculating the polarity of the tweet. Polarity is the perspective of the stated emotion is determined by the element's sentiment, which determines whether the text communicates the user's positive, negative, or neutral feeling toward the entity in question. Two new columns of subjectivity and polarity are added to the data frame.
  Figure 1: Subjectivity and Polarity
 ### Word Cloud:
 Simple text analysis is represented by word clouds, which are visual representations of text data. Word clouds show the most important or frequently used words in a
  passage of text.
A Word Cloud will often exclude the most frequent terms in the
 language ("a," "an," "the," and so on).

 
 ### Results:
 The popularity of the show is calculated by performing an analysis. A function is
 defined to classify the tweet into three categories. The three categories
 1. Positive
 2. Neutral
 3. Negative
 
 ### getAnalysis:
 This is defined to split the tweets based on the polarity score into positive, neutral, or negative. If the score calculated is less than zero then it is a negative tweet. If the score calculated is equal to zero it is considered a neutral tweet. Otherwise, it is
 considered a positive tweet. A new column “Analysis” is added to the data frame.
 After performing this analysis we can say what type of popularity this show got.
 Visualizing the type of popularity by tweets type.


 ### Conclusion and Limitations:
 We can see that there are more neutral reactions to this show than positive or negative when compared. However, the visualizations clearly show that the most talked about
 reality show “Shark Tank” has a positive response more than a negative response.
 Opinions may vary across different countries towards this show. The motive of this study was to study people’s sentiment in India, but this did not have enough tweets to filter. This is not because there are not so many tweets. Instead this study could be
 actually achieved if tweet was having a location tagged.
 
 ### References:
• https://github.com/MartinBeckUT/TwitterScraper/blob/master/snscrape/cli- with-python/snscrape-python-cli.py
• https://towardsdatascience.com/step-by-step-twitter-sentiment-analysis-in-
• https://towardsdatascience.com/step-by-step-twitter-sentiment-analysis-in-
%20python-d6f650ade58d
• https://link.springer.com/article/10.1007/s12065-019-00301-x
• https://monkeylearn.com/blog/sentiment-analysis-of-twitter/
• https://medium.com/dataseries/how-to-scrape-millions-of-tweets-using-
snscrape-195ee3594721
• https://youtu.be/ujId4ipkBio
           
  
