
git --version 


==============

Setting up git on your device/ Configuring Git

Open terminal
1. git config --global user.name "KandpalJi"
2. git config --global user.email "codewithsk27@gmail.com"

To check if everything is all right
1. git config --list

credential.helper


==============================


Local and remote
1. Local: laptop / personal system
2. remote: Files and folders in github

================

.git folder

this .git folder is present inside all the folders/repositories whom the git is tracking (means storing the history of changes in their files)


ls -a to print hidden files/folders


==================

what is commit?
=> commit means a change
=> committing a change means taking screenshot of all the files and folders inside of a git repository.
=> And we can go back to any of the taken screenshot at any point of time in history


=================


Basic git commands
1. Clone and status

	=> Clone: cloning a repo from github (remote location) into local machine (system)
		git clone #link


=====================

Four types of stages/statuses of files in git:

1. "Untracked file"
	=> A file that is not currently been tracked by git
	=> isme hue changes git ko pta hi nhi chalenge
	=> git ki nazro mei ye bs ek file hai jisme changes hone ki git ko koi parwah nhi	 
	=> represented by "U" in VS Code

2. "Modified file"
	=> A file that had been modified in VS Code (and is tracked by Git)
	=> represented by "M" in VS Code	
	=> "Changes not staged for commit:"

3. "staged file"
	=> a modified file that is not yet committed

4. "Unmodified file"
	=> unchanged file


Inshort
	1. any changes => modified
	2. nayi file => untracked
	3. modified yet not committed => staged

Each modified file needs to reach in a staged stage, for which we say "add" the file. staging (adding) before committing is kind of engagement before wedding

	add 
	and then commit

	4. unchanged => a committed file


====================

	=> Status: displays the status of the code
		git status 


====================

How Git tracks the changes?

Whenever we modify a file, we then apply a two step process afterwards:

Step 1: add     (engagement)
Step 2: commit  (wedding)

1. Add: 
	adds new or changed files to Git's staging area (i.e. file collection that is ready to be committed)

	add = modified -> staged

	a) git add #file_name
		adds file_name to staged area (index "added": "A")

	
	b) git add . 
		used to stage multiple files all together


2. Commit:
	=> commit is the "record" of change

	git commit -m "some message"
	

========================


Git Push commands: Lets push it now
modify -> add -> commit -> push

push: 
	1. upload local repo content to remote repo (github)
	2. Kinda just opposite to git clone
	

	git push origin main
	or 
	git push origin master

	
	origin: is the name of the remote github repo from which we initially made a clone in our system (default repo)
		by placing the above command we are basically telling git to make a change / commit exactly in the same repo.
		that repo is also called "default repo" and by default its name is "origin"

	
	main: is the name of the branch inside "origin" repo in which we are interested in making a change.


=======================

Init command: jahan chah wahan raah - make a local folder a git repository

git init: to create a new git repo

	1. git init


To make a local file remote: 
i.e. how to push a local file (now being added .git folder) into github

	1. git remote add random #link
		=> we want to add a new remote repo with name "random" (this name  is by default "origin"


	2. git remote -v
		=> to verify remote

	3. git branch
		=> to check branch

	4. git branch -M main
		=> rename the branch

	5. git push origin main

	6. git push -u origin main
		=> sets upsteam
		=> when we want to work on a project for so long that we don't want each time to write this origin main, so at once we say that "-u" and then for ever if we want to push something in the same repo "origin", we don't have to write that "origin main"
		=> from now on we'll write only "git push"


=======================

master used to be the "Default" branch name in Github few years ago but it eventually got changed and now the name of the default branch on github is "main"


=====================

Local Git: Git Workflow

github repo -> clone -> modify -> add -> commit -> push


========================

Git Branches

	1. when multiple developers/ feature teams/ bug fixer teams etc. are working on a single project and each one want to perform its unique act, what proceeds is that each entity creates its separate branch and then make all changes inside it. 

	2. Later some stage arrive when multiple branches are merged with the "main" branch (for example when a feature is completly made)


a) git branch 
	to view all the branches

b) git branch -M new_name
	to change branch name

c) git checkout #branch_name
	=> to navigate between multiple branches
	=> from current branch to branch_name branch

d) git checkout -b #new_branch_name 
	to create and navigate to the new branch "branch_name" 

e) git branch -d #branch_name
	=> to delete a branch
	=> we can't delete the branch in which we are currently present



	Whenever we make a change in one branch, the change is limited to the branch only and the other branches are independent of this change

===================

Merging code

	Way1
	
	git diff #branch ( to compare commits, branches, files and more)
	git merge #branch (merge the branches)

	
	Way2

	create a PR (pull request)
	it lets you tell others about changes you've pushed to a branch in a repo on GitHub



=======================


Pull: Remote (github) ke changes local ke andar

	i.e. jo github pe change ho gya wohi local pe bhi karna chah rhe hain

	git pull origin main

	it fetches and downloads content from a remote repo and immediately update teh local repo to match that content


========================

Resolving merge conflicts

an event that occurs when git is unable to automatically resolve differences in code between two commits

========================