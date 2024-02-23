# Introduction

This tutorial & exercise, developed in 2024, is designed for trainees interested in joining the lab directed by Dr. Suzanne Leal in [Center for Statistical Genetics at Columbia University](https://www.neurology.columbia.edu/research/research-centers-and-programs/center-statistical-genetics#:~:text=We%20are%20a%20group%20of,statistical%20genetics%20and%20genetic%20epidemiology.). It reflects our expectation on your computing skills in R, Python, Linux shell commands, and hopefully your ability in learning new tools in bioinformatics and related fields as well. By completing these exercise you will first set up the computational environment on your computer, then perform some data analysis of small scale using some test data. However, it is important to point out that after joining the lab, most of the research requires access to high performance computing cluster in Linux, on large-scale data such UKBiobank and All of Us data.

You may generally write in one or two languages we mentioned above, but we believe that the learning curve for things you are not that familiar with (but required in this exercise) is reasonable. You are encouraged to search online for learning new tools, and even to ask ChatGPT if necessary, as the ability to search for answers and solve the questions itself is also required in our lab. However, if there is a blocker as you go through the material, please do not hesitate to contact us (rd2972@cumc.columbia.edu). (When you do so, please describe your question clearly and provide all the information necessary for us to help you.)

## Task 1: Unix command shell and install softwares

We assume you are comfortable with command-line interface (on Linux or Mac). In this task you are going to work with git from command shell, set up the computing environment, and install basic softwares and packages needed for data analysis of Tasks 2 and 3.

### Git

Most of our work will be saved and shared on github in public or private repositories. If you have not used git in the past, please follow the [instructions here for a 5 minutes git tutorial](https://wanggroup.org/orientation/5m-git).

As the next step please [fork](https://docs.github.com/en/free-pro-team@latest/github/getting-started-with-github/fork-a-repo) this repository, add your name to the Markdown file named `hello.md`, commit it to github with a customized commit message, eg, "Add my name and github handle", and [create a pull request](https://docs.github.com/en/free-pro-team@latest/github/collaborating-with-issues-and-pull-requests/about-pull-requests) so we can see your update and incorporate it to the repository.

### Markdown and shell

Create a new markdown file (using any text editor you prefer) named `research_shell_JohnSmith.md` (replace `JohnSmith` with your name), and start with a section about any research project that you have been working on, with at least two subsections, some links, *Italic text* and **bold text** (to highlight some important content) and at least one table or figure. The content of the report would not be considered in the evaluation, but it is important to make sure it is well structured and formatted, and written in English clearly. This section would be ~300 words.

In the same markdown file, the second section would be your answers to the questions about shell commands in `notebook/shell_questions.md`. If the answer is a code, put it in the code chunk in markdown.

### Install softwares and setup computing environment

We strongly encourage you to setup the computing environment through `micromamba` with the instructions [here](https://wanggroup.org/orientation/jupyter-setup). If you succesfully follow it up to install the `pisces-rabbit` part, then you don't need to install `SoS`, `jupyter notebook` and `R/Python` manually.

If you fail to install through `micromamba`, you shall install [`SoS`](https://vatlab.github.io/sos-docs/running.html#SoS-Workflow) (simply type `pip install sos` in the terminal to install, or, check out here for [alternative installation methods](https://vatlab.github.io/sos-docs/running.html#Local-installation) if you have troubles with that command), [`jupyter notebook`](https://jupyter.org/install) and you will need [`R`](https://www.r-project.org) and [`Python`](https://www.python.org/downloads/) as well.

After you setup the computing environment (if in `micromamba`, remember to activate the `pisces-rabbit` environment first), please download both notebooks under folder `notebook/` and the toy data under `data/` on your own computer and put your name in the filename as `finemapping_JohnSmith.ipynb` and `data_analysis_sos_JohnSmith.ipynb`. 

## Task 2: Statistical genetics in `R`

The first notebook, `notebook/finemapping.ipynb` is an exercise with the `susieR` package in R. This is somewhat advanced material for those who has a background in statistical genetics.

### Summary of the SuSiE method
Please add another section in the notebook after where you put your name, and make the section title "Summary of the SuSiE method". Then take a read at [this paper](https://academic.oup.com/jrsssb/article/82/5/1273/7056114) before you run this notebook to know some basic concepts that we might mention in the notebook. Please then summarise the SuSiE method in a paragraph and describe what it does. You are supposed to summarize it yourself instead of copying content from the abstract directly. You can start the summary after reading the paper but you may also understand it better after you run the notebook. Feel free to come back and edit this section any time.

Please note that you can use ChatGPT or other tools to help you understand the method, but make sure you understand what you write here -- we may ask you questions based on your response during the interview.

### Run the notebook

Please follow the instructions in the notebook, and run all the cells. Answer the questions within the notebook directly and keep the code (that you use to get the answer) instead just leaving the answer there.

### Problem solving

During the process of running the notebook, you can take some notes and put them into a new section at the end of the notebook, where you can share with us any problem you have and how you solve it (for example, by some QA page on [Stack Overflow](https://stackoverflow.com) or simply get the answer from ChatGPT. 

## Task 3: Data analysis in a `SoS` notebook

The second notebook, `notebook/data_analysis_sos.ipynb` is an exercise that cleans a toy data set based on the UKBB, and some analysis on the polygenic risk score (PRS). It involves coding in `Python` in a `SoS` notebook. In a sos notebook, you can run different kernels for different cells. Please follow the instructions in the notebook and remember to add your name at the beginning of the notebook if you haven't done so.

Feel free to share anything at the end of the notebook as well as you just did for the `notebook/finemapping.ipynb`.

## Task 4: Report your work and submission

Organizing and communicating your work with others is essential to your success in conducting reproducible computational research. After you have completed all the tasks above, please make a tarball for the markdown file and two notebooks and email it to `rd2972@cumc.columbia.edu` for us to review. Please make the email title as "Complex Traits Research Assistant Application: Exercise Submission".


