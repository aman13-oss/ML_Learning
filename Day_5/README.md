# DAY 5 — Machine Learning Development Life Cycle

## What is MLDLC / MLDC?

**Definition:**  
Machine Learning Development Life Cycle is a **systematic step-by-step process** used to build an ML solution, starting from defining the problem and collecting data to training, deploying, testing and optimizing the model.

---

# 1. Frame the Problem

**Definition:**  
Clearly define **what problem needs to be solved**, what needs to be predicted, and what the final objective is.

### Example

Instead of saying:

> "We want to use ML for loans."

Define:

> "We want to predict whether a customer will default on a loan."

Now the problem is clear.

---

# 2. Gathering Data

**Definition:**  
Collect **relevant and sufficient data** required to solve the problem.

### Example

For loan default prediction:

```text
Age
Income
Loan Amount
Credit History
Previous Defaults
Employment
```

---

# 3. Data Preprocessing

**Definition:**  
Data preprocessing converts **raw, messy data into a clean and usable form** for ML models.

It may involve:

- Missing values
- Duplicate records
- Incorrect values
- Data formatting
- Encoding
- Scaling

### Example

If:

```text
Age = NULL
```

we need to appropriately handle that missing value.

---

# 4. Exploratory Data Analysis — EDA

**Definition:**  
EDA is the process of analyzing data to understand its **distribution, patterns, relationships, trends and unusual observations** before building a model.

### Example

We may discover:

```text
Higher income
      ↓
Lower probability of default
```

This gives us useful understanding of the dataset.

---

# 5. Feature Engineering

**Definition:**  
Feature Engineering means creating **new useful features from existing data** to help the ML model learn better patterns.

### Example

Suppose we have:

```text
Date of Birth
```

We can create:

```text
Age
```

So:

```text
Date of Birth → Age
```

---

# 6. Feature Selection

**Definition:**  
Feature Selection means selecting the **most relevant existing features** for model training and removing irrelevant or unnecessary features.

### Example

For house price prediction:

Useful:

```text
Area
Location
Bedrooms
Age
```

Possibly irrelevant:

```text
Owner's favorite color
```

---

# 7. Model Training

**Definition:**  
Model Training is the process of giving training data to an ML algorithm so that it can **learn patterns/relationships from the data**.

### Example

```text
Training Data
      ↓
Linear Regression
      ↓
Learn relationship
```

---

# 8. Model Evaluation

**Definition:**  
Model Evaluation means measuring how well the trained model performs using **appropriate evaluation metrics and unseen/test data**.

### Example

For classification:

```text
Accuracy = 92%
```

We may compare this with another model:

```text
Decision Tree → 92%
Logistic Regression → 89%
```

---

# 9. Model Selection

**Definition:**  
Model Selection means choosing the **most suitable model** based on performance and other practical requirements.

Example:

```text
Model A → 85%
Model B → 91%
Model C → 88%
```

Model B may be selected if the evaluation setup shows it is the best fit.
