# Research Project Overview
## Participants Demographics and Exploration

Upon initial exploration of the data, it was determined that understanding the demographics of the participants would be insightful.

![Figure 1. Demographics of Participants](/demographics.png)

Figure 1. Demographics of Participants. The figure displays the age, annual income, and gender distributions between the participants. 

Based on Figure 1, we see that the participants tend to be younger, averaging around 25 - 34 years old. The annual income appears to be fairly evenly distributed, but it is not as common to make more than $80,000 annually. Lastly, **the majority of participants are female-identifying people.**

## Descriptive Statistics and Tests

The experimental procedure appeared to have an even amount between the treatment and control group. From this Figure 6, the amounts of those that chose to donate and those that did not are fairly equal to each other. Between the two groups, the proportion of participants who decided to donate (based on `give_ind`) is higher within the control group at about 60.7% and 59.6% in the treatment group. The average donation amount between the two groups were approximately equivalent where the control group averaged around $0.38 and the treatment group averaged around $0.39.

### Chi-Square Test of Independence/Fisher’s Exact Test

The first test conducted was the *Chi-Square Test of Independence* for donation decision. The goal was to examine if there is a significant association between the experimental condition (treatment vs. control) and the categorical outcome of deciding to donate (donated vs. did not donate). The Chi-Square test is well-suited for categorical data and is used to assess relationships between two nominal variables.

With a p-value of 0.816, **there is no significant evidence to suggest that the experimental treatment had an effect on the likelihood of participants deciding to donate**. This high p-value indicates that any observed differences in donation decisions between the treatment and control groups could likely be attributed to chance.

### T-test/Mann-Whitney U Test

A *Mann-Whitney U test* for donation amounts was conducted because it is a non-parametric test to compare the donation amounts between participants in the treatment and control groups among those who decided to donate. The Mann-Whitney U test does not assume that the data are normally distributed, making it appropriate for analyzing differences in medians between two independent samples.

The p-value of 0.928 suggests that **there is no statistically significant difference in the median donation amounts between the treatment and control groups**. This indicates that the experimental treatment did not significantly affect the amount of money donated by those who chose to donate.

# Shell Questions/Answers

- cd alone takes you to your home directory.
- cd .. moves you up one directory (to the parent directory).
- cd ~ also takes you to your home directory, using a more explicit notation.


The chmod command stands for "change mode". It is used to change the access permissions of file system objects (files and directories). These permissions control the actions that users can perform on these objects, including reading, writing, and executing them.

To display the value of the PATH environment variable in a Unix-like operating system (such as Linux or macOS) or in a Unix-like shell environment on Windows (like Git Bash or Cygwin), you use 
```
echo $PATH
```

To count the line numbers of each `.csv` file, use 
```
for file in *.csv; do
    echo "$file: $(wc -l < "$file") lines"
done
```
To print the last line of each `.log` file:
```
for file in *.log; do
    echo "$file: $(tail -n 1 "$file")"
done
```
To print a list of `.out` files that contains `Error` somewhere in the file, and also print the line that includes `Error`:
```
grep -l "Error" *.out | while read file; do
    echo "Error found in file: $file"
    grep -Hn "Error" "$file"
done
```
To print the second column of a space-separated file (for example, `test_data.out`) using `awk`:
```
awk '{print $2}' test_data.out
```
- ps is best suited for capturing a snapshot of current processes with customizable output options.
- top provides a basic real-time overview of system performance with interactive controls for process management.
- htop offers an enhanced interface over top, with additional features for easier navigation, process management, and a more comprehensive view of system metrics.