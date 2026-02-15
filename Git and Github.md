
## What is Git?

	A version control, free, open source, under development and the most used worldwide. Most programmers interact with Git on a daily basis.

## What is a Version Control

	The management of changes to documents, computer programs, large websites and other collections of informations to track our code changes. We start out by saving an initial version of our code and then, from there, we save our changes there, not loosing track of the different versions. 

	This allows us to go back to a specific version, as well as to identify specific bugs.

## Terms

	Directory/dir -  Folder
	Terminal/CLI - Interface to run commands
	cd - change directory

## Git Commands

	git clone - Download a repository into a directory
	git add - Track changes made to the local directory
	git commit - Save the changes to .git file
	 git push - Upload Git commits to a remote repository
	 git pull - Download the Git commits to a local repository
	 git status - Gives info about all the files that have not been commited
	 git add - Tracks specific files so they can be commited (a . will tell to track all the files)

## SSH Keys

Lets start off by generating an assymetrical key pair so we can connect or machine to Github. 

Steps for Linux:

- Create an SSH pair (you can here set the directory the keys will be saved as well as a password)

	ssh-keygen

- Add it (copy paste) to: Github -> Settings -> Manage SSH and GPG keys -> Add new key

- Add it to the SSH config file (paste anywhere, but start or end prefered)
  
	  nano ~/.ssh/config


Lets break it down:

- `ssh-keygen` - Till here makes all the sense
- `-c` - If when creating the key we add the -C flag to the command it prompts us to add a Contact
- `-f` - Have no clue
- `~/.ssh/id_rsa ` - Key path

## Cloning files

We start by heading to the repo we want, click the green button "Code"choose which protocol we want to use and run in the terminal:

	git clone *link*   

From here we will have the repo directory in the directory we were on when downloading it.

On a code editor we will be able to see the folder popping up.

We can move inside it with the old:

	cd

Inside it we will have all the project we just downloaded along an hidden dot file. To display it we run:

	ls -la

This shows all the hidden files we have in the dir. The one we are looking for is the **.git** here reside a whole history of this repo, we can look at it as the mother meta data for Github.


## Editing files and checking status

Now its time to edit one o files we just cloned. Lets say we have an *html* file and we want to add some info to it, we will open this file (anyway we want) edit it, save it and then in terminal we will run:

	git status

The output will indicate that the very own file we just edited has been **modified** (the text will be red). Lets say we created a new file and ran the same command again, now the output will list the 

- Edited file as **modified**
- Newly created file as **untracked** (meaning git still doesnt know about that file)

In will now add these files to a queue before commit the changes to the *.git* file for this we run:

	git add *file_name* 

Using a "." will update all the files.

 Once we check for the status again we can see all files as tracked

	git status


## Commiting Files

Now we will be making changes to the directory we have by commiting the files we just edited/created, we run:

	git commit -m *"mandatory_description_tittle"* -m *"optional_description"*

Now they are ready to be uploaded to the remote repository!!

## Pushing files

In order to send the data we just created/changed we run:

	git push origin master

Lets break it down:

- `git push` - Till here makes all the sense
- `origin` - Is an argument that was assigned and refers to our machine -> SSH Keys
- `master` - The branch we commited our files toets break it down:

##  Adding a local Repository

The easiest way to do this is by creating the repository directly on Github.

**Pay attention to keeping the repository address provided handy**

Still, lets create a project locally and add upload it from the CLI.

In the project directory we run:

	git init

This will tell Git to add this directory to a new repository + creation path.

We check Status:

	git status

We add the file

	git add *file_name*

We commit the changes:

	git commit -m *"mandatory_tittle"* -m *"optional_description"*

We connect the just created git repository to our account

	git remote add origin git@github.com/example_account

We push the changes:

	git push -u origin master

	-u sets the upstream, if we use it, no need to write origin master in the next push.

## Git Branching

 Branches are what creates the soul of version controls.
 
 Nothing explains better than an image.
 
![[Pasted image 20260213162729.png]]

Has we can see we can create a branch and further develop a specific item of our project, independently from our main on production branch.

 
To create a branch from the CLI we start by:

Checking the number of branches;

	git branch

	This will take us to a file, with all the branches. The one we are currently at is indicated with * asterisc

To create a new branch we run:

	git checkout -b *branch_name* 

	This will move us diractly to the new branch

Navigating through branches:

	git checkout master
	git cheout new_branch

Merging branches:

	 First off we need to confirm the changes by a comparison of both files.
	 We ahve to remember that we are already in a branch of this repo, and we want to compare it against another branch

To do this we run:

	git diff new_branch

	At the top we will have:
	---a/file_name
	+++b/file_name

This shows which branch has been altered. Under this there will be differences text displayed.

Merging a branch:

	Here we have 2 ways of doing it
	
	1st used more to merge the master with a new branch

	git merge new_branch

	2nd + pull request (done from github)

	git push -u origin new_branch

In order to update the master branch locally:

	git pull  

Once we no longer need a branch we can delete it:

	git branch -d new_branch

### Branch Conflict

When the same line on different versions has code written in it a branch conflict will take place. This has to be solved manually and on the text editor.

What can happen is that when exiting (or changing branch) git we haven't commited our changes and because of that we end up loosing our work.

For this we should commit the changes we made, even with conflicts.

 
## Undoing on Git

Imagine we `add`ed a file by mistake, we can run:

	git reset

And the changes are gone

In case of commited changes we run:

	git reset HEAD~1

Lets break it down:

-  `git reset` - Till here makes all the sense
-  `HEAD`  - Informs Git that we are referring to the commit changes 
- `~` - Means go back
- `1`- The number of versions

In case we want to go back multiple versions:

We start out by checking the log:

	git log

	These will be in opposite chronological order. Each change includes a hash, wich we can use to jump back into that version as well as the code modified.

From here we run:

	git reset *hash_value*

These changes still haven't been commited, if we want to go back to a version and have as the main one we run:

	git reset --hard *hash_value*


## Forking

This makes a complete copy of a repository.

We can copy other peoples projects and work on them. We can also share a version of our's with other people without having them changing our code.


**Notes&Issues**

Since the key i created wasnt prompt to adding an email address, I found a way to edit it:

	ssh-keygen -c -f ~/.ssh/id_rsa   


