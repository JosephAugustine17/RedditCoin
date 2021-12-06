Authors: Joseph Augustine 1004183965, Azim Hirjani 1004191938

# Introduction
People are on a continual mine for wealth searching for the next biggest phenom in order to
jump that bandwagon earlier than sooner. The most recent phenomenon that has been taking
the world by storm is crypto. From Bitcoin to Squid coin the world of crypto is
continually expanding rapidly however many people are stuck in the unknown when trying to
determine what crypto to invest into. Rather than base decisions solely on impulsivity some
buyers may choose to seek rational advice from an external source such as social media. If they
however seek external help they are left in a difficult decision of trusting information being
echoed through media platforms. Our project will tackle the above by attempting to show a
relationship between the value of low-valued crypto currencies and their popularity on multiple
subreddits. We will also analyze if reddit is reactive or proactive in terms of cryptocurrencies and
for which currency is it proactive and reactive.

# Research Questions 

1. What is the relationship between popularity of coin’s mentioned on reddit and value of
coins in the real world for low valued bitcoins?
2. Does a surge in popularity due to posts and comments on reddit map to increases in
value for certain cryptocurrencies?
3. Can specific subreddits predict increases in value based on increases in popularity
through posts/comments?
4. What crypto that is most and least talked about through crypto subreddit?
5. Do surges in popularity on reddit map directly to the volume of transactions made per
cryptocurrency?
6. Do surges in popularity on reddit and twitter map directly to the volume of transactions
and price increase made per cryptocurrency?


# Data Collection and Cleaning 

## Reddit Data 
Submission data gathered from reddit

<img src="https://josephaugustine17.github.io/RedditCoin/docs/assets/submission_pre_clean.png" class="center" >
 
Comment data gathered from reddit 

<img src="https://josephaugustine17.github.io/RedditCoin/docs/assets/comment_pre_clean.png" class="center" >

Reddit submission data cleaned such that each column between "score", "title", "subreddit", "created_utc" would require values.
Reddit comment data cleaned such that each column between "score", "body", "subreddit", "created_utc" would require values.
Columns with empty values were dropped for both. 
<p align ="center">
<img src="https://josephaugustine17.github.io/RedditCoin/docs/assets/cleaned_data.png" class="center">
</p>
Additionally both submission and comment data was filtered out dates which did not contain numerical values. 

 <img src="https://josephaugustine17.github.io/RedditCoin/docs/assets/Date_filter.png" class="center" >

Reddit submission data was filtered to include subreddits with the names "btc", "BitcoinBeginners", "BitcoinMarkets", "BitcoinBeginners", "Bitcoin", "ethereum", "Vechain", "Ripple", "LitecoinMarkets", "dogecoin", "Monero", "Stellar" and any subreddit containing "crypto within the title.These are popular sub-reddits we researched.  

 <img src="https://josephaugustine17.github.io/RedditCoin/docs/assets/crypto_subreddits.png" class="center" >

## Crypto Symbol/Name Data 
Data about names and symbols of crypto's were gathered first from website CoinMarketCap. This was data was scraped from the web page and then parsed as needed. Symbols were cleaned as well removing symbols which were common english words. 

<img src="https://josephaugustine17.github.io/RedditCoin/docs/assets/common_words_filtered.png"  class="center" >


Each crypto was placed in a dataframe which maps a crypto to the number mentions made on a particular day initialized as 0.
 <p align ="center">
 <img src="https://josephaugustine17.github.io/RedditCoin/docs/assets/coin_counter.png"  class="center" >
 </p>
 Looped through each related submission and look for mention of a specific coin. Similarly done for commentsas well 
  <p align ="center">
  <img src="https://josephaugustine17.github.io/RedditCoin/docs/assets/submission_coin_counter.png" class="center">
  </p>
  Both comment and submission data was merged into single table
  <p align ="center">
  <img src="https://josephaugustine17.github.io/RedditCoin/docs/assets/total_coin_counte.png"  class="center" >
</p>

 ## Historical Crypto Data
 Data about specific crypto's was downloaded from yahoo finance. These crypto's include : Bitcoin, Ethereum,H3x, Vechain and include data such as opens,high,low,adjusted close,closes, and volume for each day. We chose these crypto's due to varying popularity. Bitcoin and Ethereum have high popularity, Vchain is medium popular, and H3x is almost unknown. 


