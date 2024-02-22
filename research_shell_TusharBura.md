# Research Project:


# Shell Commands Answers:

- Describe the difference between `cd`, `cd ..`, and `cd ~`.
  <br>
  - `cd`: Changes the current directory to the specified directory.
  - `cd ..`: Moves up one directory level from the current directory.
  - `cd ~`: Changes the current directory to the user's home directory.

- What is the purpose of the `chmod` command?
  <br>
  `chmod` is used to change the permissions of files or directories in Unix-like operating systems. It can modify the read, write, and execute permissions for the owner, group, and others.

- How would you display the value of the PATH environment variable?
  <br>
  `echo $PATH`

- In the current folder, you have hundreds of files in `.csv`, `.log`, `.out` format.
    - How to count the line numbers of each `.csv` file?
      <br>
      `wc -l *.csv`
      
    - How to print the last line of each `.log` file?
      <br>
      `tail -n 1 *.log`
      
    - How to print a list of `.out` files that contain `Error` somewhere in the file, and also print the line that includes `Error`?
      <br>
      `grep -H "Error" *.out`

- How would you print the second column of a space-separated file (for example, `test_data.out`) using `awk`?
  <br>
  `awk '{print $2}' test_data.out`

- Describe the difference between `ps`, `top`, `htop` commands.
  <br>
  - `ps`: Reports a snapshot of the current processes.
  - `top`: Provides a dynamic real-time view of system processes, updating periodically.
  - `htop`: Similar to `top` but offers more interactive features like scrolling and mouse support, providing a clearer overview of system processes.

