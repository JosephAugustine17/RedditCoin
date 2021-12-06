# RedditCoin
Analysis of reddit and whether it is reactive or proactive in terms of cryptocurrencies prediction 

## Github Link: https://github.com/JosephAugustine17/RedditCoin 

## Website: https://josephaugustine17.github.io/RedditCoin/ 

## Abstract 

People are on a continual mine for wealth searching for the next biggest phenom in order to jump that bandwagon earlier than sooner. The most recent phenomenon that has been taking the world by storm is cryptocurrency.  From BItcoin to Squid coin the world of crypto is continually expanding rapidly however many people are stuck in the unknown when trying to determine what crypto to invest into. Rather than base decisions solely on impulsivity some buyers may choose to seek rational advice from an external source such as social media. If they however seek external help they are left in a difficult decision of trusting information being echoed through media platforms. Our project will tackle the above by attempting to show a relationship between the value of low-valued crypto currencies and their popularity on multiple subreddits. We will also analyze if reddit is reactive or proactive in terms of cryptocurrencies and for which currency is it proactive and reactive.

## Research Questions 
1.What is the relationship between popularity of coin’s mentioned on reddit and value of coins in the real world for low valued bitcoins?

2. Does a surge in popularity due to posts and comments  on reddit map to increases in value for certain cryptocurrencies?

3. Can specific subreddits predict increases in value based on increases in popularity through posts/comments?
 
4. What crypto that is most and least talked about through crypto subreddit?

5. Do surges in popularity on reddit map directly to the volume of transactions made per cryptocurrency?

6. Do surges in popularity on reddit and twitter  map directly to the volume of transactions and price increase  made per cryptocurrency?


## Proposed additional datasets:

### Crypto dataset 
We intend to use a dataset of current cryptocurrencies that is located on the webpage CoinMarketCap. This will help us map  blocks of text within reddit to  realtime cryptocurrencies through both their names, and their symbol. Getting this data involved scraping data from the webpage and parsing the data as wanted. The size of the data was not large enough to raise concerns. However the format of certain coin’s raise concern. There are coins that are named as commonly used words such as “ALL'', ``ONE'', ''THE”. This will mainly be gathered through a dataset which contains the historical prices of all cryptocurrencies such as open,closes, and transactions through multiple days on certain blockchains such as CoinBase(https://www.cryptodatadownload.com/data/).. Additionally their symbols are commonly used symbols such as the coin with a symbol “A”. Searching for this symbol within subreddit posts and comments is simple however it will overcount very easily. This is why we will focus on subreddits that avoid this problem.  

### Crypto  Market Data
This will mainly be gathered through a dataset which contains the historical prices of all cryptocurrencies such as open,closes, and transactions through multiple days on certain blockchains such as CoinBase(https://www.cryptodatadownload.com/data/).We intend to use this  dataset to compare the price of a coin within certain timelines.This will enable us to make connections to the popularity and value of a coin. Additionally data about the volume of transactions of coins made during certain timelines will be pulled to make comparisons.


# Methods

There is a data cleaning process to remove values that are null or missing.

We performed initial analysis on the entire dataset creating visualizations for specific columns like score, subreddit, and date. Then we selected specific cryptocurrency subreddits and performed further analysis on the same columns. Using the specific subreddits we created a 
dataset per day of how many times each cryptocurrency is mentioned. We will do this using the Reddit dataset provided and a dataset of cryptocurrency names and symbols that was created by us using web scraping. Using the results we could find which cryptocurrencies were mentioned the most.

Our goal is to then use historical cryptocurrency data and generate visualizations with the volume, price, score and date allowing us to determine the relationship for each cryptocurrency.

# Organization: 

We are doing everything together, utilizing pair programming

Azim Hirjani hirjania 1004191938
Joseph Augustine august51 1004183965:


