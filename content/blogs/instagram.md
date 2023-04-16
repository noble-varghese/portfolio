---
title: Unlocking the Secrets of Instagram's Suggestion Algorithm!
type: page
# description: Click on me to see the content.
topic: career
author: Noble Varghese
---

Ever wondered how you get suggestions on the explore page in instagram.
Let's say we like traveling and science fiction then we are most likely to be presented with posts related to traveling, content creation & science fiction on the explore page. How does instagram manage to achieve this to increase the user engagement in the explore page. Let's take a look.


👀 What is the explore page ?
The Instagram Explore page is a collection of public photos, videos, Reels and Stories to help each individual Instagram user discover posts, accounts, hashtags or products from other accounts. 

⚙️ Working of the explore page:
	Any information retrieval system contains a two step process - candidate generation and candidate selection.

⦿ Candidate Generation:
	This is the process of selecting all the accounts that a user might be interested in based on the user's explicit or implicit interests. Say if the user is interested in an account that posts contents on traveling, the algorithm finds similar accounts that post contents similar to travelling. This is based on two classic ML principles - Embedding based similarity & Co-occurrence based similarity.
	- Embedding based similarity:
		Finding similar accounts based on the user engagement data. Using this instagram builds an account embeddings and find the topically similar accounts.
	- Co-occurrence based similarity: 
		Similarity is based on the idea of frequent pattern mining. Based on the user-media interaction, a user list of co-occurred media is generated. Then a co-occurrence frequency of those pairs are identified, sorted and top N media pairs are shown as recommendations.

⦿ Candidate Selection:
	The algorithm ranks a given post based on many factors of engagement and aversion which act as labels in our ranking pipeline. These include positive engagement factors such as like, comment, and save; and negative factors such as not interested and see fewer posts like these. Apart from these there are a list of features that instagram uses to rank the content.


🚀 Finally in order to ensure that the recommendations in explore page feel similar to posts in Home Feed they prioritize the accounts that are similar to accounts a user encounters in Home.

![](https://noble-varghese.github.io/portfolio/images/instagram.jpeg)

