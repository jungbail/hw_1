# Homework Debugging C and Linux Practice: Instructions

For this homework, you are going to work on getting your development environment setup with C and git. This will vary slightly for every student, but the goal is to get you comfortable with the tools you will be using for the rest of the semester.

- [Homework Debugging C and Linux Practice: Instructions](#homework-debugging-c-and-linux-practice-instructions)
  - [Learning Objectives](#learning-objectives)
  - [Prerequisites](#prerequisites)
    - [GIT Commit](#git-commit)
    - [C Installed](#c-installed)
    - [Setup - Cloning Your Repository](#setup---cloning-your-repository)
    - [:star: Using an IDE :star:](#star-using-an-ide-star)
  - [Instructions: Debugging Your First C Application](#instructions-debugging-your-first-c-application)
    - [Wait but I don't know C...](#wait-but-i-dont-know-c)
    - [:star: REMINDER :star:](#star-reminder-star)
    - [Report.md](#reportmd)
  - [🤖 Use of LLMs](#-use-of-llms)
  - [📝 Grading Rubric](#-grading-rubric)
    - [Submission Reminder 🚨](#submission-reminder-)
  - [📚 Resources](#-resources)
    - [Git](#git)


## Learning Objectives

The learning objects for this assignment are

* Setting up C and git on your local system or experience using them on the khoury servers
* Practice with linux 
* Practice compiling and debugging C code
* Working with markdown 
* Working with the assignment submission process

## Prerequisites 
For this assignment, you will
need to make sure the following is in place


1. Have your Github.com Account Setup ([Instructions](https://docs.github.com/en/get-started/signing-up-for-github/signing-up-for-a-new-github-account))
   * Free account is fine
   * We recommend a professional email that is not tied to a school, so your account exists after you graduate.
2. If you haven't already, in your canvas shell you will be provided with a Github classroom link that will 
let you use this repository as a template for your work. 

You will also need *git* installed ideally on your local system. If you are using a Windows system, you will need to install [Git Bash](https://git-scm.com/downloads). If you are using a Mac or Linux system, you should already have git installed.

### GIT Commit
Throughout this assignment you will be committing your changes to your repository. When you commit to Git.
* Commit frequently after every major change
* Use active/action verbs in your message, that are short yet descriptive
  * Here is a BAD commit message
  > changes made to readme
  * Here is an example of a better commit message
  > Added personal ident info: name, gitname, semester

See resources for into on Git Commit

> [!CAUTION]
> All assignments will need to have _at least_ three commits to earn full points. Most assignments will have many more than that (this is the only one who reaching three may be limited).

### C Installed
You will need to have C installed or work remotely on the course servers. Visit [Installing C Options](https://github.com/CS5008-Khoury/Resources/blob/main/InstallC.md) to learn more. 

### Setup - Cloning Your Repository 

On the various operating systems, there are terminal applications. These are used to interact with the operating system. For example, you can use the terminal to navigate your file system, and run programs. 

For Mac OS or Linux, the application is called terminal. For Windows 10 or 11, it is also called terminal, but that runs multiple types of processes. We recommend in the windows terminal, you either use the WSL (Windows Subsystem for Linux) or PowerShell. You can also access your terminal through your IDE, such as VS Code or CLion.

If you have it setup right, all of the operating systems should allow the `ls` command. This command will list the files in the current directory. 

1. Create a directory on your computer for CS 5008. For example, `cs5008`
2. Do a git *clone* request for your hw1 repository. 
   * You can do this by clicking the green "Code" button on the main page of your repository, and copying the link using the copy button. 
     ![Clone Example]
     * IMPORTANT❗  Double check that it is your personal repo, and not the general assignment repo. 
   * Then, in your terminal, navigate to your `cs5008` directory using `cd`, and type `git clone <link>`. (see linux commands in resources)
   * For example, if your link is `https://github.com/SP23-CS5008-lionelle/lionelle-hw1.git`
   * The command would be `git clone https://github.com/SP23-CS5008-lionelle/lionelle-hw1.git`



> You can also do this on the Khoury servers, but in order to get git working, you will need to setup a Personal Access Token (PAT) for your Github account. Here is a [quick guide](https://github.com/CS5008-Khoury/Resources/blob/main/pat_guide.md).

> [!IMPORTANT]
> The first time using Git, you will have to setup your email and name. You can do this by typing  
> `git config --global user.email "your_email"` and   
> `git config --global user.name "your_name"`.

### :star: Using an IDE :star: 
If you are using an IDE, such as VS Code or CLion, git is built into the applications, and we recommend getting project from git or VCS (version control system) and using the link to your repository. The name may change based on your IDE, but the functionality is the same. Feel free to ask in the general chat in MS Teams and students can help each other out pointing to the correct spot based on their IDE + OS. 

Here is the example from VS Code:

![VS Code Git]


## Instructions: Debugging Your First C Application
You are provided with a C file that doesn't currently run. You will use warnings, the comments, and logic to build a working program.  

👉🏽 **Task** 👈🏽: Fix [main.c](../src/main.c)

1. Open the file `main.c` in your IDE or text editor.
2. Read through the documented code. *You **DO NOT** have to know C to complete this assignment*. Instead, you should use what you know about programming languages in general to get an idea of what the code is doing. We will cover C in the next module. 
3. Compile `main.c`. Make sure you are using the `-Wall` flag. 
   * For most people the command will be `gcc -Wall main.c -o main.out`
   * If you do that, you can then run the program by typing `./main.out` in the terminal. 

   > [!WARNING] 
   > Your environment may modify the compile command a bit (for example Clion using cmakefiles.txt). If you are having trouble, ask in the general chat in MS Teams and students can help each other out. You will want to make sure you are using clang or gcc, and not the MSVC compiler (which is the default for Windows).

4. You will notice there are warnings when you compile using the clang compiler! This would cause the code to fail in the autograder as your code has to compile without warnings.
   1. **FIX**: Fix the warnings in the code. 
5. Now look at the logic of the program. Proper execution of the program looks like the following
```text
Please enter your name: Bob
Please enter a number: 20

Hello Bob
You are not old enough to drink in the US
Goodbye Bob
```
or
```text
Please enter your name: Jane
Please enter a number: 21

Hello Jane
You are old enough to drink in the US
Goodbye Jane
```
6. **FIX**: Fix the logic of the program so that it works as expected. Spaces between : and the name/number are required, as are the new lines. Make sure you run the program before trying to fix it, as there may be an unusual error that you can't see in the code (it may actually cause the program to crash)

> [!NOTE]
> A note on "Free"  
> In C, you have to manually free memory that you allocate. This is because C is a low level language, and it is up to the programmer to manage memory. In higher level languages, such as Python, Java, or C#, the language will automatically free memory for you. This is why you don't have to worry about it in those languages. However, what happens if you "free" memory, and then attempt to access the variable? This is called a "use after free" error, and it can cause a lot of problems. Use this knowledge to help find the mystery error. 

### Wait but I don't know C...
The errors in the code are similar to ones you can find in python or java. They are string issues or return statement issues. You also have examples throughout the code on how to do it correctly.  More importantly, as programmers making associations between languages becomes second nature to us. For many, your first job may be using a language you never programmed before, and you will be expected to pick up the language quickly. In the end, it is just a tool, and we use the best tool for the job. In this course, we use C, so you better understand what is going on 'under the hood' that many higher level languages hide.

### :star: REMINDER :star:
Make sure to commit between each change! For example, you fix spaces, you do a git commit -m'fixed spaces in strings'. Then you fix the return statement, you do a `git commit -m'fixed return statement in (func name)'`. Then you fix the logic, you do a `git commit -m'fixed logic in (location)'`.


### Report.md 
You will notice there are questions in your [readme.md](../README.md) and [Report.md](../Report.md) file. You will want to answer these questions. For this course, we will be doing a lot with Markdown files, so it is important to get used to them. You may even want to review the [Markdown Guide](https://guides.github.com/features/mastering-markdown/) to get a better understanding of how to format your readme.md file.

Every assignment will have to fill out both a README.md and Report.md, so make sure you review them!

> [!CAUTION]
> A common mistake in markdown files is not viewing how they render on the website. Always go to github and review
> how the markdown files really look. Graders go to github to review the code even though you submit on gradescope,
> as it will properly render latex math (which is required for a lot of reports). 

## 🤖 Use of LLMs
For this assignment, you should avoid LLMs for both the code and especially the report. The important part of this assignment is reasoning through the both the coding errors, and in the report reasoning through the answers. LLMs can hurt that reasoning process, and also lead you down the wrong path. At this point, it is best for you to reason through this assignment. We will have LLM use in the future but not this one. 


For studying, here are some prompts that can help

> I want to learn about Linux file permissions from scratch. Please teach me interactively:
> 
> 1. Start with the fundamentals - explain what file permissions are and why they > matter
> 2. Break down the permission system (read, write, execute for user/group/others)
> 3. Explain both symbolic (rwx) and numeric (755, 644) notation
> 4. Show me practical examples with real-world scenarios
> 
> After each concept, quiz me with questions to test my understanding. Give me immediate feedback on my answers - if I'm wrong, explain why and help me understand the correct answer. If I'm right, confirm it and build on that knowledge.
>
> Adjust the difficulty based on how I'm doing. If I'm struggling, slow down and provide more examples. If I'm getting it quickly, move faster and introduce more advanced concepts.
>
> Make it conversational and encouraging - I learn best through back-and-forth dialogue rather than lectures. Ask me one question at a time and wait for my response before continuing.
>
> Let's start with the very basics!

or with C

> I'm a Python programmer learning C for the first time. I haven't learned pointers yet, so please don't cover those yet.
>
> Focus on teaching me these fundamental differences between Python and C:
>
> 1. Type systems - why I need to declare types (int, float, char, etc.) vs > Python's dynamic typing
> 2. Variable declaration - declaring variables before using them
> 3. The compilation process - how C is compiled vs Python being interpreted
> 4. Basic I/O - using printf() and scanf() vs Python's print() and input()
> 5. Format specifiers (%d, %f, %s, etc.) and why they're needed
> 6. Semicolons, curly braces, and C syntax basics
> 
> Teach me interactively by:
> - Showing me Python code, then the equivalent C code side-by-side
> - Explaining why C requires what it does
> - Asking me to predict what C code I'd need for a given task
> - Quizzing me after each concept to check my understanding
> - Giving immediate feedback - if I'm wrong, explain why and show the correct  answer
> - If I'm right, confirm it and build on that knowledge
> 
> Make it conversational and adjust difficulty based on my responses. Ask me one question at a time and wait for my answer before continuing.
>
> Start with the absolute basics - assume I've only ever written Python. Let's begin!

## 📝 Grading Rubric

Click on the Gradescope link on the sidebar of the Canvas course. Select CS 5008, and select Homework 01. Ideally, you follow the link at the bottom of the assignment page. 

On Gradescope, select that you want to submit your code via Github, and connect your Github account with Gradescope. You'll need to authorize Gradescope to have access to your account. 

1. Learning (AG)
   * Code compiles without warnings
   * Simple errors fixed in the code (spacing, string issues, etc.)
2. Approaching  (AG)
   * Harder logic errors are fixed (free, logic)
3. Meets  (MG)
   * Report questions 1-9 are answered correctly.
4. Exceeds  (MG)
   * At least 3 commits
   * Linear search and binary search question answered correctly
   * References formatted correctly


AG - Auto-graded  
MG - Manually graded

### Submission Reminder 🚨
For manually graded elements, we only guarantee time to submit for a regrade **IF** you submit by the **DUE DATE**. Submitting late may mean it isn't possible for the MG to be graded before the **AVAILABLE BY DATE**, removing any windows for your to resubmit in time. While it will be graded, it is always best to *submit by the due date*, so you have full opportunity to improve your grade.


If you need a reminder about the grading policy, please review the syllabus and the canvas page on 'formative/summative' grading. This class uses a unique grading system that will allow you to be flexible with due dates and multiple resubmissions (if you submit with time for TAs to give feedback), but we also ask that you continue to work on the assignment until you get a full grade.

> [!CAUTION]
> For this class, we give about a month for the available until date. This means you will only have a few manual resubmission attempts, and most everyone uses at least one! As such it is essential you submit on time!


## 📚 Resources

### Git
* [Git Handbook](https://docs.github.com/en/get-started/using-git/about-git) -- start here
* [clone](https://github.com/git-guides/git-clone)
* [commit](https://github.com/git-guides/git-commit)
* [add](https://github.com/git-guides/git-add)
* [push](https://github.com/git-guides/git-push)
* [How to Write Better Commit Messages](https://www.freecodecamp.org/news/how-to-write-better-git-commit-messages/)




<!-- Link definitions-->
[VS Code Git]: vscode_git.png
[Clone Example]: clone_example.png
