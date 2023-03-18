Creation of Repository (Step by Step)
1-   git init                           ->   initiate
2-  touch files.type                    ->   make dummy files as you want
we will put the files we want to upload in this repo :D 
3-  git status                          ->   reveal status of any files added or untracked existing on your repo (the file which we include all files in)
4- git add file.type                    ->   add file to be uploaded
5- git commit -m ""                     ->   message or comment your upload whatever changes you made
6- git remote add origin "link of repo" ->   linking with the remote repo which is on github 
Or git remote add origin "ssh link"     ->   but this requires to have public key for the project to access whatever you want without getting the link everytime
7- git push origin master               ->   push only to the master branch (which is the default) 
8- git push -u origin master            ->   pull and push to the ................................

IMPORTANT!!
Why do we use the 8th not the 7th?
-Because we will have conflict, if you upload only. As maybe someone on your team changed on the remote repo (github repo), therefore if you pushed only, the files pushed are older version of the repo. So, a conflict would happen and maybe lost in data may take place


Some Other Cmds to use
1- git clone "Repo Link"                ~>   clone a repo to your local device in the file you opened git bash with 
2- cd directory                         ~>   go to the specified directory you gave
3- mkdir namefile.type                  ~>  
4- git add filename.type                ~>   add files you want to upload
5- git add *                            ~>     add all files you included in your repo            
6- git reset head filename.type         ~>     remove an added file you want (unstage) 
7- git commit -m "any comment :>"       ~>     add a comment   
8- git status                           ~>     see Status of all added or untracked files on repo
9- git branch                           ~>     see branches of repo      

Forking:
Fork on github is someone who wants to modify your repo, therefore github makes him a new repo with files and name.

Pull Request:
Pull request is a request sent from someone who did fork your project and wants to upload to you to merge on it... 


Aliases (Abbreviation used instead of the actual real command to make it easier to write UwU)
1- git config --global alias.----- ______  ex: git config --global alias.st status  -----> Then simply you can use it as -> git st :>
2- git config --global alias.cm "commit -m"  ---> This is different as it has multiple words so we group it in quotations 


Branching: 
Branches are used mostly in large teams which probably could affect the master code, therefore branches are used

1- git branch                 -> list of branches made
2- git branch branchname      -> creates a branch named as branchname 
3- git checkout branchname    -> switches to the branch that you created which is called branchname
4- git branch -d branchname   -> deletes branch if only all changes had been added and committed from the branch
5- git branch -D branchname   -> deletes branch whatever you have put in that branch 
6- git checkout -b branchname -> creates a branch and switches to it named as branchname

stash:                                                (You could assign stash@{id} to any of them) 
1- git stash                  -> create stash to hide the files you did add
2- git stash pop              -> pops or gets the files preserved in the stash and deletes the stash (the previous used stash)
3- git stash pop stash@{id}   -> ................................................................... (for a specific one chosen)
4- git stash apply            -> gets the files preserved in the stash but doesn't delete the stash  (the previous used stash)
5- git stash apply stash@{id} -> ..................................................................  (for a specific one chosen)
6- git stash save "txt"       -> saves a message and assigned to the stash                           (the previous used stash)
7- git stash drop             -> delets the stash whatever files it contains                         
8- git stash show             -> shows the files included in the stash 
9- git stash clear            -> deletes all the stashes made 

Restore & Clean: (Switch from staged to unstaged files)
1- git restore --staged filename -> turns into untracked (unstaged)
2- git clean -n                  -> removes unstaged files but this will give you a warning or notification about what would be deleted first.. then follow up with the next cmd line to delete
3- git clean -f                  -> removes untracked files

Resetting Head:
1- git log                       -> gets log for all commits
2- git reset --hard hashcode     -> change head to the commit you selected by its hashcode
3- git push origin main --force  -> pushes with the new head assigned the commit you want to stop on :>

Quick Tip: To delete a recent commit you need to make Head pointing to the previous commit you want to keep 
Quick Tip: To exit log screen -----> Press Q

Ignoring Files & Directories   (Ignoring files you don't want to include in your repo or project in general)
1- touch .gitignore              -> makes a git file that should be coded by us and specify what we need to ignore while uploading
2- code .gitignore               -> brings up the IDE to code on :>

Explanation on Video on how to type syntax of ignoring files

3- git add -f filename           -> adds by 





For writing more faster with the git cmds -> use tap to continue any cmd

For git configuration
Get a list of all cmds related to config                      ~> git config -l
Get a list of all cmds related to config & its race and trace ~> git config -l --show-origin
Get a manual for all configurations                           ~> git help config



To authenticate that you are using your pc to github, there is something called public key
ssh-keygen -t rsa -b 4096 -C "your github email"
And Here there is a file created with your public key, therefore whenever you want to access on github, use it

ssh -T git@github.com -> access or authenticate that you are who has that public key ssh :>
then it will ask you to enter the passphrase (password)

                          
