---
title: "research_shell_XinyiShang"
author: "Xinyi Shang"
output: html_document
---

# Task 1: Breast Cancer Survival Prediction

### Abstract

This study aims to identify *risk factors* that can predict survival outcomes of breast cancer patients. Utilizing patient data, we developed a Multiple Logistic Regression model with an **85.6%** accuracy in predicting survival odds, identifying *age, race, tumor stage, differentiation status, estrogen and progesterone status,* and *rate of positive regional nodes* as significant factors.

### Introduction

Breast cancer represents a significant portion of new cancer cases. This study analyzes various factors to predict breast cancer patient survival, emphasizing the importance of identifying high-risk patients for better clinical outcomes.

### Methods

#### Data Manipulation and Statistical Modeling

We used data from a **prospective cohort study**, covering *demographics, disease characteristics, and outcomes*. The analysis involved multiple logistic regression, with stepwise regression, LASSO, Ridge regression, and Elastic Net for model selection. Validation was performed using 10-fold cross-validation and ROC curve analysis.

#### Model Diagnostics

Diagnostic procedures tested linearity, multicollinearity, and influential outliers, ensuring model reliability.

### Results & Discussion

<br>

![Figure 1: ROC Curve](task1_fig1.jpg "Figure 1: ROC Curve")

<br>

Our analysis included 3480 **alive** and 616 **dead** cases, revealing significant predictors like *age, race, tumor stage,* and *hormone status*. The model achieved 85.6% accuracy in predicting survival odds.

The model shows high accuracy and sensitivity but highlights limitations such as low specificity and potential biases in race prediction. Future work could explore stratified analyses to develop race-specific models.

### Conclusion

The logistic regression model effectively identifies factors associated with increased risk of death among breast cancer patients, offering insights for targeted medical attention and policy-making.

---

#### GitHub Repository

The code and model used for our analysis can be accessed on our [GitHub repository](https://github.com/XinyiShang/p8130_final_project).

#### Final Report

The final project report is available [here](https://github.com/XinyiShang/p8130_final_project/blob/main/final_report.pdf).

---

# Task2: Shell Commands

- Describe the difference between `cd`, `cd ..`, and `cd ~`.
  `cd` changes the current directory to a different directory.
  `cd ..` changes the current directory to the parent directory of the current directory.
  `cd ~` changes the current directory to the home directory
  
- What is the purpose of the `chmod` command?
  chmod (change mode) changes the access permissions of files or directories. It allows you to set who can read, write, or execute the files.
  
- How would you display the value of the PATH environment variable?
  `echo $PATH`
  
- In the current folder, you have hunderds of files in `.csv`, `.log`, `.out` format.
    - How to count the line numbers of each `.csv` file?
      `wc -l *.csv`
    - How to print the last line of each `.log` file?
      `tail -n 1 *.log`
    - How to print a list of `.out` files that contains `Error` somewhere in the file, and also print the line that includes `Error`?
      `grep -H "Error" *.out`
      
- How would you print the second column of a space-separated file (for example, `test_data.out`) using `awk`?
  `awk '{print $2}' test_data.out`
  
- Describe the difference between `ps`, `top`, `htop` commands.
  `ps` displays information about active processes. By default, it shows processes associated with the current terminal session. There are several options available to customize the `ps` command, allowing it to display selected processes. 
  `top` provides a real-time view of the system’s running processes, including CPU and memory usage.
  `htop` is basically the same as `top`, but it adds color and provides a more user-friendly way to navigate and manage processes. Also, it displays a full list of processes running.
