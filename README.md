

#  Customer Lifetime Value (CLV) Prediction using BigQuery + TensorFlow (Vertex AI)

## Overview of the project

This project was built as part of my **Google Cloud Career Launchpad training**, where I worked on a real-world machine learning problem:
**predicting how much revenue each customer is likely to generate in the next 3 months.**

Instead of guessing or using simple averages, I tried to use customer behavior data to make smarter predictions — things like how recently they purchased, how often they buy, and how much they usually spend.

The idea is simple :
*If we can predict customer value, businesses can make better decisions about marketing, retention, and growth.*

---

## The problem I tried to solve

In most businesses, not all customers are equal.

Some customers:

* Buy frequently
* Spend more money
* Stay active for longer

Others:

* Buy once and disappear
* Spend very little
* Don’t return

The challenge was:

> Can we predict the future value of a customer using only their past behavior?

---

## My approach

I treated this as a **regression problem**, where the model predicts a numeric value (future spend).

To do that, I focused on classic customer behavior signals (RFM concept):

* **Recency** → How long since the last purchase
* **Frequency** → How often they purchase
* **Monetary value** → How much they spend
* **Customer age** → How long they’ve been active

Along with a few derived features like average order size and revenue per purchase.

---

## How the system works (high level)

Here’s the flow I followed:


<img width="5003" height="525" alt="mermaid-diagram (1)" src="https://github.com/user-attachments/assets/2b8690dc-1eb7-4589-a725-44199a83d18b" />



---

## What I did with the data

The raw dataset had over **500K+ transactions**, so I cleaned and reshaped it using BigQuery.

Here’s what I focused on:

* Removed records without customer IDs
* Filtered out invalid transactions (negative or zero values)
* Aggregated transactions at customer level
* Converted raw purchases into meaningful behavioral features
* Built a final ML-ready dataset for training

---

## Model I used

I built a **simple but effective neural network using TensorFlow (Keras)**.

### Model structure:

* Input: Customer behavioral features
* Dense layer (256 neurons, ReLU activation)
* Dropout layer (to reduce overfitting)
* Output layer: single value (predicted CLV)

### Training setup:

* Loss function: MAE (works better with outliers)
* Optimizer: Adam
* Train/validation/test split from BigQuery dataset

---

## What I observed

During exploration and training, a few interesting things stood out:

* A small group of customers contributed most of the revenue
* Spending patterns were heavily skewed (a few extreme outliers)
* Frequency and recency were strong indicators of future value
* Simple models already give a decent baseline, but ML improves stability

---

## Results (high level)

* The ML model performed better than a simple baseline approach
* Error reduced significantly compared to rule-based prediction
* Model captured customer differences more effectively than averages

(Exact metrics depend on tuning and preprocessing choices like outlier handling.)

---

## Challenges I faced

This wasn’t a perfect dataset, and that was actually the interesting part.

Some challenges:

* Very high-value outliers distorted predictions
* Many customers had only 1–2 purchases (sparse behavior)
* Distribution of spending was heavily imbalanced

To handle this, I explored:

* Using MAE instead of MSE
* Thinking about log transformations
* Considering segmentation-based modeling

---

## What I learned from this project

This project helped me understand:

* How real business problems are translated into ML problems
* Why feature engineering matters more than model complexity
* How messy real customer data actually is
* How cloud tools (BigQuery + Vertex AI) fit into real ML pipelines

Most importantly, I learned that:

> Good ML is not just about accuracy — it’s about making business decisions easier.

---

## My future work :

* Adding log transformation for skewed revenue data
* Trying XGBoost / LightGBM models for comparison
* Building customer segments before prediction
* Deploying the model using Vertex AI endpoints
* Turning this into a real-time prediction pipeline

---

## Tech Stack

* Google BigQuery
* Google Cloud Storage
* TensorFlow / Keras
* Vertex AI
* Python (Pandas, NumPy, Matplotlib)

---