# Data Exploration
With the missing data removed we are ready to perform exploratory data anaysis which was performed on our milestone report. We wanted to get an understanding of the data so we decided to use visualization techniques focusing on specific features like score, subreddit, and date.Using bar graphs we analyzed the score by looking at the frequency, this graph was unreadable so we used the log to make the graph readable. 

We discovered that many of have the submissions had no or very low score. 
 <img src="https://josephaugustine17.github.io/RedditCoin/docs/assets/submission_score_value.png"  class="center" >

 Likewise with comments
 
 <img src="https://josephaugustine17.github.io/RedditCoin/docs/assets/comments_score_value.png"  class="center" >

Also we discovered comments scores are negative are close to 0. 
  <img src="https://josephaugustine17.github.io/RedditCoin/docs/assets/comments_score_neg_value.png"  class="center" >

We performed various analysis on the date grouping by day, month, and year and seeing how post frequency varies using bar graphs. Finally we looked at the different subreddits utilizing key work searches to see if there even are crypto subreddits to do our project on. We discovered the most popular subreddits using graphs and decided which ones to focus on.

Discovered most popular cryptos which are as followed:

 <img src="https://josephaugustine17.github.io/RedditCoin/docs/assets/Most_popular.png"  class="center" >

Discovered least popular cryptos which are as followed: 
<img src="https://josephaugustine17.github.io/RedditCoin/docs/assets/least_popular.png"  class="center" >

Multiple crypto symbols have similar names as every day words. 
<img src="https://josephaugustine17.github.io/RedditCoin/docs/assets/common_words_filtered.png"  class="center">

Additionally discoverd the largest cyrpto subreddicts based on submission data: 
<img src="https://josephaugustine17.github.io/RedditCoin/docs/assets/largest_crypto_subreddit_sub.png"  class="center">

Discovered the largest cyrpto subreddicts based on comment data: 
<img src="https://josephaugustine17.github.io/RedditCoin/docs/assets/largest_crypto_subreddit_com.png"  class="center">

Discovered the most popular cyrpto's based on reddit score: 
<img src="https://josephaugustine17.github.io/RedditCoin/docs/assets/popular_crypto_subreddit.png"  class="center">

Discovered the most hated cyrpto's based on reddit score : 
<img src="https://josephaugustine17.github.io/RedditCoin/docs/assets/hated_crypto_subreddit.png"  class="center">


We are now ready to properly answer what crypto are most and least popular. Grouping by each crypto name and aggregating the score over the days we found the most popular and least popular which are THENODE and H3X. We exprected Bitcoin to be first and then realized that the symbol for THENODE is A which is used in many sentences. So we decided to use a list of common english stopping words combined with a list of words generated from looking at the data. We also removed coins that also purely referenced by either syymbol or name because it is an indication that it is just a commmon english word. For example Name:THENODE and SYMBOL:A is purely referenced by the symbol only. This cleaning method gives us a clearer idea of what the most popular coins are. The coins we found were Bitcoin and Ehtereum which were expected. The most surprising one was PanCakeSwap.


Hypothesis: After reviewing our data we believe that reddit will be predictive in terms of the increase of price of crypto's. This means reddit karma for a certain crypto will increase before a crypto's price begins to rise/drop. 

# Reddit Score vs Bitcoin Score
The reddit score for each crypto is the karma it gained in a day. The crypto score is the closed value of the crypto for that same day. The following graph compares the two values for 4 cryptos.Each graph is interactive where dragging will zoom and additonal buttons to help analysis on the top right. If buttons aren't there scroll to the right.
- ## Bitcoin

  <iframe src="https://josephaugustine17.github.io/RedditCoin/docs/assets/bitcoin.html" style="width: 1500px; height: 800px; border: 0px"></iframe>
 Through inspection of the graph it appears as thought reddit is mainly reactive. This means most of the time when there is a spike in price of the coin reddit karma  increases after the price already increased. However in Octoboer 2020 a huge spike of karma is seen and then soon after there is an increase in the price of bitcoin. This can potentially be seen as predictive however most of the time this is reactive. 
   
