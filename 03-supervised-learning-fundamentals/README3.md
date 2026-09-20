# Day 03 — Supervised Learning Fundamentals

> My Machine Learning journey — learning one concept at a time.

## What I learned today

Today I studied the basic workflow of **supervised machine learning** and how we evaluate whether a model learns useful patterns.

### Topics covered

1. Data, features, and labels
2. The supervised learning workflow
3. Training data vs testing data
4. Error / loss
5. Generalization
6. Underfitting
7. Overfitting
8. Regression and classification

---

## 1. What is Supervised Learning?

**Supervised learning** is a type of machine learning where a model learns from **labeled data**.

The training data contains:

- **Features (X)** → the information given to the model
- **Label / Target (Y)** → the correct answer we want the model to learn to predict

The model learns a relationship between `X` and `Y`.

### Simple example

Suppose we want to predict house prices.

```text
Features (X)
├── Area
├── Number of bedrooms
└── Location

        ↓

   ML Model

        ↓

Target (Y)
House Price
```

---

## 2. Data, Features, and Labels

### Data

Data is the information collected for training or testing a machine learning model.

### Dataset

A **dataset** is a collection of data examples.

### Features

Features are the useful input information we give to the model.

Example:

```text
X = [1500, 2, 3]
```

This could represent:

- `1500` → area
- `2` → number of bedrooms
- `3` → another feature

### Label / Target

The label is the answer the model is trying to predict.

```text
X = input / features
Y = target / label
```

For a house-price problem:

```text
X → [1500, 2, 3]
Y → ₹80 lakh
```

---

## 3. Supervised Learning Workflow

The basic process is:

```text
Labeled Data
     ↓
Learning Algorithm
     ↓
Trained Model
     ↓
New / Unseen Data
     ↓
Prediction
```

The model does not simply memorize the training examples. The goal is to learn useful patterns that can also work on new data.

See:

**[`01-supervised-learning-pipeline.png`](./01-supervised-learning-pipeline.png)**

---

## 4. Regression and Classification

Supervised learning commonly includes:

### Regression

Regression predicts a **continuous numerical value**.

Examples:

- House price
- Temperature
- Salary
- Sales amount

```text
Input → Model →  ₹72.5 lakh
```

### Classification

Classification predicts a **class / category**.

Examples:

- Cat / Dog
- Spam / Not Spam
- Disease / No Disease
- Pass / Fail

```text
Input → Model → Cat
```

---

## 5. Training Data vs Testing Data

We normally divide our available dataset into separate parts.

For example:

```text
1000 examples
     │
     ├───────────────┐
     ↓               ↓
  800 examples    200 examples
   TRAINING         TESTING
```

### Training data

Training data is used by the learning algorithm to learn patterns and adjust the model.

### Testing data

Testing data is used after training to check how the model performs on data it has not seen during training.

See:

**[`02-train-test-split.png`](./02-train-test-split.png)**

> The exact train/test ratio can vary depending on the dataset and problem. The 80/20 split is only an example.

---

## 6. Error / Loss

A model's prediction may differ from the actual answer.

```text
Actual Answer
      ↓
    Compare
      ↑
Prediction
```

The difference between the actual answer and the prediction is related to the model's **error**.

A **loss function** gives us a numerical way to measure how wrong the model's predictions are.

During training, the learning algorithm uses the loss to adjust model parameters so that the model can improve.

---

## 7. Generalization

**Generalization** is the ability of a trained model to perform well on **unseen data**.

A model that generalizes well has learned useful patterns instead of simply memorizing its training examples.

### Good generalization

The model performs reasonably well on both training and unseen test data.

---

## 8. Overfitting

**Overfitting** happens when a model learns the training data too closely, including noise or unimportant details.

A common sign is:

```text
Training performance → very high
Testing performance  → much lower
```

The model may have memorized the training examples instead of learning patterns that generalize.

---

## 9. Underfitting

**Underfitting** happens when a model is too simple or has not learned enough from the data.

A common sign is:

```text
Training performance → low
Testing performance  → low
```

The model has not captured the important patterns in the data.

---

## 10. The Main Idea

```text
Underfitting
     ↓
Model learns too little

Good Generalization
     ↓
Model learns useful patterns

Overfitting
     ↓
Model learns training data too closely
```

See:

**[`03-underfitting-good-fit-overfitting.png`](./03-underfitting-good-fit-overfitting.png)**

---

## Key Takeaways

- Supervised learning uses **labeled data**.
- **Features (X)** are the inputs.
- **Labels / targets (Y)** are the answers we want to predict.
- The model learns patterns from training data.
- Testing data helps us evaluate performance on unseen examples.
- **Regression** predicts continuous numerical values.
- **Classification** predicts categories.
- **Loss** measures prediction error.
- **Generalization** means performing well on unseen data.
- **Overfitting** means learning the training data too closely.
- **Underfitting** means the model has not learned enough.

---

## My Learning Progress

- [x] Day 01 — Introduction to AI, ML and DL
- [x] Day 02 — Types of Machine Learning
- [x] Day 03 — Supervised Learning Fundamentals
- [ ] Day 04 — Next topic

---

## Questions I should explore next

- How does a model actually learn from the loss?
- What are model parameters?
- What is a linear regression model?
- How do we calculate regression loss?
- How do we measure classification accuracy?
