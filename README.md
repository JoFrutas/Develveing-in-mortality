ICU Mortality Analysis
This repository contains the R Markdown script and associated data files used for analyzing ICU mortality rates using various severity scores (SAPS II, SAPS III, APACHE II, and SOFA scores). The analysis includes logistic regression models, comparisons of model performance, and adjusted mortality rate calculations segmented by age.

Project Overview
The goal of this project is to analyze the mortality rates in ICU patients based on different severity scores and to understand the impact of these scores on predicting mortality. The analysis is performed on a dataset containing patient information and various severity scores.

Data
The data used in this project is stored in an Excel file df.xlsx located in the dados directory. The dataset includes the following columns:

sapsii
sapsiii
valor_sofa_initial
apacheii
Death_ICU
Death_outside_ICU
age
Various SOFA sub-scores
Analysis
The analysis includes the following steps:

Data Preprocessing: Conversion of relevant columns to numeric, handling missing values, and creating new columns for mortality status.
Logistic Regression Models: Fitting logistic regression models to predict ICU mortality using SAPS II, SAPS III, APACHE II, and SOFA scores.
Model Comparison: Comparing the models using Akaike Information Criterion (AIC) and pseudo R-squared values.
Adjusted Mortality Rates: Calculating adjusted mortality rates based on SOFA scores and segmenting the data into different age groups for further analysis.
Random Forest Model: Training random forest models to predict mortality status outside ICU and identifying important predictors.
Statistical Tests: Using the Wilcoxon rank-sum test to compare adjusted mortality rates between different age groups.
Results
The results of the analysis are summarized in the R Markdown document, including model summaries, adjusted mortality rates, and variable importance from the random forest models. Key findings include:

The performance of different severity scores in predicting ICU mortality.
The impact of age on adjusted mortality rates.
Important predictors of mortality status outside ICU.
Usage
To reproduce the analysis:

Clone this repository.
Ensure you have the necessary R packages installed:
R
Copiar código
install.packages(c("readxl", "dplyr", "broom", "pscl", "randomForest", "caret", "ggplot2", "mice", "VIM"))
Place the df.xlsx file in the dados directory.
Open the R Markdown document and knit it to generate the HTML report.
Dependencies
The analysis relies on the following R packages:

readxl
dplyr
broom
pscl
randomForest
caret
ggplot2
mice
VIM
License
This project is licensed under the MIT License. See the LICENSE file for details.

Contributing
Contributions are welcome! Please feel free to submit a pull request or open an issue to discuss any changes or improvements.
