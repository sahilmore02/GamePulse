# GamePulse: Online Gaming Behaviour Analysis

## Project Overview

GamePulse is a data analytics project focused on understanding online gaming behaviour, player engagement, and in-game purchase patterns. Using Python and machine learning techniques, the project explores player characteristics, identifies behavioural patterns, segments players, and classifies engagement levels.

The project follows an end-to-end workflow, from data inspection and exploratory data analysis to statistical testing, clustering, anomaly detection, and predictive modelling.

## Dataset

- **Dataset Name:** Predict Online Gaming Behavior Dataset
- **Dataset URL:** https://www.kaggle.com/datasets/rabieelkharoua/predict-online-gaming-behavior-dataset
- **Records:** 40,034
- **Original Features:** 13
- **Target Variable:** `EngagementLevel`

The dataset contains information about player demographics, gaming preferences, playtime, session activity, player progression, achievements, and in-game purchases.

**Note:** The dataset is synthetic. Findings represent patterns within this dataset and should not automatically be generalised to real-world gaming populations.

## Tools and Technologies

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- SciPy
- Scikit-learn
- Kaggle Notebooks

## Project Workflow

### 1. Initial Data Inspection
- Examined dataset structure, dimensions, and data types.
- Checked for missing values, duplicate records, and duplicate player IDs.
- Reviewed descriptive statistics and categorical distributions.

### 2. Data Cleaning and Preparation
- Validated numerical and categorical values.
- Checked for invalid values and inconsistent records.
- Investigated potential inconsistencies in player session activity.

### 3. Exploratory Data Analysis (EDA)
- Analysed player demographics and gaming preferences.
- Visualised engagement levels and gaming behaviour.
- Explored relationships between playtime, session activity, and engagement.
- Examined in-game purchase patterns.

### 4. Statistical Analysis
- Calculated descriptive statistics and examined numerical correlations.
- Compared gaming behaviour across engagement groups.
- Used the Kruskal-Wallis test to evaluate differences in playtime distributions across engagement levels.

### 5. Player Segmentation Using K-Means
- Standardised selected numerical features.
- Applied K-Means clustering to group players based on gaming behaviour and progression.
- Interpreted three clusters as high-playtime, high-level, and low-playtime player groups.

### 6. Anomaly Detection Using Isolation Forest
- Applied Isolation Forest to identify unusual combinations of player characteristics.
- Flagged approximately 5% of records as potential anomalies using the selected contamination setting.
- Investigated unusual records without automatically treating them as errors.

### 7. Predictive Modelling
- Built classification models to predict player engagement levels.
- Compared a baseline model, Logistic Regression, and Random Forest.
- Evaluated model performance using accuracy, precision, recall, and F1-score.

The Random Forest model achieved approximately 89.97% accuracy when session frequency and average session duration were included. However, these features may be closely related to how engagement levels were defined. Potential target leakage must therefore be considered, and this result should not be interpreted as proof of reliable real-world predictive performance.

### 8. Insights and Business Recommendations
- Summarised the main findings from the analysis.
- Identified opportunities to investigate player engagement and progression.
- Evaluated whether engagement level meaningfully differentiated in-game purchase behaviour.
- Developed recommendations while considering the dataset's limitations.

## Key Findings

- The dataset contains 40,034 player records with no missing values or duplicate rows.
- Approximately 48.39% of players belong to the Medium engagement category, while High and Low engagement each account for approximately 25.8%.
- High-engagement players averaged 14.25 sessions per week and an average session duration of approximately 131.92 minutes.
- Low-engagement players averaged 4.53 sessions per week and an average session duration of approximately 66.88 minutes.
- Average playtime was similar across engagement groups. The Kruskal-Wallis test did not find a statistically significant difference in playtime distributions at the 5% significance level (p = 0.1604).
- Approximately 20.09% of players made in-game purchases. Purchase rates were similar across engagement groups, ranging from approximately 19.73% to 20.65%.
- K-Means identified three player segments primarily differentiated by playtime and player level.
- Isolation Forest flagged approximately 5% of records as potential anomalies. These records require further investigation rather than being assumed to be incorrect.
- Session frequency and average session duration were the most important features in the full Random Forest model, highlighting the need to investigate potential target leakage.

## Limitations

- The dataset is synthetic and may not represent real-world gaming behaviour.
- The data does not provide a usable timeline for analysing player retention or changes in behaviour over time.
- The measurement period for certain gaming activity variables is unclear.
- Some records show potentially inconsistent combinations of session activity and playtime.
- The predictive model may be affected by target leakage because session-related features may be closely related to the engagement label.
- Clustering and anomaly detection results depend on the selected features and model settings.
- Observed associations do not establish causation.

## Conclusion

GamePulse demonstrates an end-to-end data analytics workflow using Python, covering data preparation, exploratory analysis, statistical testing, player segmentation, anomaly detection, and introductory predictive modelling.

The project emphasises interpreting results carefully, communicating findings clearly, and recognising the limitations of the available data rather than relying solely on model performance metrics.

## Project Notebook

Kaggle Notebook: https://www.kaggle.com/code/sahilmo/gamepulse
