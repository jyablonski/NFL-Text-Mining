# Super Bowl LIV Text Mining and Sentiment Analysis

This project goes through my process for analyzing Twitter & Reddit data on Super Bowl LIV.  I used a combination of the rTweet package & the Pushshift.io API to extract data, preprocessed & cleaned it in R, and utilized the tidytext package to analyze the text and get insights from the data.

![rnfl](https://user-images.githubusercontent.com/16946556/73687222-6b67a680-467e-11ea-963b-9dde77368b82.png)

This is an overview of the past 13 months of NFL related events, with the overall popularity measured by # of comments on the r/nfl subreddit.  Because I don't have access to the contents of the comments themselves, I decided to take a subset of data from Tweets from Twitter to get an idea of how people reacted to Super Bowl LIV.  The Twitter API limits you to only extracting 18,000 tweets at a time. 

![rnflTop25](https://user-images.githubusercontent.com/16946556/73687230-6efb2d80-467e-11ea-8849-646c53d47f0f.png)
Here are the top 25 most popular words in the Twitter Analysis after removing stop words such as and, if, for, to etc.

![rnfltweets](https://user-images.githubusercontent.com/16946556/73687228-6e629700-467e-11ea-8bab-4da71abc8745.png)
By applying the 'BING' sentiment we can separate words into positive or negative connotation.  You can see a much more significant amount of positive word counts rather than negative.

![rnflWordcloud1](https://user-images.githubusercontent.com/16946556/73687238-6efb2d80-467e-11ea-973e-26fdaaf0c721.png)
Because we're analyzing Super Bowl tweets, I filtered the word 'super' out of the positive list and recreated the graph.

![rnflNot](https://user-images.githubusercontent.com/16946556/73687235-6efb2d80-467e-11ea-8c81-6d12529a91e6.png)
Negation words like not, without, and no can have opposite meaning with the word they're associated with.  This chart includes words that were preceded by 'not' that the previous 2 graphs weren't able to take into account.  However because their number of occurrences is so low, we can be confident that it didn't have a meaningful impact on the analysis.

![comparisoncloudcolor](https://user-images.githubusercontent.com/16946556/73692062-6dcefe00-4688-11ea-8080-ffa8e06ecaaf.png)

This is a wordcloud version of the positive & negative sentiment analysis charts from above.  Blue is positive and red is negative.  The bigger the word, the more frequently it appears in the text analysis.

![rnflWordPairs](https://user-images.githubusercontent.com/16946556/73687229-6e629700-467e-11ea-9ff5-3bfad922275a.png)
This is a chart showcasing bigrams in the dataset; words that are located close to one another we're commonly tweeted in conjunction with one another.

![rnflpointer2](https://user-images.githubusercontent.com/16946556/73687231-6efb2d80-467e-11ea-806e-cb64751bc274.png)
Same concept but with arrows pointing towards the word pair.  The darker the arrow, the more common the word pair was.  Super Bowl and Andy Reid are among the most popular here. 

A common word pair throughout the analysis was the "Madden Curse", which is when a Pro Athlete who appears on the front cover of a video game title (Madden NFL 2020) suffers a major injury during that season.  Pat Mahomes dislocated his knee cap in mid October but went on to win the Super Bowl MVP this year, breaking the infamous "Madden Curse".

![rnflLog](https://user-images.githubusercontent.com/16946556/73687237-6efb2d80-467e-11ea-843d-6d6ceb731300.png)
This helps give an idea of how the top few words represent the majority of the text data (also known as the Pareto Principle).  There's only about ~20 words that have significant occurrences in the data before they start falling off.

![top6 words](https://user-images.githubusercontent.com/16946556/73688679-6a844400-4681-11ea-9b44-e8fb827f10bd.png)

Here are the top 6 most common words found in the tweets, which represent over 26.6% of the entire dataset.  You can see the majority of people are praising the Chiefs and Head Coach Andy Reid, who won his first Super Bowl as a Head Coach after more than 20 years with the Philadelphia Eagles and the Kansas City Chiefs.
