## Step 1: Clean the Data

- Split the merged column “tunnel_parents label detailed-label”
- Remove duplicate --> 0 duplicates found
- Check and handle infinite/missing values ​​--> No infinite values found / Missing values handled
- Remove columns with only 1 unique value (local_orig, local_resp, missed_bytes, tunnel_parents)
- Meaning: Ensure “clean” data to avoid errors when training the model and avoid wasting memory.

## Step 1.1: Balancing the Dataset

- Begnin (469275) < Malicious (539473)

--> Fix the amount of data in the dataset (Make Beginn larger than Malicious)

--> Decided to convert the problem to Binary Classification (Benign vs Malicious).

- **Signification**: Avoid falling into the "multi-class" trap which is not feasible with the available data --> avoid getting low scores because F1-score of rare classes = 0.

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
- 3.1 Time-based features
- 3.2 Duration features
- 3.3 Byte & packet basic features (cast to numeric safely)
- 3.4 Ratio & per-second features (extremely powerful for scan detection)
- 3.5 Port features – destination port is the #1 discriminator in this dataset
- 3.6 Protocol & Service encoding (one-hot + target encoding hybrid)
- 3.7 Conn_state & History flags
- 3.8 IP-related features (source IP behavior)
- 3.9 Final feature list for modeling (drop non-numeric / redundant columns)

## Step 4: Model selection & evaluation

## Step 5: Training, Tuning, and Testing

## Step 6: Visualization

## Step 7: Report Writing

Objectives:

- Supervised Learning
- Feature Selection
- Optimization
- Model Evaluation- Hyperparameter Tuning
