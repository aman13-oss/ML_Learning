# DAY 8 — Overfitting & Underfitting

## 1. Overfitting

**Definition:**  
Overfitting occurs when a model learns the training data **too closely**, including its noise and unnecessary patterns, resulting in poor performance on unseen data.

### Example

```text
Training Accuracy → 99%
Testing Accuracy  → 70%
```

The model has learned the training data too specifically.

### Easy Trick

**Overfitting = Model memorizes**

---

# 2. Underfitting

**Definition:**  
Underfitting occurs when a model is **too simple or insufficiently trained** to capture the important patterns in the data, resulting in poor performance even on training data.

### Example

```text
Training Accuracy → 65%
Testing Accuracy  → 63%
```

The model has failed to learn enough.

### Easy Trick

**Underfitting = Model has not learned enough**

---

# Overfitting vs Underfitting

| | Overfitting | Underfitting |
|---|---|---|
| Training performance | Very good | Poor |
| Test performance | Poor | Poor |
| Main problem | Learns too much/memorizes | Learns too little |
| Model | Too complex | Too simple |

Ideal model:

```text
Good Training Performance
          +
Good Testing Performance
          ↓
       Generalization
```
