# RetailRecommendationSystem_Association-Rule-Mining


Market Basket Analysis - Items that are frequently bought together
Apriori Algorithm :
Apriori is an algorithm for frequent item set mining and association rule learning. It proceeds by identifying the frequent individual items in the data and extending them to larger and larger item sets as long as those item sets appear sufficiently often in the data. The frequent item sets determined by Apriori can be used to determine association rules which highlight general trends in the data.

Metrics :
There are three major components of Apriori algorithm:

1) Support
2) Confidence
3) Lift

Suppose we have a record of 1000 customer transactions, and we want to find the Support, Confidence, and Lift for two items e.g. milk and bread. Out of one thousand transactions, 100 contain bread while 150 contain a milk. Out of 150 transactions where a milk is purchased, 50 transactions contain bread as well. Using this data, we want to find the support, confidence, and lift.

Support :
Support refers to the default popularity of an item and can be calculated by finding number of transactions containing a particular item divided by total number of transactions.

For instance if out of 1000 transactions, 100 transactions contain bread then the support for item bread can be calculated as:

Support(Bread) = (Transactions containing Bread)/(Total Transactions)

Support(Bread) = 100/1000
= 10%

Confidence :
Confidence refers to the likelihood that an item B is also bought if item A is bought. It can be calculated by finding the number of transactions where A and B are bought together, divided by total number of transactions where A is bought.

Coming back to our problem, we had 50 transactions where Milk and Bread were bought together. While in 150 transactions, milk is bought. Then we can find likelihood of buying bread when milk is bought can be represented as confidence of Milk -> Bread

Confidence(Milk → Bread) = 50/150
= 33.3%

Lift :
Lift(A -> B) refers to the increase in the ratio of sale of B when A is sold. Lift(A –> B) can be calculated by dividing Confidence(A -> B) divided by Support(B).

Coming back to our Milk and Bread problem, the Lift(Milk -> Bread) can be calculated as:

Lift(Milk → Bread) = (Confidence (Milk → Bread))/(Support (Bread))

Lift(Milk → Bread) = 33.3/10
= 3.33%

Lift basically tells us that the likelihood of buying Milk and Bread together is 3.33 times more than the likelihood of just buying the bread. A Lift of 1 means there is no association between products A and B. Lift of greater than 1 means products A and B are more likely to be bought together. Finally, Lift of less than 1 refers to the case where two products are unlikely to be bought together.




- Performed market basket analysis and create association rules to recommend items that are commonly bought together

- Analyzed the transactional data for the retail store to provide insights on the items that are bought together frequently. This will help the retail store to plan its design and layout of the products to improve profits.

- I have used Apriori algorithm to calculate the association mining rules based on this package (http://rasbt.github.io/mlxtend/user_guide/frequent_patterns/association_rules/#example-1-generating-association-rules-from-frequent-itemsets)