- ## Vechain
  <iframe src="https://josephaugustine17.github.io/RedditCoin/docs/assets/vechain.html" style="width: 1500px; height: 800px; border: 0px"></iframe>
   Through inspection of the graph it appears as thought reddit is predictive. Looking athe spikes in July 2020 to around Feb 2021 we see that increases in prices occur after there is high karma with that coin on reddit. Additionally when reddit karma dies down the price of the coin steadily decreases.
  
- ## Ethereum
<iframe src="https://josephaugustine17.github.io/RedditCoin/docs/assets/ethereum.html" style="width: 1500px; height: 800px; border: 0px"></iframe>
   Through inspection of the graph it appears as thought reddit is predictive. We see early spikes in 2019 as well as spikes closer to when the price increaseses. For example in June 2020 reddict activity spikes and then soon later Ethereum begins to climb in price. This pattern continue sin January 2021 and April 2021 where the spikes in activity are followed by increases in price. 
   
- ## H3x
<iframe src="https://josephaugustine17.github.io/RedditCoin/docs/assets/h3x.html" style="width: 1500px; height: 800px; border: 0px"></iframe>
 Through inspection of the graph it appears as thought reddit is reactive. The price of the current begins to drop right before July 2020 however as the price of the crypto begins to drop we see that reddit score begins to drop as well. This however occurs after which is why we believe it to be reactive. 


# Reddit score vs Trade Volume
The reddit score for each crypto is the amount of karma it gained in a day. The trade volume is amount of transactions made with that crypto that same day. The following graph compares both side by side. Each graph is interactive where dragging will zoom and additonal buttons to help analysis on the top right. If buttons aren't there scroll to the right. 

- ##  Bitcoin
  <iframe src="https://josephaugustine17.github.io/RedditCoin/docs/assets/bitcoin_volume.html" style="width: 1500px; height: 800px; border: 0px"></iframe>
  Through inspection of the graph we see the two factors are highly correlated. When we look at spikes of reddit score we see that the amount of Bitcoin being  bought soon after karma rises significantly. This is seen in most of the spikes however as of recent the correlation has been a bit off as high reddit score in around June did not result in increase int bitcoin transaction. 
  
- ## VeChain
  <iframe src="https://josephaugustine17.github.io/RedditCoin/docs/assets/vechain_volume.html" style="width: 1500px; height: 800px; border: 0px"></iframe>
   Through inspection of the graph we see the two factors are highly correlated. When we look at spikes of reddit score we see that the amount of VeChain being  bought soon after karma rises significantly. This is found significantyl around Feb 2021 where there is a huge spike of VeChain reddit score and then soon later amount of Vechain bought begins to rise steadily and then spikes 2 months after. 
   
- ## Ethereum
<iframe src="https://josephaugustine17.github.io/RedditCoin/docs/assets/ethereum_volume.html" style="width: 1500px; height: 800px; border: 0px"></iframe>
   Through inspection of the graph we see the two factors are highly correlated. When we look at spikes of reddit score we see that the amount of Ethereum being  bought soon after karma rises significantly. We see spikes in reddit karma early 2019 was followed by increase of transaction. This occurs similarly in late 2019 and early 2021. 
- ## H3x
 <iframe src="https://josephaugustine17.github.io/RedditCoin/docs/assets/h3x_volume.html" style="width: 1500px; height: 800px; border: 0px"></iframe
    Through inspection of the graph we see the two factors are highly correlated. Even though this is fairly unknown crypto we see that reddit still picks up on the transaction trends. Specifically look at around Jun 2020 reddit score drops substantially which followed the decrease in the number of transactions. When the karma went back up the volume of transactions also went up. 

## Communication 

The data tells us  that reddit score is highly correlated with the volume traded of cryptos from high to low popularity. Activities on reddit also correlated with larges movements in price of a coin. The most popular crypto mentioned in reddit is Bitcoin, and the least popular crypto is H3x, and DragonChain. It appears that increased activity in reddit maps to increase in price in the long run(1-2 years). This is true through the inspection of cryptos across different popularity and their karma across reddit and volume bought /price each day.


