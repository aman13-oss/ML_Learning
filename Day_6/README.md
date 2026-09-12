# DAY 6 — Deployment, Testing & Optimization

## 1. Model Deployment

**Definition:**  
Model Deployment means making a trained ML model **available in a real-world system/application** so that it can generate predictions on new data.

### Example

A bank has trained a loan prediction model.

Deployment:

```text
Bank Website
      ↓
Customer enters details
      ↓
ML Model
      ↓
Loan Risk Prediction
```

---

# 2. Offline Learning / Deployment

**Definition:**  
In an offline learning setup, the model is trained using **historical/available data first**, and the trained model is then deployed to make predictions. New data is generally incorporated later through another training/update cycle.

### Example

```text
January–December Data
        ↓
Train Model
        ↓
Deploy
        ↓
Make Predictions
```

Later:

```text
New Data
   ↓
Retrain
   ↓
New Model
   ↓
Redeploy
```

---

# 3. Software Integration

**Definition:**  
Software Integration means connecting the ML model with an **existing software application, backend, API or system** so that the application can use the model's predictions.

### Example

```text
Mobile App
    ↓
Backend/API
    ↓
ML Model
    ↓
Prediction
    ↓
Mobile App
```

---

# 4. Testing

**Definition:**  
Testing checks whether the **ML model and complete ML application work correctly, reliably and as expected** after development/deployment.

### Example

Give different customer inputs:

```text
Customer A → Prediction
Customer B → Prediction
Customer C → Prediction
```

Check whether the system handles valid, invalid, edge-case and unexpected inputs correctly.

---

# 5. Optimization

**Definition:**  
Optimization means improving the ML system's **performance, efficiency, speed, resource usage or predictive quality**.

### Example

Suppose:

```text
Model prediction time = 5 seconds
```

After optimization:

```text
Prediction time = 0.5 seconds
```

The model/system becomes faster.
