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


2.2
Why did we commit A+B separately from C? When would you want to split commits this way?
so that we can keep changes organized and make it easier to track each feature. we can do this when working on diff features so it is easier to review and undo the changes made if we want. 


2.3
What would happen if you made a local commit first WITHOUT pulling? What command helps you check?
local changes might conflict with the changes on github. 
git status: to check my current status
git fetch: to check for updates from github before pushing


3.1
Did this merge create a merge commit or was it a fast-forward? How can you tell?
fast-forward, because main didnt change while we were on the branch. also git merge feature/profile-page output says fast forward. 

3.2
Why did this conflict happen? (Reference the rule: same file, same line)
because both branches changed the same line of same file. if this happens, git cant choose one on its own so it gives conflict error.


Would there have been a conflict if the two branches edited different lines of team.txt?
no conflict if diff lines edited.


Would there have been a conflict if one branch edited team.txt and the other edited about.md?
no conflict if diff files 


4.1
What is the purpose of a pull request? Why not just merge directly?
pull request lets team lead review your changes before merging them into the main branch. it is done so that errors or bugs are caught and corrected instead of merging directly without checking them.


Name two things a reviewer should check in a pull request.
whether the code works and when tested, gives the correct output.
no secrets or debugs in code.


What is the difference between a merge commit and a fast-forward merge?
merge commit: creates a new commit to combine changes from two branches.
fast forward: merge moves the main branch forward if there are no separate new commits on it.


Part 5:

1. Scenario A.
Ahmed creates a branch and changes line 10 of index.html. Sara creates a different branch and changes line 1 of the same index.html. Both merge into main. Will there be a conflict? Why or why not?
-Different lines of the same file hence no conflict, git merges automatically


2. Scenario B. 
Ali edits style.css on his branch. Fatima edits app.js on her branch. Both merge into main. Will there be a conflict? Why or why not?
-Different file hence no conflict


3. Scenario C. 
DevA changes line 5 of config.py to DEBUG = True. Dev B changes line 5 of config.py to DEBUG = False . Both merge into main . Will there be a conflict? If yes, show exactly what the conflict markers would look like in the file.
-Same lines, different values so there will be a conflict. 
  <<<<<<< HEAD
  DEBUG = True
  =======
  DEBUG = False
  >>>>>>> 

4. Scenario D. 
You run git merge feature/new-ui and see this output:

Auto-merging index.html
CONFLICT (content): Merge conflict in index.html
Automatic merge failed; fix conflicts and then commit the result.

Write out the exact steps (commands included) you would take to resolve this conflict and finish the merge.
- run git status to see which files conflicted
- open index.html and choose and combine the content
- delete all markers
- run git add index.html
- run git commit -m "fix: resolved conflict in index.html"
- git merge --abort cancels the merge if required

5. Scenario E.
Your teammate says: "I always do git pull before I start working every morning." Is this a good practice? Explain why or why not, and what could go wrong if they skip it.
-it's a good practice. we should always start from latest code. if we don't, we will starting changing the older version of th ecode hence the possibility of gettings conflicts later increase. 