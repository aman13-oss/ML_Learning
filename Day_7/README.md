# DAY 7 — Problems in Machine Learning

## 1. Data Collection

**Definition:**  
Data Collection is the process of gathering **relevant, sufficient and reliable data** needed for ML training.

### Example

For customer churn prediction:

```text
Customer usage
Purchase history
Complaints
Subscription
```

must be collected.

---

# 2. Insufficient Data

**Definition:**  
Insufficient Data means there is **not enough training data** for the model to learn reliable patterns.

### Example

Trying to train a house-price model using only:

```text
20 houses
```

may not represent the actual market well.

---

# 3. Insufficient Labelled Data

**Definition:**  
Insufficient Labelled Data means there are not enough examples with **correct Output/Labels**, making supervised learning difficult.

### Example

For disease classification:

```text
10,000 medical images
```

but only:

```text
100 images → labeled
9900 → unlabeled
```

---

# 4. Poor Quality Data

**Definition:**  
Poor Quality Data contains problems such as **missing, incorrect, duplicate, inconsistent or noisy values**, which can negatively affect model learning.

### Example

```text
Age = -50
Salary = "ABC"
Gender = missing
```

Such data needs to be handled.

---

# 5. Irrelevant Features

**Definition:**  
Irrelevant Features are features that **do not provide useful information for the prediction task**.

### Example

House price prediction:

```text
Area → Relevant
Location → Relevant
Bedrooms → Relevant

Favorite Color → Irrelevant
```
