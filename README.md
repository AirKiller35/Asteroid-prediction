# Asteroid Risk Prediction using Machine Learning

This project predicts whether an asteroid poses a potential risk to Earth using data from NASA’s Near-Earth Object (NEO) dataset.
It applies machine learning techniques to classify asteroids as hazardous or non-hazardous, based on their physical and orbital parameters.

## Project Overview

Asteroids are constantly monitored by NASA for their proximity, velocity, and size to assess potential danger to Earth.
In this project, a **Random Forrest classifier based model** was trained to predict asteroid risk using key features such as:

- Absolute magnitude (H)

- Estimated diameter (min & max)

- Relative velocity

- Miss distance

- Orbiting body

To handle data imbalance, the model uses **class weighting** and an **optimized decision threshold that maximizes the F1-score** for better recall on risky cases.

# Key Steps

- Data Preprocessing

- Handled missing values and converted string-based numerics.

- Scaled features using StandardScaler.

- Model Training

  _ Used LogisticRegression with class_weight='balanced' to counter data imbalance.

  _ Split data into training and testing sets for validation.

- Evaluation Metrics

  _ Confusion Matrix, Precision, Recall, F1-score

  _ ROC and Precision–Recall Curves

  _ Decision threshold optimization based on F1-score

# Results
**Accuracy**	~76%
**Precision (Hazardous)**	~0.48
**Recall (Hazardous)**	~0.36
**F1-score (Hazardous)**	~0.41
**Best Decision Threshold**	≈ 0.45

Adjusting the threshold improved the balance between identifying true hazardous asteroids and minimizing false alarms.

# Technologies Used

- **Python** 

- **Scikit-learn**: Model training and evaluation

- **Pandas, NumPy**: Data manipulation and preprocessing

- **Matplotlib, Seaborn**: Data visualization

# Visualizations

- ROC Curve (AUC)

- Precision–Recall Curve

- Confusion Matrix

- Each visualization helps interpret model behavior and understand trade-offs between precision and recall.
