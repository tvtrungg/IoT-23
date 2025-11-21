## Step 1: Clean the Data

- Remove duplicates, infinite and missing values
- Handle missing values

## Step 1.1: Balancing the Dataset

- Begnin > Malicious

--> Fix the amount of data in the dataset (Make Beginn larger than Malicious)

## Step 2: Exploratory Data Analysis (EDA)

- Purpose: To understand the characteristics of IoT-23 (which is very different from CICIDS or NSL-KDD) and discover practical insights into IoT attack behavior.

- 2.1 Label normalization
- 2.2 Time-based analysis (ts)
- 2.3 Protocol & Service
- 2.4 Top destination ports are attacked
- 2.5 Distribution of numerical features
- 2.6 Correlation heatmap
- 2.7. Scatter plot `orig_bytes` vs `resp_bytes`

## Step 3: Feature Engineering

- Create new features
- 3.1 Time Processing
- 3.2 Creating Features from History
- 3.3 Flow-Based Features
- 3.4 Encoding Categorical Features
- 3.5 Handling Imbalance

## Step 4: Model selection & evaluation

## Step 5: Training, Tuning, and Testing

## Step 6: Visualization

## Step 7: Report Writing

Objectives:

- Supervised Learning
- Feature Selection
- Optimization
- Model Evaluation- Hyperparameter Tuning
