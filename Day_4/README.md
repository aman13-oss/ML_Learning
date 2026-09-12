# DAY 4 — Instance-Based vs Model-Based Learning

## 1. Instance-Based Learning

**Definition:**  
Instance-Based Learning stores or remembers training examples and makes predictions for new data by finding **similarity with previously observed examples**.

### Example — KNN

Suppose we want to classify a new customer.

The model looks for:

```text
Which existing customers are most similar?
```

If most nearby customers are:

```text
Premium
Premium
Premium
Regular
```

The new customer may be classified as:

```text
Premium
```

The model relies heavily on the stored examples.

---

# 2. Model-Based Learning

**Definition:**  
Model-Based Learning learns a **generalized pattern or mathematical relationship** from training data and uses that learned model to make predictions on new data.

### Example — Linear Regression

Suppose:

```text
House Size → Price
```

The model learns a relationship between these variables.

After learning:

```text
New House Size
      ↓
Learned Model
      ↓
Predicted Price
```

It does not need to compare the new house with every training example in the same way KNN does.

---

# 3. Main Difference

```text
Instance-Based
Data → Store examples → Compare similarity → Prediction

Model-Based
Data → Learn pattern/model → Prediction
```

### Easy trick

**Instance-Based = Remember examples**

**Model-Based = Learn rules/pattern**
