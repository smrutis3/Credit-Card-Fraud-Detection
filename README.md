# Credit-Card-Fraud-Detection
Credit Card Fraud Detection System

**Overview**\
This project addresses the critical challenge of accurately detecting fraudulent credit card transactions using machine learning while minimizing false alarms that block legitimate customers. Traditional fraud detection methods often fail due to two major problems:

Missing real fraud (letting fraud slip through)\
False alarms (blocking genuine customers)

**Problem Statement**\
How can we accurately detect fraudulent credit card transactions using machine learning without blocking genuine customers?\
Fraudsters continuously develop new tactics to exploit credit card systems using stolen cards or fake purchases. Our solution focuses on detecting fraud based on sequential behavior and intent, rather than just transaction size.

**Inspiration**\
This project was inspired by JPMorgan Chase AI Research, particularly their work on:

Generating Synthetic Data in Finance: Highlighted the limits of synthetic datasets that miss real human behavior\
Behavior Trace Classification: Emphasized the need to detect fraud based on sequential behavior and intent, not just transaction size

**What We Built**\
A comprehensive fraud detection system using real behavioral features:

**Key Features**

Transaction Velocity: How often and how quickly someone is transacting\
Device/IP Changes: Detection of sudden changes in device or IP address\
Timing Patterns: Analysis of weekends, night-time transactions, and previous fraud patterns

**Machine Learning Models**\
We trained and compared multiple models:

Random Forest: Reliable, fast, and highly explainable\
XGBoost: High performance, great at spotting complex fraud patterns\
XGBoost + SMOTE: Balanced approach for imbalanced fraud datasets\
LSTM: Deep learning for sequential pattern recognition

**Methodology**
1. Data Preparation

Cleaned and transformed raw data\
Enabled behavioral pattern detection including:

Device changes\
Sudden spending spikes\
Unusual transaction times

2. Model Training

Trained multiple machine learning models\
Used metrics like Precision, Recall, and AUC for evaluation\
Visualized feature importance and model performance

3. Model Selection\
Random Forest emerged as the top performer:

Perfect Precision (1.0): No false alarms\
High Recall (0.98): Caught almost all fraud\
Best for real-time use: Fast and explainable

4. Real-World Testing\
Simulated real scenarios to validate model performance across different risk levels.

**Results**\
Dataset Distribution

66% Safe transactions: No fraud involved\
34% Fraudulent transactions: Needed to be caught\
Balanced dataset provides fair representation of both safe and fraudulent behaviors

Random Forest: Best overall performance with perfect precision and high recall\
XGBoost + SMOTE: Improved handling of imbalanced data\
LSTM: Poor performance due to dataset not being sequential in nature

**Real-World Testing**\
Scenario Testing Results

Scenario 1 (Low-risk): Everyday transaction → Safe (Risk: 0.02)\
Scenario 2 (Suspicious): Weekend + new device → Still safe but flagged (Risk: 0.03)\
Scenario 3 (High-risk): Weekend + device change + high spending → Flagged for review (Risk: 0.63)

**Why This Matters**\
This research bridges the gap between technical accuracy and real-world usability:

Prevents financial losses from fraud\
Reduces false flags on honest customers\
Simple enough to explain to business teams and integrate into production\
Scalable to real-world banking systems

**Future Scope**\
Real-Time Fraud Detection: Streaming detection using Kafka + PySpark\
Global Signal Sharing: Securely share fraud patterns across banks\
Geolocation Awareness: Flag odd behaviors (NY login + Dubai payment)\
Adaptive Learning: Auto-adjust thresholds using user drift patterns\
Explainability with LLMs: Generate human-readable reasons for fraud detection

**Why It Matters**\
Directly addresses JPMorgan AI research concerns:

Lack of behavioral signals in static datasets\
Scaling explainable models across global banks\
False positives that frustrate genuine users

"This isn't just a project — it's a foundation for real fraud defense."

**Technologies Used**

Python: Primary programming language\
Scikit-learn: Machine learning models (Random Forest)\
XGBoost: Gradient boosting framework\
TensorFlow/Keras: Deep learning (LSTM)\
Pandas: Data manipulation\
NumPy: Numerical computations\
Matplotlib/Seaborn: Data visualization\
SMOTE: Synthetic minority oversampling technique

**Acknowledgments**

JPMorgan Chase AI Research for inspiration and research direction\
Research papers on synthetic data generation in finance\
Domain-independent classification of behavior traces

**Contact**
For questions or collaborations, please reach out through GitHub issues or contact [smrutis3@illinois.edu].

**Building smarter fraud detection systems that protect both banks and customers.**
