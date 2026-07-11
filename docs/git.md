
**Settings to config once**

git config --global diff.tool vscode
git config --global difftool.vscode.cmd "code --wait --diff $LOCAL $REMOTE"
git config --global init.defaultBranch main 

git config --global core.autocrlf false
git config --global core.eol lf
git config --global core.safecrlf false

Confirm the above settings by git config --global -e 


**Overview commands**

- git log
- git log --oneline
- git log --oneline --reverse
- git status 
- git status -s
- git branch
- git reflog


- git remote 
- git remote -v
- git remote set-url origin <new-url> 
- Git remote add origin <url>
- Git remote rename oldname newname 
- Git remote remove (name) 
- Git push origin localbranch:remotebranch 
- git remote show <shortname> 


- Git branch
- Git branch <branchname> <hash> #To create a new branch pointing to that commit


- Git restore


- Git rebase
- Never rebase what you have already pushed 
- Only rebase local unpushed commits 


- Git merge


- Git ls-tree
- Git ls-tree (commitid) 


- Git ls-files


- Git rm


- Git mv


- Git show
- Git show (commitid) 
- Git show (commitid):file path 
- Git show (tree/blob id) 


- Git restore
- Git restore --source=commitid filename
- Git restore --staged filename


Git clean  
Git reset  
Git checkout  
Git switch  


Git revert  
Git revert creates a new commit that does the opposite of the previous commit  
If previous commit added 50 lines, revert will create new commit by removing those 50 lines  


Git stash  
git stash  
git stash pop  
git stash list  
git stash apply stash@{}  


Git commit --amend  
Git add -p  # For adding only a selected part from a file  


Workflow to change branch name and pushing to github  
git branch -m old-name new-name  
git push origin :old-name new-name  
git push -u origin new-name  


git remote set-url origin https://github.com/upstream/repo.git  
git remote set-url --push origin git@github.com:yourname/fork.git  



git push origin --delete tag v1.0  
git pull --rebase  
Git config global pull.rebase true  

git switch -c dev --track origin/dev  
git push origin --delete dev  
The command git branch name1 name2  
Creates new branch (or selects existing) name1, and points it to the commit name2  
-f flag for force  

