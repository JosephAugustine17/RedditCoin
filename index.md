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

1. ## Reddit Data 
Submission data gathered from reddit

<img src="https://josephaugustine17.github.io/RedditCoin/docs/assets/submission_pre_clean.png" >
 
Comment data gathered from reddit 

<img src="https://josephaugustine17.github.io/RedditCoin/docs/assets/comment_pre_clean.png" >

Reddit submission data cleaned such that each column between "score", "title", "subreddit", "created_utc" would require values.
Reddit comment data cleaned such that each column between "score", "body", "subreddit", "created_utc" would require values.
Columns with empty values were dropped for both. 

<img src="https://josephaugustine17.github.io/RedditCoin/docs/assets/cleaned_data.png">

Additionally both fields filtered out dates which did not contain numerical values. 
 <img src="https://josephaugustine17.github.io/RedditCoin/docs/assets/Date_filter.png" >

Reddit submission data was filtered to include subreddits with the names "btc", "BitcoinBeginners", "BitcoinMarkets", "BitcoinBeginners", "Bitcoin", "ethereum", "Vechain", "Ripple", "LitecoinMarkets", "dogecoin", "Monero", "Stellar" and any subreddit containing "crypto within the title. 
<img src="https://josephaugustine17.github.io/RedditCoin/docs/assets/crypto_subreddits.png">

- ## Crypto Symbol/Name Data 
Data about names and symbols of crypto's were gathered first from website CoinMarketCap. This was data was scraped from the web page and then parsed as needed. Symbols were cleaned as well removing symbols which were common english words. 

<img src="https://josephaugustine17.github.io/RedditCoin/docs/assets/common_words_filtered.png" >


Each crypto was placed in a dataframe which maps a crypto to the number mentions made on a particular day initialized as 0.
 
 <img src="https://josephaugustine17.github.io/RedditCoin/docs/assets/coin_counter.png" >
 
 Looped through each related submission and look for mention of a specific coin. Similarly done for commentsas well 
  
  <img src="https://josephaugustine17.github.io/RedditCoin/docs/assets/submission_coin_counter.png">
  
  Both comment and submission data was merged into single table
  
  <img src="https://josephaugustine17.github.io/RedditCoin/docs/assets/total_coin_counte.png" >

- ## Historical Crypto Data
- Data about specific crypto's was downloaded from yahoo finance. These crypto's include : Bitcoin, Ethereum,H3x, Vechani and include data such as opens,high,low,adjusted close,closes, and volume for each day. 


# Data Exploration
Discovered most popular cryptos which are as followed: 
 <img src="https://josephaugustine17.github.io/RedditCoin/docs/assets/Most_popular.png" >

Discovered least popular cryptos which are as followed: 
<img src="https://josephaugustine17.github.io/RedditCoin/docs/assets/least_popular.png" >

Multiple crypto symbols have similar names as every day words. 
<img src="https://josephaugustine17.github.io/RedditCoin/docs/assets/common_words.png">

Hypothesis: After reviewing our data we believe that reddit will be predictive in terms of the increase of price of crypto's. This means reddit activity for a certain crypto will increase before a crypto's price begins to rise/drop. 

# Reddit Score vs BitCoin Score
The reddit score for each crypto is the amount of times it was mentioned in a day. The crypto score is the closed value of the crypto for that same day. The following graph compares the two values for 4 cryptos. 
- ##  Bitcoin
  <iframe src="https://josephaugustine17.github.io/RedditCoin/docs/assets/bitcoin.html" style="width: 2200px; height: 800px; border: 0px"></iframe>
- ## Vechain
  <iframe src="https://josephaugustine17.github.io/RedditCoin/docs/assets/vechain.html" style="width: 2200px; height: 800px; border: 0px"></iframe>
- ## Ethereum
<iframe src="https://josephaugustine17.github.io/RedditCoin/docs/assets/ethereum.html" style="width: 2200px; height: 800px; border: 0px"></iframe>
- ## H3x
<iframe src="https://josephaugustine17.github.io/RedditCoin/docs/assets/h3x.html" style="width: 2200px; height: 800px; border: 0px"></iframe>


# Reddit score vs Trade Volume
The reddit score for each crypto is the amount of times it was mentioned in a day. The trade volume is amount of transactions made with that crypto that same day. The following graph compares both side by side. 
- ##  Bitcoin
  <iframe src="https://josephaugustine17.github.io/RedditCoin/docs/assets/bitcoin_volume.html" style="width: 2200px; height: 800px; border: 0px"></iframe>
- ## Vechain
  <iframe src="https://josephaugustine17.github.io/RedditCoin/docs/assets/vechain_volume.html" style="width: 2200px; height: 800px; border: 0px"></iframe>
- ## Ethereum
<iframe src="https://josephaugustine17.github.io/RedditCoin/docs/assets/ethereum_volume.html" style="width: 2200px; height: 800px; border: 0px"></iframe>
- ## H3x
- <iframe src="https://josephaugustine17.github.io/RedditCoin/docs/assets/h3x_volume.html" style="width: 2200px; height: 800px; border: 0px"></iframe>

## Interpretation 



## Communication 

Clearly describe what you learned and how others can use 
what is the story the data is telling 
what is th evidence its true and what are the limitations 
relate back to the goal 

  
```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![![image](https://user-images.githubusercontent.com/50184583/144765925-438d42c5-1b65-432e-ba42-305da82beb8e.png)
]()
](src)
```

For more details see [Basic writing and formatting syntax](https://docs.github.com/en/github/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax).

<p>test <p>
### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/JosephAugustine17/RedditCoin/settings/pages). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://docs.github.com/categories/github-pages-basics/) or [contact support](https://support.github.com/contact) and we’ll help you sort it out.
