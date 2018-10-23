# GitHub Tutorial

_by Osvaldo Gomez_

---
## Git vs. GitHub
- *__Git__*
  - Git job is to take snapshots of code  
  - Git doesn't require github
- _**Github**_  
  - Github job is to store the code in the website  
  - Github requires git

---
## Initial Setup

**There is 10 steps to create your account:** 
1. To make a github account you need to go to [_Github_](https://github.com/)  
2. When you are on the github website click on sign up  
3. Then start by creating your personal account
4. Make your username that fits you and you won't forget
5. Add in your email adress
6. Make a password make sure you will remember your password and make it strong so people can't guess propaly 
7. solve some quick puzzles just to verify you aren't a robot 
8. choose your personal plan
9. finish saying your experience with coding
10. you finished making your github account  
 
**Creating your SSH key:**
Once you are finish with creating your account you go click the to right profile icon and go to settings. on the left side bar go to SSH and GPG keys. go to new ssh keys and title it cloud9. After that, switch to your cloud9 tab and go to the top-right on the gear icon. Go to the SSH keys tab and copy/paste the 2nd SSH key into GitHub (private) (it starts with ssh-rsa).Add it to the SSH key, On cloud9 OPEN your workspace. You succesfully created your ssh key


---
## Repository Setup

On your cloud9 workspace to make your first github repo, on the bottom where it says bash **cd ~/workspace** and make a file by doing so you need to **mkdir first-repo** you later **cd first-repo** and also put **git init** now we need to add a README file, by doing so you put in **touch README.md** you then open the README file, in the file type in "This is my first repo" and save it, and add it by typing git add. commit it by using **git commit -m "create readme"** you need to put a message as i did by putting "create readme" But we can't push since we dont have a repository.

For that we need to create a repository, by doing that we have to go to [_Github_](https://github.com/), on the top right click on the plus sign and click on new repository name the repository as you named the file it has to be the exact same way you named your file wich in this case for us we will have to name it first-repo. create your repository and if they ask for your email to verify it do so if not continue normally.

---
## Workflow & Commands

Learning about workflow and commands you need to know what status, add, commit, and push do.

**Status:** to be able to use status you need to put git status. git status is a command to see which files have been edited since the last commit it will be red. git status is also a command to see which files are staged for the commit wich will make it green.


**Add:** add can be used to add files to be able to commit and can also be able to add a directory and can add even deleted files. For example we can use git add file.txt to add the file(s) to the stage to be committed. Also, we can use git add . wich will add the current/entire directory, git add . also ill only add new and modified files it won't add anything that's been deleted or been renamed for that you will need git add file.ext

**Commit:**to be able to commit you will need to use git commit -m "short/specific message" wich will take a ‘snapshot’ of the files on the stage. The message should be present-tense and describe what was modified in this snapshot wich will create a HTML template.

**Push:** to be able to use git push -u origin master. when you push you are sending our commits from our local repo to our remote repo. The -u means “upstream.” This tells git to remember which remote repo & branch to push our changes to when we type git push in the future. Also, origin is to know which remote we are pushing to. master is the main branch of our project.

---
## Rolling Back Changes

Rolling back changes is when you undo edits, undo add, undo commit, and undo push.

**undo edits:**
- will undo evreything you edited.for example, if you added text, delete text, or change texts.
- to be able to use undo edits you have to use git status.
- git status will give you two hints to be able to undo edits such as (use "%%%%%%%%%%%%" to discard changes in working directory) 
- to be able to undo edits you will need to type the command that will discard your changes.

**undo add:**
- will undo the files you added
- you must need to use git status 
- to be able to undo add you must use the command git reset <file>, <- you put the file you added that you want to undo.

**undo commit:**
- when you commit/snapshot acidently you can be able to undo the commit.
- you can't use git status to be able to commit
- the command that will make you able to undo commit is git reset --soft HEAD~1, and git reset --hard HEAD~1
- git reset --soft HEAD~1 will be able to makes sure that the changes in undone revisions are preserved.
- git reset --hard HEAD~1 you will use this if you don't want to keep these changes

**undo push:**
- to be able to undo push you will need to use git revert -m 1 <merge-commit>
-git revert -m 1 <merge-commit> will undo your commits you pushed 
- With ‘-m 1’ it tell git to revert to the first parent of the mergecommit on the master branch.