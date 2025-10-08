# ClimateWins: Predicting Weather with Machine Learning

**Objective:** Predict weather in mainland Europe by using historical weather data and machine learning methods. 

**Why?** Assist ClimateWins in predicting climate change and its consequences

Methods used: 
1. KNN
     - Non-parametric classifier that takes on supervised learning. 
Used to classify good weather and bad weather by reducing distance between similar groups
    - Tested on both scaled and unscaled data
2. Decision Tree
     - Classification tree used to define good and poor weather. 
     - Function: DecisionTreeClassifier
     - Gini criterion used to measure the quality of split
     - Minimum number of samples required to splot the note is 2
3. ANN
   - Input data goes through various layers to classify bad and good weather.
   - Many layer adjustments but final model had three layers:
       - Layer 1: 100
       - Layer 2: 50 
       - Layer 3: 25

### Summarized Results  

1. KNN
  - Predicts pleasant weather at a 95% accuracy rate
  - None of the weather stations are fully accurate except for Sonnblick which has a perfect accuracy rating. 
  - F1 scores for the scaled data mirror the other classifiers.
2. Decision Tree
  - Variates in performance between the different weather stations. 
  - The complexity of the tree seems to indicate overfitting as well.
3. ANN
   - Does not converge on the test data. 
   - Highest average F1 Score: 0.75

**Which model performed the best?**  
KNN and decision tree performed similarly. ANN has the highest F1 score. 
With a more complex black box (100, 50, 25) and higher iterations the ANN approach the f1 score is slightly higher than the KNN and decision tree classifiers. 
ANN may be the best option to fine-tune going forward. 
A common issue is that the models are doing well on specific cities but not others. Using hyperparameters may help with this problem. Each model overfits on SONNBLICK data due to it only having one type of classified weather.  
**Future Steps**  
Fine – tuning ANN with hyperparameters
If insufficient, other methods or even unsupervised models may be tested.
Perfected model can be used to predict future weather events!

