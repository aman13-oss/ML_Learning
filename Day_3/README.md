# DAY 3 — Batch Learning & Online Learning

## 1. Batch Learning

**Definition:**  
Batch Learning trains the model using the **entire available training dataset at once**, and the model is updated after processing the complete dataset.

### Example

Dataset:

```text
1,00,000 records
```

Model:

```text
Entire dataset
      ↓
Training
      ↓
Model Update
```

If new data arrives later, normally the model needs to be retrained/updated using that new data.

---

# 2. Online Learning

**Definition:**  
Online Learning trains or updates the model using **data one-by-one or in small batches**, so the model can continuously learn from newly arriving data.

### Example

A stock/news recommendation system receives new data continuously:

```text
New Data
   ↓
Model Update
   ↓
New Data
   ↓
Model Update
   ↓
New Data
```

The model keeps adapting.

---

# 3. When to Use Online Learning?

Use Online Learning when:

### Continuous data

Example:

```text
Stock market data
Sensor data
User activity
```

### Huge datasets

When processing the complete dataset at once is difficult.

### Changing data

When patterns change over time.

Example:

Customer preferences may change every few months.

---

# 4. Learning Rate

**Definition:**  
Learning Rate determines **how much the model changes or updates its learned parameters when learning from new information**.

Think of it as the **speed of learning**.

### High learning rate

Model changes quickly.

```text
New information
      ↓
Large update
```

It can learn quickly but may become unstable.

### Low learning rate

```text
New information
      ↓
Small update
```

Learning is slower but generally more gradual.

---

# 5. Out-of-Core Learning

**Definition:**  
Out-of-Core Learning is used when the dataset is **too large to fit into the available RAM**, so the data is processed in smaller chunks.

### Example

Suppose:

```text
Dataset = 500 GB
RAM = 16 GB
```

We cannot load the entire dataset into memory.

Instead:

```text
500 GB
 ↓
Chunk 1 → Train
Chunk 2 → Train
Chunk 3 → Train
...
```

This allows ML to work with extremely large datasets.

---

# 6. Batch vs Online Learning

| Batch Learning | Online Learning |
|---|---|
| Processes complete dataset | Processes small chunks/data continuously |
| Model updates less frequently | Model updates frequently |
| Good for static data | Good for streaming data |
| Can require more memory | Usually memory efficient |
| Slow to adapt to changes | Quickly adapts to changes |
