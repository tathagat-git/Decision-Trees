Decision Tree in Machine Learning – Key Concepts
1. Decision Tree
A supervised learning algorithm that splits data into branches based on feature values, forming a tree-like structure to make predictions.

Classification Tree → predicts categorical values.

Regression Tree → predicts continuous values.

2. Entropy
A measure of impurity or randomness in the dataset.

Formula:

𝐸
𝑛
𝑡
𝑟
𝑜
𝑝
𝑦
(
𝑆
)
=
−
∑
𝑖
=
1
𝑛
𝑝
𝑖
log
⁡
2
𝑝
𝑖
Entropy(S)=− 
i=1
∑
n
​
 p 
i
​
 log 
2
​
 p 
i
​
 
where 
𝑝
𝑖
p 
i
​
  = proportion of class 
𝑖
i.

High entropy → data is more mixed.

Low entropy → data is more pure.

3. Gini Impurity
Another measure of impurity used in CART (Classification and Regression Trees).

Formula:

𝐺
𝑖
𝑛
𝑖
(
𝑆
)
=
1
−
∑
𝑖
=
1
𝑛
𝑝
𝑖
2
Gini(S)=1− 
i=1
∑
n
​
 p 
i
2
​
 
Gini = 0 → perfectly pure node.

Faster to compute than entropy.

4. Information Gain
The reduction in impurity after a split.

Formula (using entropy):

𝐼
𝐺
=
𝐸
𝑛
𝑡
𝑟
𝑜
𝑝
𝑦
(
𝑃
𝑎
𝑟
𝑒
𝑛
𝑡
)
−
∑
𝑘
∣
𝐶
ℎ
𝑖
𝑙
𝑑
𝑘
∣
∣
𝑃
𝑎
𝑟
𝑒
𝑛
𝑡
∣
⋅
𝐸
𝑛
𝑡
𝑟
𝑜
𝑝
𝑦
(
𝐶
ℎ
𝑖
𝑙
𝑑
𝑘
)
IG=Entropy(Parent)− 
k
∑
​
  
∣Parent∣
∣Child 
k
​
 ∣
​
 ⋅Entropy(Child 
k
​
 )
Higher IG → better split.

5. Pre-Pruning (Early Stopping)
Stop growing the tree early to avoid overfitting.

Methods:

Set max depth.

Minimum samples per split.

Minimum information gain threshold.

6. Post-Pruning
Grow the full tree first, then remove branches that have little impact.

Methods:

Cost complexity pruning (CART’s alpha pruning).

Reduced error pruning.

✅ Summary Table:

Term	Meaning	Goal
Entropy	Impurity measure (log-based)	Find best split
Gini Impurity	Impurity measure (probability-based)	Find best split
Information Gain	Reduction in impurity	Choose split feature
Pre-Pruning	Stop early	Prevent overfitting
Post-Pruning	Prune after training	Reduce overfitting

