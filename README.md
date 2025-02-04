# Predicting Viewer Engagement with Educational Videos  

## Overview  
With the increasing popularity of online education, platforms like Coursera and videolectures.net host thousands of educational videos. However, matching learners with engaging content remains a challenge. This project applies **machine learning** to predict video engagement, helping to identify features that contribute to better learning experiences.  

## Problem Statement  
The goal is to predict whether a video is engaging based on its metadata and content features.

## Setup and Installation

To run this dashboard, the following libraries are required:
  1. pandas
  2. numpy
  3. matplotlib
  4. seaborn
  5. scikit-learn
- code: pip install pandas numpy matplotlib seaborn scikit

## How to run this project

1. Clone the Repository:
- code: git clone https://github.com/AsuquoAA/Predicting_Viewer_Engagement_with_Educational_Videos.git
2. Navigating to directory
- code: cd Predicting_Viewer_Engagement_with_Educational_Videos


## Dataset  
The dataset is derived from the **VLE Dataset** compiled by researchers at University College London.
1. The training (`train.csv`)
2. The test (`test.csv`)  

- **title_word_count**: Number of words in the title.  
- **document_entropy**: Measures topic variety in the transcript.  
- **freshness**: Days since video publication (higher means newer).  
- **easiness**: Text difficulty score (lower means harder).  
- **fraction_stopword_presence**: Fraction of stopwords in the transcript.  
- **speaker_speed**: Words per minute spoken by the presenter.  
- **silent_period_rate**: Fraction of the video where no speech is present.  
- **engagement** (Target variable, present in `train.csv` only):  
  - `True` if at least 30% of the video is watched.  
  - `False` otherwise.  

## Methodology  
The project follows a **standard machine learning pipeline**:  

1. **Exploratory Data Analysis (EDA)**  
   - Identified feature correlations and trends.  
   - Visualized data distributions.
   - 
2. **Data Preprocessing**  
   - Handled missing values and performed feature scaling.  
   - Converted categorical variables into numerical representations.  

3. **Model Selection & Training**  
   - Trained multiple classification models:  
     - Logistic Regression  
     - Random Forest  
     - Gradient Boosting (XGBoost)  
   - Performed **hyperparameter tuning** using GridSearchCV.  

4. **Model Evaluation**  
   - Used **AUC (Area Under the ROC Curve)** as the primary evaluation metric.  
   - Visualized feature importance to understand engagement drivers.  

## Results  
The best-performing model achieved an **AUC score of > 0.85**, meeting the passing criteria. The **most important features** influencing engagement included:  
- **document_entropy** (topic variety)  
- **speaker_speed**  
- **easiness** (text complexity)  

## Output Preview


## Acknowledgements
I would like to express my sincere gratitude to the University of Michigan for providing me with the opportunity to develop and apply my skills through their courses. Their exceptional teaching resources have significantly contributed to the completion of this project.

