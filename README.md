# RedditCoin
Analysis of reddit and whether it is reactive or proactive in terms of cryptocurrencies prediction 

## Github Link: https://github.com/JosephAugustine17/RedditCoin 

## Website: https://josephaugustine17.github.io/RedditCoin/ 

## Abstract 

People are on a continual mine for wealth searching for the next biggest phenom in order to jump that bandwagon earlier than sooner. The most recent phenomenon that has been taking the world by storm is cryptocurrency.  From BItcoin to Squid coin the world of crypto is continually expanding rapidly however many people are stuck in the unknown when trying to determine what crypto to invest into. Rather than base decisions solely on impulsivity some buyers may choose to seek rational advice from an external source such as social media. If they however seek external help they are left in a difficult decision of trusting information being echoed through media platforms. Our project will tackle the above by attempting to show a relationship between the value of low-valued crypto currencies and their popularity on multiple subreddits. We will also analyze if reddit is reactive or proactive in terms of cryptocurrencies and for which currency is it proactive and reactive.

## Research Questions 
1. What is the relationship between popularity of coin’s mentioned on reddit and value of coins in the real world for low valued bitcoins?

2. Does a surge in popularity due to posts and comments  on reddit map to increases in value for certain cryptocurrencies?

3. Can specific subreddits predict increases in value based on increases in popularity through posts/comments?
 
4. What crypto that is most and least talked about through crypto subreddit?

5. Do surges in popularity on reddit map directly to the volume of transactions made per cryptocurrency?

6. Do surges in popularity on reddit and twitter  map directly to the volume of transactions and price increase  made per cryptocurrency?


## Proposed additional datasets:

### Crypto dataset 
We intend to use a dataset of current cryptocurrencies that is located on the webpage CoinMarketCap. This will help us map  blocks of text within reddit to  realtime cryptocurrencies through both their names, and their symbol. Getting this data involved scraping data from the webpage and parsing the data as wanted. The size of the data was not large enough to raise concerns. However the format of certain coin’s raise concern. There are coins that are named as commonly used words such as “ALL'', ``ONE'', ''THE”. This will mainly be gathered through a dataset which contains the historical prices of all cryptocurrencies such as open,closes, and transactions through multiple days on certain blockchains such as CoinBase(https://www.cryptodatadownload.com/data/). Additionally their symbols are commonly used symbols such as the coin with a symbol “A”. Searching for this symbol within subreddit posts and comments is simple however it will overcount very easily. This is why we will focus on subreddits that avoid this problem.  

### Crypto  Market Data
This will mainly be gathered through a dataset which contains the historical prices of all cryptocurrencies such as open,closes, and transactions through multiple days on certain blockchains such as CoinBase(https://www.cryptodatadownload.com/data/). We intend to use this  dataset to compare the price of a coin within certain timelines.This will enable us to make connections to the popularity and value of a coin. Additionally data about the volume of transactions of coins made during certain timelines will be pulled to make comparisons.


# Methods

We will perform our analysis on both the the comment and submission datasets because they cover most of the popular crypto subreddits and is an appropriate size to be able to work with it.

Before we start to answer our questions we will perform some exploratory analysis which we did on the milestone report to get an understanding of the data. To do this exploratory analysis the data must be cleaned. We will clean the data by removing rows with missing values in specific columns, then we parsed the date used a date parser so it can be used in analysis later.

With the missing data removed we are ready to perform exploratory data anaysis which was performed on our milestone report. We wanted to get an understanding of the data so we decided to use visualization techniques focusing on specific features like score, subreddit, and date. Using bar graphs we analyzed the score by looking at the frequency, this graph was unreadable so we used the log to make the graph readable. We performed various analysis on the date grouping by day, month, and year and seeing how post frequency varies using bar graphs. Finally we looked at the different subreddits utilizing key work searches to see if there even are crypto subreddits to do our project on. We discovered the most popular subreddits using graphs and decided which ones to focus on.

Relating to our project we wanted to do size by size visual comparisons of reddit scores of certain crypto and their price over time using line graphs. So in our milestone we decided to start by getting a count of how many times a crypto is mentioned throughout the entire dataset and find the most and least popular coins. To count the score of each cryptocurrency we needed a list of valid cryptocurrencies so we webscraped a list because there is no list easily available to download including extremely unknown currencies. We used both the symbol and name of a cryptocurrency because both a commonly used. We discovered through bar graphs that Swap is the most popular and BitWhite is the least popular.

In the final report we now want to now count the score of a crypto per day instead of for the entire time like in the milestone. So we created dataframes where there was a row for each crypto for each day. We also improved the search by using a list of popular subreddits that we researched. The submission and comment data was then used to perform a search on the body and text data looking for the symbols and names of cryptocurrency webscraped and tracked on the dataframes created. In this search there were 4 distinct searches (Crypto Name and Submission Data), (Cryto Symbol and Submission Data), (Crypto Name and Comment Data), and (Crypto Symbol and Comment Data). We searched for the former in the latter of the pairs and aggregated the results into a single dataframe. This search was intensive as the datasets were quite large but we utilized hash maps to reduce search times to O(1).

We are now ready to properly answer what crypto are most and least popular. Grouping by each crypto name and aggregating the score over the days we found the most popular and least popular which are THENODE and H3X. We exprected Bitcoin to be first and then realized that the symbol for THENODE is A which is used in many sentences.


# Organization: 

We are doing everything together, utilizing pair programming

Azim Hirjani hirjania 1004191938

Joseph Augustine august51 1004183965


