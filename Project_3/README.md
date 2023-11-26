# Problem Statement

M Corporation after Project 2 ends towards the customer. The old wants to help analyze the behavior of customers. Especially what customers are interested in this period By going back to the period of Covid-19 where people's behavior is modified Controlled and limited travel And many activities are canceled.

To find out What is the "Outdoor activity" that is the most talked about? The purpose of the customer is to bring the analyzed data to the market plan. Event plan To be consistent with the current interest

Conditions provided by the customer
1. Is an outdoor activity That can be held often Or go out to do activities every day
2. It is said in the www.reddit.com period since post-Covid-19
3. It is not redundant with activities that are already popular today.

Of the conditions above, the selected community is
- Community: running.
- Community: Camping & Hiking.

The information that will be pulled from the website will be scoped from the post-Covid period onwards, that is, from 2022 to the present.

![](img/reddit_top_commu.png)

# Datasets

Scraping data from the two subreddits:
1. [r/running](https://www.reddit.com/r/running/)
2. [r/Camping&Hiking](https://www.reddit.com/r/Camping&Hiking/)

to train models.

# EDA

After scraping the data and combining the same data, it will enter the cleaning process. Because the information obtained will have some title, Comment that has been deleted We will remove this information. After that, it will enter the process of eliminating words that are disturbing such as punctuations, delimiters, and stopwords, then lemmatized.

From the complete information, find 20 Unigram and 20 Bigram to see the words that are often used. And have enough to bring into models

![](img/uni_bi_gram.png)

# Modeling

1. Logistic Regression
2. KNN Classification
3. Random Forest
4. SVM

| Modeling | Vectorize | Accuracy | F1 Score |
|----------|-----------|----------|----------|
| Logistic Regression | CountVectorize | 0.996 | 0.975 |
| Logistic Regression | TF-IDF | 0.998 | 0.977 |
| KNN Classification | CountVectorize | 0.906 | 0.833 |
| KNN Classification | TF-IDF | 0.947 | 0.893 |
| Random Forest | CountVectorize | 0.996 | 0.979 |
| Random Forest | TF-IDF | 0.996 | 0.983 |


From the results of the model mentioned by relying on the accuracy (Accuracy) Model that will be imported to predict is
Random Forest.

This, even if viewed from other models, will find that the accuracy score is similar. But in predicting the accuracy of talking about the model that gives the highest score, it will reduce the risk of errors.
