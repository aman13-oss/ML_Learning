# DAY 1 — Introduction to Machine Learning & Types

## 1. What is Machine Learning?

**Definition:**  
Machine Learning is a field of AI where a computer system **learns patterns from data** and uses those learned patterns to make predictions or decisions without being explicitly programmed for every possible situation.

Traditional programming:

```text
Rules + Data → Output
```

Machine Learning:

```text
Data + Output → Learn Rules/Pattern
```

Then:

```text
New Data → Learned Model → Prediction
```

### Example

Suppose we want to detect spam emails.

Traditional programming requires us to manually define rules:

```text
If email contains "free money"
→ Spam
```

But spam can contain thousands of different patterns.

In ML, we provide many examples:

```text
Email              Label
--------------------------------
"Win free money"   Spam
"Meeting at 5 PM"  Not Spam
"Claim your prize" Spam
```

The model learns patterns from these examples and predicts whether a new email is spam.

---

# 2. Types of Machine Learning

Machine Learning can broadly be divided into:

```text
Machine Learning
│
├── Supervised Learning
├── Unsupervised Learning
├── Semi-Supervised Learning
└── Reinforcement Learning
```

---

# 3. Supervised Learning

**Definition:**  
Supervised Learning is a Machine Learning technique where the model is trained using **Input + correct Output/Label**, so that it can learn the relationship between them and predict the output for new input.

### Example

House price prediction:

```text
Input              Output
-------------------------
1000 sq.ft         ₹40 Lakh
1500 sq.ft         ₹60 Lakh
2000 sq.ft         ₹80 Lakh
```

The model learns:

```text
House Size → House Price
```

Then:

```text
1800 sq.ft → ₹72 Lakh
```

### Main Types

```text
Supervised Learning
│
├── Regression
└── Classification
```

---

# 4. Regression

**Definition:**  
Regression is a **Supervised Learning** technique where the model is trained using **Input + Output/Label**, and the output is a **continuous numerical value**.

### Example

Predicting house price:

```text
Input → House Size
Output → Price
```

Possible outputs:

```text
₹45.2 Lakh
₹57.8 Lakh
₹91.4 Lakh
```

These are continuous numerical values.

### Other examples

- Salary prediction
- Temperature prediction
- Sales prediction
- Stock price prediction

---

# 5. Classification

**Definition:**  
Classification is a **Supervised Learning** technique where the model is trained using **Input + Output/Label**, and the output belongs to a **predefined category/class**.

### Example

Email classification:

```text
Input → Email
Output → Spam / Not Spam
```

Another example:

```text
Medical data → Disease / No Disease
```

### Regression vs Classification

| Regression | Classification |
|---|---|
| Continuous numerical output | Categorical output |
| Predicts a value | Predicts a class |
| House price | Spam/Not Spam |
| Salary | Cat/Dog |
