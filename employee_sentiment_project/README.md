# Employee Sentiment Analysis – Final LLM Assessment

## 🔍 Project Overview
This project analyzes employee emails to evaluate workplace sentiment and engagement.  
The dataset (`test.csv`) contains unlabeled messages, and the goal is to generate insights using NLP and data analysis techniques.

## 🧠 Objectives
✔ Sentiment labeling (Positive / Negative / Neutral)  
✔ Exploratory Data Analysis (EDA)  
✔ Monthly sentiment scoring per employee  
✔ Employee ranking (Top 3 Positive & Top 3 Negative)  
✔ Flight-risk employee identification  
✔ Predictive modeling using Linear Regression

---

## 🗂 Methodology

### 1️⃣ Sentiment Labeling
- Text preprocessing applied on **body** column.
- Sentiment generated using **TextBlob** (or LLM where applicable).
- New column added: `Sentiment`

### 2️⃣ EDA
- Checked dataset structure, missing values, distributions
- Visualizations:
  - Sentiment distribution
  - Monthly trend of sentiment scores
  - Message frequency per employee

### 3️⃣ Monthly Sentiment Score
Formula applied:  
| Sentiment | Score |
|----------|--------|
| Positive | +1     |
| Neutral  | 0      |
| Negative | -1     |

`Score` aggregated per **Employee × Month**.

### 4️⃣ Employee Ranking
- Ranked employees monthly based on sentiment score.
- Output:
  - **Top 3 Positive employees**
  - **Top 3 Negative employees**

### 5️⃣ Flight Risk
Criteria:  
> Employee who sends **4 or more negative emails within a 30-day period**  
Flight-risk employees list generated and included in results.

### 6️⃣ Predictive Modeling
Model: **Linear Regression**  
Target: Monthly sentiment score  
Features used:
- Message count
- Average message word count
- Average message length
Model evaluation included train-test split and performance metrics.

---
