**Section I**

**Investigating the Relationship Between Air Quality and Cancer Incidence in the United States**
[Link](https://fangaomingyu.github.io/Investigating-Relationships-Between-Air-Quality-and-Lung-and-Bronchus-Cancer/)

*Introduction*
Questions discussed are Whether certain states have higher Lung and Bronchus cancer rate? What are the trends in Lung and Bronchus cancer incidence and air quality over time? Determine if there are geographical areas in the United States with consistently poor air quality and elevated Lung and Bronchus cancer rates. Are there any outliers in terms of cancer incidence or air quality? Whether there is a statistically significant correlation between long-term exposure to poor air quality (measured by pollutants like PM2.5 and ozone) and the incidence of Lung and Bronchus cancer in different regions of the United States?

*Time series Analysis*
![Image](URL "https://fangaomingyu.github.io/Investigating-Relationships-Between-Air-Quality-and-Lung-and-Bronchus-Cancer/results_files/figure-html/unnamed-chunk-4-1.png")

*Result*
The exploration of the link between total cancer rates and air quality yielded initial findings that were in line with our expectations: a positive correlation between cancer rates and PM2.5 levels, suggesting that poorer air quality could be associated with heightened cancer rates. In contrast, our analysis unexpectedly unveiled a negative correlation between ground level ozone concentration and cancer rates, contradicting our initial hypothesis which anticipated negative impact of higher ground level ozone concentrations.

**Section II**
the second section would be your answers to the questions about shell commands in `notebook/shell_questions.md`. If the answer is a code, put it in the code chunk in markdown.

- Describe the difference between `cd`, `cd ..`, and `cd ~`.
cd : When used without any arguments, cd changes the current directory to the user's home directory. 
cd.. : Move up one level in the directory hierachy
cd ~ : Change to the home directory.

- What is the purpose of the `chmod` command?
Change the permissions of a file or directory. Manage the security and accessibility of files and directories in a multi-user environment, allowing for the control of who can access or modify files and directories.

- How would you display the value of the PATH environment variable?
```
echo $PATH
```

- In the current folder, you have hunderds of files in `.csv`, `.log`, `.out` format.
    - How to count the line numbers of each `.csv` file?
    ```
    wc -l *.csv
    ```
    - How to print the last line of each `.log` file?
    ```
    tail -n 1 *.log
    ```
    - How to print a list of `.out` files that contains `Error` somewhere in the file, and also print the line that includes `Error`?
    ```
    grep -i "Error" *.out
    ```

- How would you print the second column of a space-separated file (for example, `test_data.out`) using `awk`?
```
awk '{print $2}' test_data.out
```
- Describe the difference between `ps`, `top`, `htop` commands.
The `ps` command provides a snapshot of the current processes. It doesn't continuously update the information, it just gives the status of processes at the time the command was run.
The `top` command provides a dynamic, real-time view of the system's running processes. It updates the information periodically, showing a list of processes that consume the most system resources (CPU, memory) by default.
The `htop` command is an enhanced version of `top`, with a more user-friendly and colorful interface. It provides a dynamic, real-time view of the running processes, similar to top, but with an improved visual representation.

