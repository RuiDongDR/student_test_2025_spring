# ResNet50 model on LC/MS image classification

## Research Objectives and Background

This section provides a brief overview of my research project. The aim of the project is to **utilize a ResNet model to differentiate patients with arteriostenosis from healthy samples based on their LC/MS spectra**, as the traditional metabolomics analysis pipeline does not perform well with our data.

The motivation of this method can be found [here](https://pubs.acs.org/doi/full/10.1021/acs.analchem.2c05079).

## Data Description

In this section, we collected LC/MS spectra from **1011 participants** in both positive and nagative modes, with specific information as follows:

| Sample Group | Positive | Negative |
|--------------|----------|----------|
| Case         | 679      | 679      |
| Control      | 332      | 332      |
| Total        | 1011     | 1011     |

## Methodology

The classification of LC/MS spectra is base on the following steps (_for both positive ions and negative ions_):

1. Convert the raw image into compressed sparse matrix.
2. Split the original data set into training set, validation set, and testing set with a proportion of 6:2:2.
3. Split the images into small tiles and select those with high entropy and rich information for prediction.
4. Use these tiles for each image in the training set and validation set to train a ResNet50 model and save the best weight with the lowest validation loss.
5. Fit the testing set with the trained model to evaluate the model.

A overview of the workflow is presented below:
![Workflow](https://file%2B.vscode-resource.vscode-cdn.net/Users/xujingyi/Documents/Columbia/Leal%20lab/workflow%20of%20image%20prediction.png?version%3D1727195484439)

## Result Analysis

I've trained two ResNet models for positive ions and negative ions separately, using earlystopping strategy with patience of 30 to select appropriate epochs. The training process was completed on a Linux server.

The training performances of models selected for both positive and negative ions are summarized in the table below: 

|          | Epochs_end | Best_epochs | Val_loss | Val_auc | Train_loss | Train_auc |
|----------|------------|-------------|----------|---------|------------|-----------|
| pos      | 42	        | 12	      | 0.5222	 | 0.7581  | 0.4639	    | 0.8311    |
| neg      | 69	        | 39	      | 0.4407	 | 0.8504  | 0.4445	    | 0.8450    |

Finally, the testing sets were used to evaluate the models' performance. The confusion matrix and performance matrics for both models were calculated and presented below.

**Confusion matrix for positive ions model**
|          | Prediction(+) | Prediction (-) | Sum |
|----------|---------------|----------------|-----|
| Label(+) | TP - 112      | FN - 23        | 135 |
| Label(-) | FP - 19       | TN - 47	    | 66  |
| Sum	   | 131	       | 70	            | 201 |

**Confusion matrix for negative ions model**
|          | Prediction(+) | Prediction (-) | Sum |
|----------|---------------|----------------|-----|
| Label(+) | TP - 111      | FN - 24        | 135 |
| Label(-) | FP - 22       | TN - 44	    | 66  |
| Sum	   | 133	       | 68	            | 201 |

**Performances matrics for both models**
| Models | accuracy% | precision% | recall% | auc% | prc% | npv% |
|--------|-----------|------------|---------|------|------|------|
| pos	 | 79.10 (73.63, 84.58) | 85.50 (79.56, 91.13) | 82.96 (76.30, 89.47) | 77.08 (77.14, 77.46) | 83.71 (83.69, 83.99) | 67.14 (56.66, 78.26) |
| neg	 | 77.11 (71.14, 83.08) | 83.46 (76.98, 89.29) | 82.22 (75.00, 88.55) | 74.44 (74.32, 75.63) | 81.81 (81.73, 82.34) | 64.70 (53.23, 76.19) |

From the tables above, the positive ions model achieves better performances than negative ions model in terms of AUC. Comparing to other matrics, NPV achieves a disappointing performances with a value of 67.14% and 64.70%.

## Conclusion

The LC/MS spectrum, characterized by simple patterns and lines, lends itself well to interpretation using convolutional neural networks (CNNs). In our approach, we employed ResNet50 to build classification models for the LC/MS spectra. These models achieved less than 80% accuracy and AUC, suggesting room for improvement. Notably, models developed with positive ions exhibited slightly better performance than those built with negative ions.

The reduced model performance is mainly due to the limited ability to classify control samples, as reflected in the lower NPV values. This issue likely stems from an unbalanced dataset, where the scarcity of control samples makes it challenging to capture their distinct features. Addressing this imbalance is one potential strategy for enhancement. Additionally, selecting all tiles with any intensity/information, rather than only those with high intensity, may improve model performance. The suboptimal quality of LC/MS spectra also poses a challenge, and re-running the LC/MS procedure could be beneficial if feasible.



# Shell Commands Questions

1. **How would you list all files in the current directory, including hidden ones?**
   ```bash
   ls -a
   ```
2. **What command would you use to find the number of lines in a file named data.txt?**
    ```bash
    wc -l data.txt
    ```
3. **How can you search for the string "error" in all `*.log` files in the current directory?**
    ```bash
    grep "error" *.log
    ```
4. **Describe how you would change the permissions of a file named script.sh to make it executable.**
    ```bash
    chmod +x script.sh
    ```
5. **How would you display the last 20 lines of a file named output.log?**
    ```bash
    tail -n 20 output.log
    ```
6. **Explain how to combine the contents of file1.txt and file2.txt into a new file named combined.txt.**
    ```bash
    cat file1.txt file2.txt > combined.txt
    ```
7. **How would you check for the presence of the word "Completed" in a file named status.txt and display the line containing it?**
    ```bash
    grep "Completed" status.txt
    ```
8. **What command can you use to sort the lines in a file named unsorted.txt in alphabetical order and save the result to a new file named sorted.txt?**
    ```bash
    sort unsorted.txt > sorted.txt
    ```


