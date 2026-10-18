# Git Assignment - Answers

Part 1:
Question 1: Terminal Basics

1. What is a terminal? How is it different from clicking through folders in a file explorer?
terminal is an app, usually command prompt and windows powershell, on which we just write commands instead of interacting with visuals like folders. 
we usually click folders in file explorer and make files using mouse clicks. but with terminal, we only give textual commands and they happen in the folder the command prompt is currently in. the folder path is always being shown at the start of each line.


2. Write the terminal command to: 
(a) list all files including hidden ones:
ls -a 


(b) create a folder called project:
mkdir project

(c) move into that folder:
cd project


3. What does the cd .. command do? What about cd ~ ?
cd .. : terminal comes out of only one folder
cd ~ : takes you back to home directly regardless of where we currently are


Q2. Version control concepts

4. Explain what version control is in your own words. Give one real-world analogy (not Google Docs — pick your own).
Version Control is a system for tracking and managing all changes done to files. basically, it helps us keep reecord of all changes so we can go back to an older version if we want. git is used for version control. 
e.g. it's like keeping diff drafts of an assignment so we can go back to any version we want if we make a mistake. 


5. What is the difference between Git and GitHubs? Can you use Git without GitHub?
Git is a tool on our computer used for version control and Github is the website which helps us store and keep our code online in repos. yes, git can work without github. 


6. Name three features GitHub provides that Git alone does not.
respositories, pages and pull requests.


7. What is a repository? What is the difference between a local repository and a remote
repository?
a repository is a project folder that is tracked by git incl with its full history. 
local repository is on our computer and a remote repo is the copy on github.


Q3. Git internals 

8. Explain what HEAD means in Git. What happens to HEAD when you switch branches?
HEAD is a pointer to where we currently are which is the latest commit in our current branch. when we switch branches, HEAD moves to point to the new branch.


9. What is a .gitignore file? Write a .gitignore that ignores: all .log files, a folder called node_modules/ , and any file ending in .env.
.gitignore file has names of all files that we dont want git to track.
*.log
node_modules/ 
*.env


Why did we commit A+B separately from C? When would you want to split commits this way?
so that we can keep changes organized and make it easier to track each feature. we can do this when working on diff features so it is easier to review and undo the changes made if we want. 

