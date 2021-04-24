# Finding frequent itemsets
Finding restaurants tuples that appears in review data from Yelp.com

### Sample data
Sample data is a subset of business.json and review.json data from the Yelp dataset (Done by Preprocess.py).
The raw data is in csv format as shown below:

![image](https://user-images.githubusercontent.com/25105806/115973383-77e95080-a509-11eb-91ae-9952bef1a1d7.png)



### 1. SON algorithm/Market-Basket model
SON algorithm is used to build Market-Basket model. There are two cases related to MB model:
  1. Frequent businesses: combinations of frequent businesses (as singletons, pairs, triples, etc.) that are qualified as frequent given a support threshold
```
user1: [business11, business12, business13, ...]
user2: [business21, business22, business23, ...]
user3: [business31, business32, business33, ...]
```
    
  3. Frequent users: combinations of frequent users (as singletons, pairs, triples, etc.) that are qualified as frequent given a support threshold.
```
business1: [user11, user12, user13, ...]
business2: [user21, user22, user23, ...]
business3: [user31, user32, user33, ...]
```
The market-basket model is built using SON algorithm with A-Priori algorithm and test using relatively small dataset.

### 2. Market-Basket model on frequent businesses with large dataset
The result is similiar to previous Market-Basket model except that we're working with large dataset this time. So this time I improved the implementation and speeded up the runtime. SON algorithm and A-Priori is also applied here.
Preprocess.py takes charge of building market-basket model from the large raw data extracted from Yelp.com in json format.

### 3. FP-growth algorithm
FP-Growth tree algorithm did the same work as task2, this is to compare the runtime and result difference. 

