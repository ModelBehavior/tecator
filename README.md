# [Project 1: Fat Content With IR](https://github.com/ModelBehavior/tecator/blob/main/teactor.Rmd)
## Regression Analysis of Fat content using IR as Predictors
### Data Description
Infrared (IR) spectroscopy technology is used to determine the chemical makeup of a substance. The device measures the absorbance of the sample at each individual frequency. This series of measurements creates a spectrum profile which can then be used to determine the chemical makeup of the sample material. A Tecator Infratec Food and Feed Analyzer intrument was used to analyze 215 samples of meat across 100 frequencies. In addition to an IR profile, analytical chemistry determined the percent fat for each sample.

### Goals of Analysis
If we can establish a predictive relationship between IR spectrum and fat content, then food scientist could predict a sample's fat content, then food scientist could predict a sample's fat content with IR instead of analytical chemistry. This could provide cost savings, since analytical chemistry is  a more expensive, time-consuming process.

### Methodology
The data was split into a testing and training set, and different preprocessing methods were done. \
The predictors are highly correlated, so PCA was used to reduce the dimension of the predictor space. \
Cross-validation was done to find the optimal value of the tuning parameters for models that required this. \
The different types of models that fit the data were: bagged trees, boosted trees, cubist, linear regression, decision trees, MARS, neural networks, KNN, random forest, and SVM. \
The neural network model performed the best on the training data with an RMSE of .85088724 and a standard error of 0.03248912, followed by the cubist model.

![](https://github.com/ModelBehavior/Shawn_Portfolio/blob/main/images/project1_1)

### Results 
Applying the best model to the test set, we get an RMSE of .7274025 with an r-squared of 0.9968596.
