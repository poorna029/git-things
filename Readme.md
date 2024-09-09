# git basic commands 
1 . To check git version -> | git -v | git --version </br>
2 . To initialize .git folder we need to use -> | git init </br>
3 . To verify what is the git remote repo use -> | git remote -v </br>
4 . To add remote to local repo use -> | git remote add origin git-remote-repo-url </br>
5 . To check current branch status use -> | git status </br>
6 . To check git commit history use -> | git log </br>
7 . To get file tracked by git or to make files to staging area use -> | git add file1 file2 | git add .  </br>
8 . To commit,is having set of changes till the point & have all changed content(repo) | git commit -m "commit message" </br>
9 . To undo changes in the unstaged changes use -> | git stash </br>
10 . To apply changes to staging to undo git stash -> | git stash pop </br>
11 . To undo to the previous n commit/s use -> | git reset HEAD~n </br> 
12 . To discard commit process use -> | rm -Force .git/index.lock  </br>
13 . To create a branch use -> | git branch branch-name | git checkout -b branch-name </br>
14 . To relocate to a particular branch use -> | git checkout branch-name  </br>
15 . To merge changes from a branch use -> | git merge branch-name </br>
16 . To delete safely a branch use -> | git brnach -d  branch-name  </br>
17 . To foreful delete a branch use -> | git branch -D branch-name </br>
18 . To clone to a particular repo use -> | git clone remote-git-reop-url  </br>
19 . To push changes to a remote reop -> | git push -u origin main  - (first time) | git push (next time) </br>
20 . To check difference between current commit and changes after it -> | git diff  </br>
21 . To get upto date with default branch use -> | git pull </br>