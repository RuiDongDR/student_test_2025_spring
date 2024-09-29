research_shell_ShizheZhang
================
Shizhe Zhang
2024-09-27

# Project Description

## Overview

Trisomy 21, also known as Down’s syndrome (DS), is a human genetic
disease. It results from an abnormal number of human chromosome 21. The
proteins **APP** and **SOD1** are encoded by the genes on chromosome 21.
A set of available data measured in the Ts65Dn mouse experiment was used
in this investigation. Box plots were plotted to observe protein
expression levels and the two-way ANOVA was used to test the correlation
of protein expression levels with treatment and behavior. In addition,
the HSD test indicated the combination of treatment and behavior that
had the greatest effect on protein expressions. The results showed that
neither memantine nor stimulated learning had a significant effect on
APP expression, while memantine and no stimulation of learning resulted
in the highest amount of SOD1 expression in trisomic mice.

## Methods

All the manipulations were finished by the Rstudio version 2022.07.0+548
software program.

There were 72 mice in total participating in the experiment, with 34
trisomic mice and 38 controls, i.e. normal genotype mice.

The first thing to clean the dataset was deleting the missing values. By
filtering the data, protein APP and SOD1 were selected to be used, as
well as mouse id, genotype, treatment, behavior and class. In order to
explore the expression levels of the two proteins in trisomic and
control mice, treatment of saline and behavior of shock-context (S/C)
were controlled to set a new dataset. Two histograms and two boxplots
were plotted for visualization, and the same manipulations were done for
context-shock (C/S) mice.

The next step is to explore whether learning and medicine affect the
protein APP or SOD1 expression. Two-way ANOVA was used to manipulate the
data. The hypothesis that protein expression is independent of treatment
or behavior is not true if p value \< 0.05. Similar manipulations on APP
and SOD1, and then multiple comparisons were performed with the Tukey
test.

## (part of) Results

<img src="../student test 2024/Figures/figure1.png" width="1005" />

*Figure 1: Histogram of APP expression level in control and Ts65Dn
without treatment or behavior.*

<img src="../student test 2024/Figures/figure3.png" width="1087" />

*FIGURE 3. APP and SOD1 expression in different genotype with saline
treatment and shock-context behavior.*

|       Source        | DF  | Sum Sq  |  Mean Sq  | F value | Pr(\>F) |
|:-------------------:|:---:|:-------:|:---------:|:-------:|:-------:|
|      Treatment      |  1  | 0.00175 | 0.0017535 | 0.5786  | 0.4472  |
|      Behavior       |  1  | 0.00067 | 0.0006712 | 0.2215  | 0.6381  |
| Treatment: Behavior |  1  | 0.00149 | 0.0014880 | 0.4909  | 0.4838  |
|      Residuals      | 503 | 1.52452 | 0.0030308 |   NA    |   NA    |

*TABLE 1. Analysis of variance response to APP with treatment and
behavior.*

### For more information and the whole article

You can find via [Effect of drug injection and stimulated learning on
trisomic mice expressions of APP and
SOD1](https://www.spiedigitallibrary.org/conference-proceedings-of-spie/12611/126115G/Effect-of-drug-injection-and-stimulated-learning-on-trisomic-mice/10.1117/12.2669963.full).

# Answer Questions

1.  `list.files(path = ".", all.files = TRUE)` or `ls -a` in Terminal

2.  `length(readLines("data.txt"))` or `wc -l data.txt` in Terminal

3.  `grep -i "error" *.log`

4.  `chmod +x script.sh`

5.  `tail -n 20 output.log` in terminal or `tail(filename, 20)` in R

6.  `cat file1.txt file2.txt > combined.txt` in terminal or read two
    files using R then combine them as combined.txt

7.  `grep "Completed" status.txt` in terminal or
    `print(grep("Completed", status, value = TRUE))` in R (“status” is
    the name reading `status.txt`)

8.  `sort unsorted.txt > sorted.txt`
