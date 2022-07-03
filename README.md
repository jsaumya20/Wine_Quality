# Wine_Quality
Predict the quality of white wine from the UCI Machine Learning Repository dataset
For this project I plan to build and interpret two models.
A model to predict Wine Quality score **(a regression model)**.This model will interpret the effect of each feature on quality. 
For example say for every unit increase in residula sugar the quality goes up by X units, etc.
A model to predict High Quality wines (those wines with quality >=7) vs Low quality (wines with quality < 7) **(a classification model)**

**For this project I plan to focus on the following criteria:**
1. Clarity of my code 
2. Clarity of my approach 
3. Model tuning and model selection 
4. Findings and data insights, i.e. clear interpretations. 

 Attribute information:
 **Input variables (based on physicochemical tests):**
   1 - fixed acidity
   2 - volatile acidity
   3 - citric acid
   4 - residual sugar
   5 - chlorides
   6 - free sulfur dioxide
   7 - total sulfur dioxide
   8 - density
   9 - pH
   10 - sulphates
   11 - alcohol
   **Output variable (based on sensory data):** 
   12 - quality (score between 0 and 10)
**Missing Attribute Values:** None

For Regression Model I have used Lasso, OLS Regression, Linear Regression Algorithmns.
For Classisfication Model, classification of wine was done as low quality and high quality wines after which I have ussed KNeighborsClassifier
and then calculated misclassification error, Cross-Validation Accuracy Score.

**Findings for Regression Model**

**Equation for Linear Reggresion :**

Quality (Y) = 110.101 -1.92800e+00 * volatile_acidity + 6.60000e-02residual_sugar -5.19000e-01 * chlorides +3.00000e-03 free_sulfur_dioxide -1.09122e+02 *density + 4.56000e-01 *pH + 5.71000e-01 * sulphates + 2.42000e-01alcohol

#So after removing variable(as suggested by Lasso) we get all pvalue as significant . So our final model for predicting Quality will have following variable : 'volatile_acidity', 'residual_sugar','chlorides', 'free_sulfur_dioxide', 'density','pH', 'sulphates', 'alcohol']

with everything being constant :

*On average ,If we increase alcohol amount by 1 unit under study, then the quality of wine would increase by 0.2415

*On average ,If we increase ph amount by 1 unit under study, then the quality of wine would increase by 0.4555

*On average ,If we increase residual sugar amount by 1 unit under study, then the quality of wine would increase by 0.0656

*On average ,If we increase density by 1 unit under study, then the quality of wine would decrease by -109.1225

So , Density can have very negative effect on the quality of wine .

**Findings for Classification Model**
k = 14 produces the best result with CV error close to 19%. This error is more than what we found before but is more reliable since it's a CV error. 
