# Breast Cancer Classification Analysis

This repository contains an R Markdown report and corresponding PDF output titled **"Breast Cancer Classification Analysis"**. The analysis uses supervised and unsupervised learning techniques to classify breast cancer tissue samples as benign or malignant, based on features from the Wisconsin Breast Cancer dataset.

---

## Project Information

- **Title**: Breast Cancer Classification Analysis  
- **Author**: Pranav Sunil Raja  
- **Student ID**: 240408545  
- **Date**: November 19, 2024  
- **University**: Newcastle University – MSc Data Science & AI  
- **Format**: R Markdown (`.Rmd`) + PDF Output

---

## Objective

This project investigates whether nine diagnostic features from FNAC (Fine Needle Aspiration Cytology) breast tissue samples can be used to classify tumors as **benign** or **malignant**. The goal is to apply statistical and machine learning methods to develop a robust classification pipeline with interpretable and accurate results.

---

## Dataset

- **Source**: `mlbench::BreastCancer`
- **Total Observations**: 699
- **Post-cleaning**: 444 benign, 239 malignant
- **Features**: 9 numerical features (e.g., Cl.thickness, Cell.size)  
- **Target**: Class (benign = 0, malignant = 1)

---

## Analysis Overview

### 1. Data Exploration
- Handled missing values and converted class to binary
- Summary statistics, scatter plot matrix, correlation matrix
- Standard deviation analysis to understand variable spread

### 2. Unsupervised Learning
- **K-Means Clustering**: Grouped data based on feature similarities
- Evaluated natural group separability between benign/malignant classes

### 3. Supervised Learning
- **Best Subset Selection (BIC)**: Achieved best performance (3.6% test error)
- **Lasso Regression**: Penalized logistic regression using `glmnet`
- **Linear Discriminant Analysis (LDA)**: Evaluated classification performance with all features

### 4. Model Comparison
| Model                         | Test Error |
|------------------------------|------------|
| Best Subset (BIC)            | **3.6%**   |
| Lasso Logistic Regression     | 5.1%       |
| Linear Discriminant Analysis | 6.6%       |

---

## Repository Structure

```
BreastCancer-Classification
 ┣ BreastCancer_analysis_report.Rmd
 ┣ BreastCancer_analysis_report.pdf
 ┗ README.md
```

---

## Getting Started

### Requirements

Make sure you have the following R packages installed:

```r
install.packages(c("mlbench", "dplyr", "ggplot2", "ggbiplot", "caret", "purrr", "bestglm", "glmnet", "MASS"))
```

### To Render the R Markdown

```r
rmarkdown::render("BreastCancer_analysis_report.Rmd")
```

You can also open the `.Rmd` file in RStudio and click **Knit** to generate the report.

---

## Conclusion

The project shows that a carefully selected subset of features—specifically *Cl.thickness, Cell.size, Marg.adhesion, Bare.nuclei,* and *Bl.cromatin*—can effectively distinguish between benign and malignant cases. The BIC-based logistic regression model emerged as the best performer among all approaches, offering a robust foundation for clinical decision-making.

---

## Author

- **Pranav Sunil Raja**  
- MSc Data Science & AI, Newcastle University  
- GitHub: [@pranavsraja](https://github.com/pranavsraja)

---

## License

This project is for academic and educational use only.
