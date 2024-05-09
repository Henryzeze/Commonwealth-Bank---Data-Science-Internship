# Commonwealth-Bank---Data-Science-Internship

![](cover.jpg)

## Overview

As a Data Analyst for Commonwealth Bank, 1 embarked on a long-term vision alongside one of their trusted partner, InsightSpark, a data science specialist. In this project, we set out to leverage the vast volumes of CBA's transactional data, open-source data, and advanced data science capabilities. Our goal was to construct a platform designed to provide invaluable insights for businesses, governments, and investors across Australia.

In this ambitious endeavor, i and the data engineering team shoulders a significant responsibility. Tasked with constructing data engineering pipelines, conducting analysis on extensive datasets, and deploying algorithms at scale, the success of the project hinged greatly on our collective efforts.

## Task 1

I was given a data set named “supermarket_transactions.csv.” This data set contained three years of transactional data collected from supermarkets across Australia. 

InsightSpark wanted to access the company's data to perform some analysis across Australian supermarkets. But Before this could happen, I needed to perform some analysis on the provided CSV data set (a sample of the database) to answer the following questions:

Across locations, how many apples were purchased in cash?
How much total cash was spent on these apples?
Across all payment methods, how much money was spent at the Bakershire store location by non-member customers?

My analysis was conducted in Microsoft Excel using pivot tables.

![](cover1.jpg)


## Task 2

I was provided with a data set named “mobile_customers.csv.” This contained information about customers who have signed up for the mobile app in the last three years.

I was tasked to anonymize this data to hide personal details while preserving any useful information for the data scientists at InsightSpark.

Anonymizing a data set can involve the following:
Removing columns that don’t provide helpful information for analysis (e.g., names or credit card numbers).
Masking any columns that can identify an individual (e.g., passport numbers or mobile numbers).
Categorizing personal figures (e.g., age and income) into a bracket rather than a specific number.

First, I had to research the different techniques for anonymizing the data set. Then, I edited the data set and created an anonymized data set as a CSV file. I decided to do this task using a Python script instead of Excel.

***Note*** python script and anonymize_data can be found in the files.

## Task 3

This task involved familiarizing myself with the CommBank Account and drafting a proposal informing my team on how web scraping the data available from this account will help provide valuable insights into customer interactions, market perceptions, and any other relevant trends to the banking sector. I also highlighted the following potential use cases for Insightspark:

**Customer Sentiment Analysis:**

- By analyzing tweets mentioning @CommBank, Insightspark can perform sentiment analysis to gauge public sentiment towards the bank.
- Insights derived from sentiment analysis can help CBA identify areas for improvement in customer satisfaction and address potential pain points.

**Product Feedback and Market Insights:**

- Analyzing user mentions and replies can provide valuable feedback on CBA products, services, and customer experiences.
- Monitoring discussions around specific banking products or services can offer insights into market trends, customer preferences, and competitors' offerings.

**Brand Reputation Management:**

- Tracking mentions, retweets, and engagement metrics can help assess the bank's brand perception and reputation on Twitter.
- Identifying and addressing negative sentiments or potential PR crises in real-time can mitigate reputational risks and maintain a positive brand image.

**Customer Engagement and Outreach:**

- Analyzing user interactions and engagement patterns can inform personalized marketing strategies and customer engagement initiatives.
- Identifying influential users and brand advocates can facilitate targeted outreach efforts and foster community engagement.

## Task 4

I was tasked to propose a database structure that stores tweets from the CommBank Twitter account, as well as user replies, user quote retweets, and direct mentions.

**My Database Structure Proposal for Storing Twitter Data**

**List of Tables:**

- Tweets
- Users
- Replies
- Quote Retweets
- Direct Mentions

**Items to Include in Each Table:**

Tweets:

- tweet_id (Primary key): Unique identifier for each tweet.
- user_id: ID of the user who posted the tweet.
- tweet_text: Content of the tweet.
- tweet_date: Date and time when the tweet was posted.

Users:

- user_id (Primary key): Unique identifier for each user.
- username: Twitter username of the user.
- name: Full name of the user.
- bio: User's bio description.
- location: User's location.
- follower_count: Number of followers.
- following_count: Number of accounts the user is following.

Replies:

- reply_id (Primary key): Unique identifier for each reply.
- tweet_id: ID of the tweet being replied to.
- user_id: ID of the user who posted the reply.
- reply_text: Content of the reply.
- reply_date: Date and time when the reply was posted.

Quote Retweets:

- quote_retweet_id (Primary key): Unique identifier for each quote retweet.
- tweet_id: ID of the tweet being quoted.
- user_id: ID of the user who posted the quote retweet.
- quote_retweet_text: Content of the quote retweet.
- quote_retweet_date: Date and time when the quote retweet was posted.

Direct Mentions:

- mention_id (Primary key): Unique identifier for each direct mention.
- tweet_id: ID of the tweet where the mention occurred.
- user_id: ID of the user who was mentioned.
- mention_text: Content of the mention.
- mention_date: Date and time when the mention was made.

**Table Relationships:**

- Each tweet in the Tweets table is linked to the corresponding user in the Users table through the user_id field.
- Replies are linked to the original tweet in the Tweets table through the tweet_id field.
- Quote retweets are linked to the original tweet in the Tweets table through the tweet_id field.
- Direct mentions are linked to the original tweet in the Tweets table through the tweet_id field.





