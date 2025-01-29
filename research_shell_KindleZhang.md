"# Initalize the first assignment" 

# section 1

# section 2

Answer the questions about shell commands 

**the answer is based on the git bash instead of git cmd(powershell)**

```bash
$ cd /d/Study/linux_learn/student_test_2025_spring
```

- How would you list all files in the current directory, including hidden ones?

```bash
$ ls -A
```

- What command would you use to find the number of lines in a file named data.txt?

```bash
$ wc -l data.txt
```

- How can you search for the string "error" in all *.log files in the current directory?

```bash
$ grep -n "error" *.log
```

- Describe how you would change the permissions of a file named script.sh to make it executable.

```bash
$ chmod +x script.sh
```

- How would you display the last 20 lines of a file named output.log?

```bash
$ tail -n 20 output.log
```

- Explain how to combine the contents of file1.txt and file2.txt into a new file named combined.txt.

```bash
$ cat data.txt data_2.txt > combined.txt
```

- How would you check for the presence of the word "Completed" in a file named status.txt and display the line containing it?

```bash
$ grep -n "Completed" status.txt
```

- What command can you use to sort the lines in a file named unsorted.txt in alphabetical order and save the result to a new file named sorted.txt?

```bash
$ sort unsorted.txt > sorted.txt
```