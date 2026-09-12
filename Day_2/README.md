# DAY 2 — Unsupervised, Semi-Supervised & Reinforcement Learning

## 1. Unsupervised Learning

**Definition:**  
Unsupervised Learning is a Machine Learning technique where the model receives **only Input data and no Output/Label during training**, and it tries to discover hidden patterns, structures or relationships within the data.

### Example

Suppose a shopping company has:

```text
Customer  Age  Spending
A         20      2000
B         22      2500
C         45     30000
D         50     35000
```

There is no label saying:

```text
Budget
Premium
```

The model can discover groups itself:

```text
Group 1 → Low spending customers
Group 2 → High spending customers
```

### Main techniques

```text
Unsupervised Learning
│
├── Clustering
├── Dimensionality Reduction
├── Anomaly Detection
└── Association Rule Learning
```

---

# 2. Clustering

**Definition:**  
Clustering is an **Unsupervised Learning** technique where the model uses **only Input data, without Output/Labels**, and groups similar data points into different clusters.

### Example

Customer data:

```text
Customer A → Low spending
Customer B → Low spending
Customer C → High spending
Customer D → High spending
```

Model may create:

```text
Cluster 1 → Budget Customers
Cluster 2 → Premium Customers
```

No one tells the model which customer belongs to which group.

---

# 3. Dimensionality Reduction

**Definition:**  
Dimensionality Reduction is a technique where the model uses **Input data without Output/Labels** to reduce the number of features/dimensions while preserving as much important information as possible.

### Why?

Suppose:

```text
Dataset = 1000 features
```

Working with so many features can make the model:

- slower
- more complex
- harder to visualize
- more prone to unnecessary information

We can reduce:

```text
1000 features → 50 important dimensions
```

### Example

A customer dataset contains:

```text
Age
Income
Spending
Location
Education
Occupation
...
100 features
```

Dimensionality reduction can represent the data using fewer dimensions while retaining important patterns.

---

# 4. Anomaly Detection

**Definition:**  
Anomaly Detection is an **Unsupervised Learning** technique where the model receives **Input data without Output/Labels** and identifies data points that are significantly different from normal patterns.

### Example

Normal transactions:

```text
₹500
₹1200
₹800
₹2000
₹1500
```

Suddenly:

```text
₹5,00,000
```

This transaction is very different from the normal pattern, so the model may identify it as an **anomaly**.

### Applications

- Fraud detection
- Network intrusion detection
- Machine failure detection
- Unusual user behavior

---

# 5. Association Rule Learning

**Definition:**  
Association Rule Learning is an **Unsupervised Learning** technique where the model uses **Input data without Output/Labels** to discover relationships or associations between different items.

### Example

A supermarket analyzes thousands of bills and discovers:

```text
People who buy Bread
        ↓
often buy Butter
```

This can be represented as:

```text
Bread → Butter
```

### Application

This is commonly used in:

**Market Basket Analysis**

For example, online stores can recommend:

> Customers who bought this product also bought these products.

---

# 6. Semi-Supervised Learning

**Definition:**  
Semi-Supervised Learning uses **both types of data**: a small amount of **Input + Output/Label** data and a large amount of **Input-only/unlabeled** data.

### Example

Suppose we have 10,000 images.

```text
500 images → labeled
9500 images → unlabeled
```

Instead of ignoring the 9500 images, the model uses both labeled and unlabeled data to improve learning.

### Why useful?

Labeling data can be expensive.

For example, labeling medical images may require an expert doctor.

---

# 7. Reinforcement Learning

**Definition:**  
Reinforcement Learning is a learning approach where the model does **not receive the correct Output/Label directly**. Instead, an **agent interacts with an environment**, takes actions and receives **rewards or penalties**, using them to learn better actions.

### Example

Chess-playing AI:

```text
AI takes action
      ↓
Environment responds
      ↓
Reward / Penalty
      ↓
AI learns
```

If AI wins:

```text
+10 Reward
```

If AI loses:

```text
Penalty
```

Over many games, it learns better strategies.
