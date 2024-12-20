
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

	2. 