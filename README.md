# ClimateWins: Predicting Weather with Machine Learning

**Objective:** Predict weather in mainland Europe by using historical weather data and machine learning methods. 

**Why?** Assist ClimateWins in predicting climate change and its consequences

Methods used: 
1. KNN
     - Non-parametric classifier that takes on supervised learning. 
    - Used to classify good weather and bad weather by reducing distance between similar groups
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
4. Principal Component Analysis (PCA)
   - Reduces high-dimensional climate data into key components
   - Highlights dominant weather patterns, improves efficiency and interpretability
5. K-Means & Hierarchical Clustering
   - Identify natural groupings in weather behavior without labels
6. Convolutional Neural Networks (CNNs)
  - Uses various hidden layers to learn  patterns in the data for prediction
  - Detecting evolving weather systems across Europe
7. Recurrent Neural Networks (RNNs) & Long Short-Term Memory (LSTM)
  - Model how past conditions influence future outcomes
  - Essential for forecasting and trend detection
8. Random Forests
  - Provides feature importance, improving model transparency through a collection of decision trees
9. Generative Adversarial Networks (GANs)
  - Use two competing neural networks to generate artificial data to help train thee  model. 
  - Use photos like the ones on the right to predict current and future weather conditions
10. Bayesian Optimization
  - Efficiently tunes hyperparameters across all models

### Summarized Results  

1. KNN
  - Predicts pleasant weather at a 95% accuracy rate
  - None of the weather stations are fully accurate except for Sonnblick which has a perfect accuracy rating. 
  - F1 scores for the scaled data mirror the other classifiers.
2. Decision Tree
  - Variates in performance between the different weather stations. 
  - F1 scores are perfect for train data but much lower on testing data which indicates overfitting. 
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

