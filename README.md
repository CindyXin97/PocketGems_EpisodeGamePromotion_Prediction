# PocketGems_EpisodeGamePromotion_Prediction
This Project is launched by a game company , and we predict the group go customers to launch the promotions and which group of customers are going to convert by themselves.
## Episode Analytics

### Backgrounds and Intro

The majority of our users never generate any revenue (i.e., ‘convert’, in marketing parlance). We want to offer a promotion to some of these ‘non-payers’, in hopes of generating incremental revenue. Unfortunately, it’s not easy to identify true non-payers because many payers don’t convert until several weeks after installing the game. If you simply set a cutoff date and offer sales to everyone who hasn’t yet converted, you might find that revenue actually falls. This can occur if large numbers of not-yet-converted future payers take advantage of the sale instead of paying full price. If you’re not lucky, you might fail to convert a sufficient number of true non-payers, while ‘cannibalizing’ future payers by providing more value than they actually require.

The goal of this assignment is to devise a scheme to maximize incremental revenue. We’ll actually specify the promotion to be offered, namely, a two-for-one sale. What we want you to do is to specify a target group and prescribe a test protocol that can be used to evaluate the results.

### Data

User data, including user ID and install date
Session history, including date and session number
Purchase history, including date and amount
Spending history, including date, currency, and amount
‘Spending’ takes place when a user exchanges game currency (usually ‘gems’) for something of perceived value, such as a new outfit. Game currency can be earned during gameplay, but the bulk of it is obtained by making cash purchases, which are recorded in the ‘iaps’ (in-app-purchases) table.


### Target Main Solving Problems:

1. Specify a target group of users. Justify your choice using the sample data.
2. Specify a test and evaluation protocol. How long should the test run? How will you know if you have successfully increased revenue?
3. Build a model in R or Python to help us identify users who are likely to convert on their own. This part can be done independently -- it’s not necessary to combine the output of this model with your other analyses. Please assume, however, that we would eventually do this.
Note: The promotion is a two-for-one offer. We will not be reducing prices. Instead, we will be providing twice as much value for the same price.

### Methods 

1.  I used clustering methods for all the users who have gotten the gems, as it will exclude some users are really new to the game. Then I got 2 Clusters.

2. By looking into these 2 clusters, and conducting T-test, these two groups have significant differences in purchasing behavior and Rev, then we believe that Group1 are more likely to purchase. Then I selected all the people in Group 1 who haven't had any purchasing behavior as Type 1.

3. By using a Business Model RFM model, we believe that users who have high recency and high frequencies are likely to convert by themselves. Then other users in type 1 are users who need promotions. 

4. Random Forest, Figure out the important features 

5. Design A/B Test 

