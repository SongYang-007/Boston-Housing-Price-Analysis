
# Boston Housing Price Analysis

This project analyzes the Boston Housing dataset from the 1970s to explore the key factors influencing housing prices and to compare the performance of different predictive models.

## Project Background
The Boston Housing dataset contains 506 observations with 14 features describing economic, social, and environmental characteristics of neighborhoods in Boston, such as crime rate, number of rooms, tax rate, and pupil–teacher ratio.  
The target variable is the median housing price.

The objective of this project is to understand how different housing-related features affect prices and to evaluate multiple modeling approaches for housing price prediction.

## Objectives
- Analyze correlations between housing prices and explanatory variables  
- Visualize the distribution of key features  
- Build and compare different predictive models  
- Evaluate model performance using quantitative metrics  

## Methods

Three different modeling approaches were implemented and compared in this project:

### Linear Regression
Linear regression was used as a baseline model to capture the linear relationship between housing prices and explanatory variables.  
This model provides an interpretable reference for evaluating the performance of more advanced methods.

### Robust Regression (Huber Regressor)
Robust regression was applied to reduce the influence of outliers in the dataset.  
The Huber Regressor combines squared loss and absolute loss, making it less sensitive to extreme values while maintaining stable parameter estimation.

### Multi-Layer Perceptron (MLP)
A multi-layer perceptron (MLP) neural network was constructed to model non-linear relationships between housing features and prices.  
The model consists of multiple hidden layers and was trained using a training–validation–testing split to prevent overfitting and improve generalization.

All models were evaluated using Mean Squared Error (MSE) and the R² score on the test set.

## Results

| Model | MSE | R² |
|------|-----|----|
| Linear Regression | 24.81 | 0.66 |
| Robust Regression | 28.83 | 0.61 |
| MLP | 11.75 | 0.84 |

Linear regression and robust regression were primarily used as baseline models to establish reference performance levels.  
Due to its significantly superior predictive accuracy, detailed visualizations are presented for the MLP model.

## Visual Results

### Model Prediction Performance (MLP)
![MLP Prediction Results](figures/mlp_prediction.bmp)

The scatter plot compares true housing prices with MLP-predicted values, showing strong alignment between predictions and actual values.

### Training Process (MLP)
![MLP Training Loss](figures/training_loss.bmp)

The training and validation loss curves indicate stable convergence and effective learning during model training.

## Project Structure


Boston-Housing-Price-Analysis/
├── data/
│ └── houseprice.csv
├── figures/
│ ├── mlp_prediction.bmp
│ └── training_loss.bmp
├── *.py
├── .gitignore
└── README.md