# Finding frequent itemsets
Finding restaurants tuples that appears in review data from Yelp.com

#### Market-Basket model
There are two cases related to MB model:
  1. Frequent businesses: combinations of frequent businesses (as singletons, pairs, triples, etc.) that are qualified as frequent given a support threshold
```
user1: [business11, business12, business13, ...]
user2: [business21, business22, business23, ...]
user3: [business31, business32, business33, ...]
```
    
  3. Frequent users: combinations of frequent users (as singletons, pairs, triples, etc.) that are qualified as frequent given a support threshold.

task1 is to build market-basket model and test the implementation of SON algorithm using relatively small dataset.

task2 is to finding frequent itemsets in a large file, improving the implementation, speed up the runtime.

teak3 is the FP-Growth tree algorithm doing the same work as task2, this is to compare the runtime and result difference. 

preprocess takes charge of building market-basket model from the large raw data extracted from Yelp.com in json format.
