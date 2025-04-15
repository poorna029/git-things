# git basic commands 

## setting git account in vscode :

git config --global.user.name "username"
git config --global.user.email "username@gmail.com"

(default account) if you don't provide any git details these credentials will be used 

## using another git account for a project :
git config user.name "username1"
git config user.email "username1@gmail.com" 




## if you want to see git details :
on root folder 
>ls -a 
>cd .git
>ls           ( you will find all folders and files )
>cat config   ( for local git user details )

*** Head always points to latest commit on the branch 
Head -> (master)


1 . To check git version -> | git --v | git -version 
2 . To initialize .git folder we need to use -> | git init || git init folder_name
3 . To verify what is the git remote repo use -> | git remote -v 
4 . To add remote to local repo use -> | git remote add origin git-remote-repo-url
5 . To check current branch status use -> | git status

6 . To check git commits made so far (commit history) use -> | git log 
6.a To check git commits made so far (commit history in brief way) use -> |  git log --oneline (summary of our log statements with shortID)

7 . To get file tracked by git or to make files to staging area use -> | git add file1 file2 | git add . 

8 . To commit,is having set of changes till the point & have all changed content(repo) -> | git commit -m "commit message"
8.a To change commit message -> | git commit --amend -m "our modified msg here" *** Note : our commit id will change 
8.b If your commitID is 64e68ac3f0677e9ee3fb27217b83cc87b2ff8cd2 (first 7 characters make short commitID -> 64e68ac )
8.c we can move to any commit/version by going to particular commitID -> | git checkout commitID 
8.d to go to latest commit -> git checkout branch_name

9 . To undo changes in the unstaged changes use -> | git stash
10 . To apply changes to staging to undo git stash -> | git stash pop

11 . To undo to the previous n commit/s use -> | git reset HEAD~n (deault one) || git reset --mixed HEAD (both are same removing --mixed flag does'nt make any change that is default one, NO flag is default)(uncommits , but keeps code changes , doesn't stay in staging area)
11.a To revert to a commit -> | git revert commitID and (press ESC :wq) wq is write and quit (if you unfortunately deleted sth from previous commit and in current commit that is not present for that purpose)
***Note : by default commit message will be provided by git after revert, enter a  
11.b To uncommit to previous n commit/s use -> | git reset --soft HEAD~n (uncommits last n commits,but keeps code changes from last n commits , stays in staging area )
11.c To completely remove to previous n commit/s use -> | git reset --hard HEAD~n (uncommits last n commits, deletes code changes from last n commits)
***Note : very dangerous , as we cannot go back , all the code fron n commits will be permanently deleted 

12 . To discard commit process use -> | rm -Force .git/index.lock 
13 . To create a branch use -> | git branch branch-name | git checkout -b branch-name
14 . To relocate to a particular branch use -> | git checkout branch-name 
15 . To merge changes from a branch use -> | git merge branch-name
16 . To delete safely a branch use -> | git brnach -d  branch-name 
17 . To foreful delete a branch use -> | git branch -D branch-name
18 . To clone to a particular repo use -> | git clone remote-git-reop-url 
19 . To push changes to a remote reop -> | git push -u origin main  - (first time) | git push (next time)
20 . To check difference between current commit and changes after it -> | git diff 
21 . To get upto date with default branch use -> | git pull 

## To squash : Squash in Git means compressing multiple commits into one to make your Git history clean, readable, and meaningful.

22 . Tos squash -> | git rebase -i HEAD~5 (here 5 means combine/merge all recent 4 commits to the recent 5th commit) 
22.a  use (pick) for recent/last 5th commit  and rest all commits use squash for merging remaining 4  commits 

23 . To remove folder from tracked files use -> | git rm -r --cached folder_name/ (here -r is must for folder , -r is for recursively deleting files inside folder)
23.a To remove file from tracked files use -> |   git rm --cached file_name (here -r is not needed)


## To make git ignore files and folders create .gitignore file in root level 
in that .gitignore file just add folder or file names

for Folders:
suppose you have a folder called [api_keys]
in .gitignore file :
  add folder name like this :   api_keys/

for Files :
suppose you have a folder name [secret_logic.js]
in .gitignore file :
  add file name like this :   secret_logic.js 



    

 


