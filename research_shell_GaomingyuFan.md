**Section I**
start with a section about any research project that you have been working on, with at least two subsections, some links, *Italic text* and **bold text** (to highlight some important content) and at least one table or figure. 


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

