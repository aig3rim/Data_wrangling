# Data_wrangling
**Goal:** As a part of [Udacity's Data Ananlyst Nanodegree program](https://www.udacity.com/course/data-analyst-nanodegree--nd002), I had to wrangle WeRateDogs Twitter data to create interesting and trustworthy analyses and visualizations. The Twitter archive is great, but it only contains very basic tweet information. Additional gathering, then assessing and cleaning is required for "Wow!"-worthy analyses and visualizations.

## Data

1) **The WeRateDogs Twitter archive** contains basic tweet data for all 5000+ of their tweets, but not everything. One column the archive does contain though: each tweet's text, which I used to extract rating, dog name, and dog "stage" (i.e. doggo, floofer, pupper, and puppo) to make this Twitter archive "enhanced."

2) **Image Predictions file** a table full of image predictions (the top three only) using neural networks alongside each tweet ID, image URL, and the image number that corresponded to the most confident prediction (numbered 1 to 4 since tweets can have up to four images).

3) **JSON file with tweets** includes retweet count and favorite count. Using the tweet IDs in the WeRateDogs Twitter archive, I queried the Twitter API for each tweet's JSON data using Python's Tweepy library and stored each tweet's entire set of JSON data in a file called tweet_json.txt file.

## Getting started
You need an installation of Python, plus the following libraries:

* numpy
* pandas
* matplotlib.pyplot
* seaborn

## Insights
* Pupper is the most popular among defined dog stages. However, the majority of dog stages is not defined, what creates some uncertainties.
* The average rating for each dog stage is around 12. The most popular dog stage by the rating is Puppo. However, None values are presented and it creates some uncertainties.
* According to the number of retweets, Doggo and Puppo are the most popular among other dog stages.
* Puppo and Doggo are the most favorite dog stages, which have a significant number of favorite counts in comparison with other dog stages.
* As it was explained in the project, dog rating should >= 10, which is correct after data cleaning. Also, it should be noted that the majority of ratings belongs to the interval between 10 to 12.
* It's clear that retweets lie in the interval between 0 and less than 10,000. However, there are some number of outliers for tweets, which can be between 10,000 and 80,000.
* The number of favorite tweets vary between 0 to 3,000. However, there are some outliers, where the number of favorites lie between >3,000 and 16,000. 
* 50% of data for the confidence of prediction of a dog breed belongs to the interval between 0.4 to 0.85, where the mean probability is around 0.6.
