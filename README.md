# Decision Tree in Machine Learning – Key Concepts

## 1. Decision Tree
A supervised learning algorithm that splits data into branches based on feature values, forming a tree-like structure to make predictions.

- **Classification Tree** → predicts categorical values.  
- **Regression Tree** → predicts continuous values.

     ┌── Feature A? ──┐
     │               │
  Yes▼               ▼No


---

## 2. Entropy
A measure of **impurity or randomness** in the dataset.

**Formula:**
Entropy(S) = -Σ p_i * log₂(p_i)
where `p_i` = proportion of class *i*.

- **High entropy** → data is more mixed.  
- **Low entropy** → data is more pure.

---

## 3. Gini Impurity
Another measure of impurity used in CART (Classification and Regression Trees).

**Formula:**
Gini(S) = 1 - Σ (p_i)²
- **Gini = 0** → perfectly pure node.  
- Faster to compute than entropy.

---

## 4. Information Gain
The **reduction in impurity** after a split.

**Formula (using entropy):**
IG = Entropy(Parent) − Σ ( |Child_k| / |Parent| ) × Entropy(Child_k)
- Higher IG → better split.

---

## 5. Pre-Pruning (Early Stopping)
Stop growing the tree early to avoid overfitting.

**Methods:**
- Set maximum depth.  
- Minimum samples per split.  
- Minimum information gain threshold.

---

## 6. Post-Pruning
Grow the full tree first, then remove branches that have little impact.

**Methods:**
- Cost complexity pruning (**CART’s alpha pruning**).  
- Reduced error pruning.

---

## 📊 Summary Table

| Term               | Meaning                              | Goal                  |
|--------------------|--------------------------------------|-----------------------|
| **Entropy**        | Impurity measure (log-based)         | Find best split       |
| **Gini Impurity**  | Impurity measure (probability-based) | Find best split       |
| **Information Gain** | Reduction in impurity              | Choose split feature  |
| **Pre-Pruning**    | Stop early                           | Prevent overfitting   |
| **Post-Pruning**   | Prune after training                 | Reduce overfitting    |

---

## 🌳 Pruning Workflow
[Train full tree]
↓
[Evaluate branches]
↓
[Remove low-impact splits]
↓
[Smaller tree → Less overfitting]
