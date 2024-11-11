### Boston House Pricing Prediction using Machine Learning Regression Model

### Tools and Software Requirement
Tools used:
[![Tools](https://skillicons.dev/icons?i=python,sklearn,vscode,github,flask,&theme=light)](https://skillicons.dev)
Cloud and software used:
2. [Render Account](https://render.com/)
3. [VS Code IDE](https://code.visualstudio.com/)

### Dataset Information

**Dataset Characteristics:**  

    :Number of Instances: 506 

    :Number of Attributes: 13 numeric/categorical predictive. Median Value (attribute 14) is usually the target.

    :Attribute Information (in order):
        - CRIM     per capita crime rate by town
        - ZN       proportion of residential land zoned for lots over 25,000 sq.ft.
        - INDUS    proportion of non-retail business acres per town
        - CHAS     Charles River dummy variable (= 1 if tract bounds river; 0 otherwise)
        - NOX      nitric oxides concentration (parts per 10 million)
        - RM       average number of rooms per dwelling
        - AGE      proportion of owner-occupied units built prior to 1940
        - DIS      weighted distances to five Boston employment centres
        - RAD      index of accessibility to radial highways
        - TAX      full-value property-tax rate per $10,000
        - PTRATIO  pupil-teacher ratio by town
        - B        1000(Bk - 0.63)^2 where Bk is the proportion of black people by town
        - LSTAT    % lower status of the population
        - MEDV     Median value of owner-occupied homes in $1000's

    :Missing Attribute Values: None


# Observations & Prediction
### Observations
1. Pirplot
   ![pairplot](https://github.com/user-attachments/assets/9bb25c91-38e1-40e0-934b-3bcb1dc819e5)

2. 
![CRIM_Price](https://github.com/user-attachments/assets/fd7457c7-d12c-4427-bb7f-e5d01246b7c3)
It is observed that, **with lower crime rate, the price increases**

3. 
![RM_Price](https://github.com/user-attachments/assets/99446ee1-8739-405c-8b2d-3dbb2c331e50)
**With increaing number of rooms in the apartment indicates higher rent.**

![RM_Price_Corr](https://github.com/user-attachments/assets/1fbc2508-34df-47e1-b6d3-11b399178e63)
**A linear correlation is observed between the Price (dependant) and Room Numbers (independent) features.**

4.
![LSTAT_Price](https://github.com/user-attachments/assets/e1b50e01-934c-441e-b3ee-2a8726cc8b9f)
**When the LSTAT is decreasing, the price is increasing. Features are found to be negatively corralated.**

5. 
![CHAS_Price](https://github.com/user-attachments/assets/280f6ce0-72c0-4303-9e87-b0eb5bd9ec40)
**These features are not at all correlated.**

There should have some relationships of linearity, either positively or negatively.

6. ![PTRATIO_Price](https://github.com/user-attachments/assets/dff4ccfb-d6af-4cc4-8116-88bb780ab04a)
**Some negative corralation exist with inverse relationship. While PTRATIO increases price decresease.**

### Predictions
![pred_model](https://github.com/user-attachments/assets/f675aff2-4e32-4919-893d-1800ddf302b6)
**Prediction model is linear, so the model expects to perform well (y_test vs prediction)**

![residuals](https://github.com/user-attachments/assets/e3e0a63c-ad27-48f6-9291-c1ea281af4a2)
**Normally distributed, and there is little error between 10 to 30 (right side)**

![pred and res](https://github.com/user-attachments/assets/e878213d-2bb6-450c-bf7a-3749e40bfdfe)
**scatter plot with respect to prediction and residulas. Uniform distribution.**

Model expects to work well, and to make it guaranteed, let's have a look at the:
### Performance Metrics
- MAE: 3.162709871457406
- MSE: 21.517444231177212
- RMSE: 4.638689926172821
- R-Squared: 0.7112260057484932
- Adjusted R-Squared: 0.6840226584639308
  Here, Adjusted R-Squared is less than R-Squared. Which is expected and looks good.

  
### New data prediction
![prediction_webapp](https://github.com/user-attachments/assets/a541af41-b13b-44da-8b38-42e7d208e398)
HTML View

![prediction_results](https://github.com/user-attachments/assets/93d3b72e-3a61-4772-bd3f-219510aab101)
Predicts the price.
.......................................................................................................................................................................................

# Procedure
- Create a new environment
```
conda create -p venv python==3.11 -y 
```

- Activate the environment

```
conda activate venv/
```

- Installing the requirements
```
pip install -r requirements.txt
```

- Git Configuaration between VS Code and GitHub account 

```
git config --global user.name
git config --global user.email
```

- Commiting files
```
git status
```

```
git add . 
```

```
git commit -m "commit includes the files"
```

```
git push origin main
```

