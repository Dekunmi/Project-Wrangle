# Project: Wrangle and Analyze WeRateDogs Data
## by Rachael Olakunmi Ogunye

## Introduction
> The purpose of the project is to put into practice all that I learnt from the Data Wrangling lesson in the Data Analysis Nanodegree offered by Udacity. The dataset I wrangled is the tweet archive @DogRates, also known as @WeRateDogs. WeRateDogs is a Twitter account that rates individual’s dogs with a humorous comment about the dogs. This ratings almost always have a denominator of 10.

### Project Goal:
> The project's goal is to effectively wrangle WeRateDogs Twitter data to create interesting analyses and visualization. The Twitter archive is great but additional gathering, assessing and cleaning was required before analysis.

### Project Details:
> This report highlights the various steps I took to obtain a clean dataset ready for analysis.

#### Gathering Data
> The three different datasets used in this project were obtained as follows:

1) **Enhanced Twitter Archive file**: This was provided by Udacity. I manually downloaded this file by following the link provided in the classroom, twitter_archive_enhanced.csv, I then upload it into my Jupyter notebook workspace and read the data into a pandas DataFrame. I imported the pandas library as it's 'pd' and used the pandas '.read_csv()' function to read the file into the dataframe named 'df_enhanced'.

2) **Tweet Image Prediction file**: This file (image_predictions.tsv) is present in each tweet according to a neural network. It is hosted on Udacity's servers and was downloaded programmatically using the Requests library and the following URL: https://d17h27t6h515a5.cloudfront.net/topher/2017/August/599fd2ad_image-predictions/image-predictions.tsv I import the Python requests and os libraries. With the '.get()' function of the requests library, I obtained the data through its url and saved it in a response variable. Response displayed 200, an HTML code for successful. Then using the 'with open' function, the content was saved to a 'tsv' file in the same working directory. I then read the downloaded tsv file into the dataframe named 'df_image_predictions'.

3) **Tweet_Json text**: I accessed this file without a twitter account by reading the tweet_json.txt file, provided by Udacity, line by line with the Python 'with open' function and a 'for' loop into a pandas DataFrame, called 'df_tweets' with (at minimum) tweet ID, retweet count, and favorite count.

#### Assessing Data
**Visual Assessment**: Each of the gathered DataFrames above was displayed in the Jupyter Notebook for visual assessment purposes. The DataFrames were also assessed in an external application (Excel).

**Programmatic Assessment**: I assessed programmatically using the various pandas' functions and methods such as; '.head()', '.tail()', '.info()', '.describe()', '.isnull()', '.sample()', '.duplicated()', and '.value_counts()'.

> At the end of the assessment process, eight(8) quality issues and two(2) tidiness issues were observed.

#### Storing Data
> The cleaned master DataFrame was stored in a CSV file named 'twitter_archive_master.csv'.


### Key Insights from the Analysis 

1. The DataFrame has a total of 21 columns and 1994 rows (entries)

2. All columns are completely filled except the 'dog_stage' column which has missing values.

3. The minimum favorite count is 81 while the maximum favorite count is 132810.

4. The minimum retweet count is 16 while the maximum retweet count is 79515.

5. Quite a good number of dogs have no names (about 32%).

6. The most common dog type is Labrador Retriever.

7. The pupper stage is the most popular while the floofer stage is the least popular.

8. p2 is the most successful algorithm while p3 is the least successful algorithm


### Conclusion

> This was an exciting project. Although I had a number of challenges, I took time to trace the source of errors, recheck codes and read documentations. I am now familiar with using Python programming language and its packages to successfully wrangle data and gain insights from the data. This is all part of the process of becoming a better Data wrangler.

