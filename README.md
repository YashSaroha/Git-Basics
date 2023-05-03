# Git-Basics
Basic readme file including all the essential commands of git

1) Initialize an empty repository                   ->      git init
2) Know the current directory                       ->      pwd
3) Change the directory                             ->      cd
4) List all the files in current directory          ->      ls
5) Clone any existing repository                    ->      git clone "url"
6) Status of changes in directory                   ->      git status
7) Know the actual change made in a file            ->      git diff "changed-file-name"      like  git diff index.html
   Know what change is made                         ->      git show "commit-id"

Staging Area , Unstaging Area
Any code which needs to be commited should be present on staging area

8) Add to staging area                              ->      git add
9) Commiting the changes done                       ->      git commit -m *index file is changed*
10) Get all the previous commits                    ->      git log
11) Get specific number (e.g = 5) of logs           ->      git log -5
12) Display all the branches                        ->      git branch

Current branch will be displayed in green color

Creating a new branch                               ->      git branch NewBranch
Shift to new branch                                 ->      git checkout NewBranch , git checkout master
Create a new branch and shift to that branch        ->      git checkout -b YashBranch
Deleting a branch                                   ->      git branch -d YashBranch    (first shift to other branch by git checkout master)
Merge two branches                                  ->      git merge NewBranch

// To merge 2 branches...let's suppose in NewBranch we have made some changes...it means it is 1 step ahead of master as it is now the 
// file with latest code...so by remaining in this branch we cannot merge it with master
// Come out of this branch    ->    git checkout master
// Now specifying which branch is to be merged with master    ->    git merge NewBranch
// Now Newbranche has been merged into master branch

Undo last made commit & remove the change                         ->      git reset --hard HEAD^
Undo last made commit but keep the change           ->      git reset --soft "commit id of the commit present after the main commit"

// Branch where we have pulled the data is REMOTE BRANCH
// Branch on which we are working locally is LOCAL BRANCH
// One master branch is present on local pc and another master branch on remote 
// Now we need to push the data from local to remote

Removing file from staging area                     ->      git restore --staged index.html
Removing all the changes made                       ->      git restore index.html
