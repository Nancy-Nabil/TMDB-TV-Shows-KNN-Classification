🎬 TMDB TV Shows — KNN Classification
📋 Project Overview
This project applies K-Nearest Neighbors (KNN) to predict whether a TV show is highly rated using data from the TMDB TV Shows dataset.
A show is labeled 1 (highly rated) if its vote_average >= 7.5, otherwise 0.

🚀 Steps Performed
1. Data Preprocessing
Selected Features: number_of_seasons, number_of_episodes, vote_count, vote_average, popularity, episode_run_time
Target Variable: HighRated (binary classification)
Missing Values: Dropped rows with nulls in selected features.
Normalization: Standardized all numeric features with StandardScaler.
Data Splits:
Training: 60%
Validation: 20%
Test: 20%
Stratified sampling applied to preserve class distribution.
2. KNN Model
Library: scikit-learn
Tuning: Tested K from 1 → 30 on training subset
Best K: 4
Validation Accuracy: 94.68%
3. Cross-Validation
Method: 5-Fold Cross-Validation on the full training set
Average Accuracy: 91.64%
4. Confusion Matrix & Test Results
Test Accuracy: 93.67%
Confusion Matrix:
True Positives (TP): 176
True Negatives (TN): 194
False Positives (FP): 10
False Negatives (FN): 15

Metrics:

Precision: 0.95
Recall: 0.92
F1-score: 0.93

5. Overfitting Discussion
Validation & test accuracies are close → minimal overfitting.
Cross-validation showed stable performance across folds.
Overfitting mitigation techniques used:
Proper K tuning
Feature normalization
Stratified splits
6. Visualizations
Confusion matrix heatmap
PCA 2D plot of classes (optional), showing partial separation
📊 Conclusion
The KNN classifier performed strongly, with test accuracy ~94%.
Model generalized well across validation and cross-validation.
Small improvements possible with:
Feature engineering
Ensemble models
Addressing class imbalance
📂 Repository Structure

TMDB-TVShows-KNN-Classification/
│
├── data/
│   └── tmdb\_tv\_shows.csv     # Dataset 
│
├── notebooks/
│   └── knn\_classification.ipynb
│
├── scripts/
│   ├── preprocess.py
│   ├── train\_knn.py
│   └── evaluate.py
│
├── README.md
└── LICENSE

🛠 Technologies
Python 3.x
pandas, numpy
scikit-learn
matplotlib, seaborn
👩‍💻 Author
Nancy Nabil Mohamed Emam
📧 Contact: nancnanbil647@gmail.com
🔗 LinkedIn: Nancy Nabil
MennaAllah Mohamed Ibrahim
📧 Contact: mennafakharanyy@gmail.com
🔗 LinkedIn: Menna Fakharany
