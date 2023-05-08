# Git-Basics
Basic readme file including all the essential commands of git

1)	Making a new directory			->	mkdir yashhh
2)	Know the current directory		->	pwd
3)	Change the directory			->	cd directory-name
4)	List all the files in current directory	->	ls
5)	List all hidden files in directory		->	ls -a
6)	Clone any existing repository		->	git clone “url”
7)	Status of changes in directory		->	git status
8)	Know the actual change made in file	->	git diff index.html
9)	Creating a new file in directory		->	touch yash.txt 
10)	Get the content of a file in directory        ->	cat yash.txt

// Directory means folder and Repository means converting that folder into a repo
// When we create a repo, a .git file is made that stores all the history of changes in that repo
// Staging Area , Unstaging Area
// Any code which needs to be commited should be present on staging area

11)	Add to staging area			->	git add index.html
12)	Add all files of directory to staging area  ->	git add .
13)	Removing file from staging area                ->	git restore --staged index.html
14)	Removing all the changes made                ->	git restore index.html
15)	Committing the changes done		->	git commit -m “index file changed”
16)	Get all the previous commits		->	git log
17)	Get specific number (e.g = 5) of logs        ->	git log -5
18)	Undo changes upto a particular commit  ->	git reset “desired-commit-hash-id”
19)	Undo last made commit & remove the change           ->      git reset --hard HEAD^
20)	Undo last made commit but keep the change             ->      git reset --soft "commit id of the commit present after the main commit"
21)	Send changes to backstage without committing         ->	  git stash      (first add them to stage by git add .  and then do git stash
22)	Bringing the backstaged changes back	->	git stash pop
23)	Clear all the backstaged changes	->	git stash clean

24)	Display all the branches                              ->	git branch
25)	Creating a new branch                                -> 	git branch NewBranch
26)	Shift to new branch                                     ->	git checkout NewBranch
27)	Create and shift to a  new branch             ->	git checkout -b YashBranch
28)	Deleting a branch                                         ->	git branch -d YashBranch    (first shift to other branch by git checkout master)
29)	Merge two branches                                   ->	git merge NewBranch

// Current branch will be displayed in green color
// To merge 2 branches...let's suppose in NewBranch we have made some changes...it means it is 1 step ahead of master 
// as it is now the file with latest code...so by remaining in this branch we cannot merge it with master
// Come out of this branch by...   git checkout master   and specifying which branch is to be merged with master...    git merge NewBranch
// Now Newbranch has been merged into master branch
// Branch where we have pulled the data is REMOTE BRANCH
// Branch on which we are working locally is LOCAL BRANCH
// One master branch is present on local pc and another master branch on remote 
// Now we need to push the data from local to remote

30)	Connect a repo to a directory		->	git remote add origin “url”
31)	Show all urls connected to a directory     ->	git remote -v

// ORIGIN can be understood as the name of the url
// Now to update / push the changes of the files into the repo we will push it and we need to tell where the changes needs to be pushed and to which branch

32)	Push changes to the repository		->	git push origin master 

// Now refreshing the repo will give us all the updated files
