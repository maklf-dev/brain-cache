## Commands:

- `pwd` : print working directory 
- `ls` : list
- `mkdir` : make directory
- `cd` : change directory
- `touch` : create new file
- `git init` : new Git repository (initialize)
- `git status` : files status
- `git add <file>` : moves fils into staging area
    - `git add .` : move every files to staging area
- `git rm --chached <file>` : remove file from staging area 
- `git commit` : saves snapshot into Git history
- `git commit -m ""` : saves a message into Git history
- `git log` : commit history
    - `git log --oneline` : short commit history
    - `git log --oneline --graph --decorate`: show a graphical design og commits and branches
    - `git log --oneline --graph --decorate -<int>` : show only the last \<int> commits
- `code .` : open current folder in VS Code
- `git diff` : exact changes in file
- `git remote add origin <url>` : connect local got project to online repo
- `git remote -v` : lists connected remote repo
- `git push -u origin main` : upload main branch to git repo
- `git branch -vv` : show local branches and their connected remote ones
- `git switch <branchName>` : switch to a new branch
    - `git switch -c <branchName>` : create and switch to a new branch
- `git branch` : list project branches
    - `git branch -d <branchName>` : remove branch
- `git merge <branchName>` : merge `<branchName>` with current branch
- `git pull` : gets the latest GitHub version and update local version with it
- `git restore` : discards unstaged changes
    - `git restore --staged <fileName>`: use it after staging, but before commit for recovery
- `git commit --amed -m "<newCommit>`: change the commit
- `git commit --amed --no-edit`: add the staged file into the previous commit whit the same message
- `git revert`
    - `git revert HEAD` : prev commit exists, but new commit cancels it
- `git reset`
    - `git reset --soft`
    - `git reset --mixed`
    -  __~~`git reset --hard`~~__
- __~~`git  clean --fd`~~__

## Terms:
- **Working Directory** : project main folder
- **Staging Area** : files that get tracked
- **Commit History** : changes history
- **Initialized/Reinitialized** : start a repository
- **Untracked** : file is NOT tracking by git
- **commit** : explanation about each checkpoint
- **modified** : has changed
- **remote** : online version of Git repo
- **fetch** : download/check from GitHub
- **push** : upload/send to GitHub
- **main** : the main and live version of your code
- **branch** : an stiky note that points at a version of main
- **head** : current location of you on the graph of main and branches
- **detached head** : when you go back and work on prev version of main, which has no branch
- **orphand commit** : when you commit on *detached head* , it commits point a no branch and eventually get garbage collected 
- **checkout** : moves head safely, without any changes. just movieng viewpoint
- **reset** : move main branch to point at specific commit. ahead commit still exist, but orphaned
    - **soft** : moves brnach, but staging area and wd stay unchanged. for when you want to combine commits into one
    - **mixed** : default; move branch and change staging area. for when you want to restage a commit diffrently; split it to multiple commit
    - **hard** : **DANGER ZONE!**; move branch, reset staging area, reset working directory. Uncommit work gone.
- **revert** : creats new commit and remove latest changes on that commit. actually you copy a version of your commit, before applieng changes to it
- **rebase** : when you have some branches and diffrent version, you have two choice:
    - **merge** : which merge all the the cahnges to final version and you have one final commit with all the changes
    - **rebase**: which copies all the commits in branch, add them a new parent (which is the final commit) and append them at the end of the line

- **reflog** : shows the latest activity of head. if commits are not garbage collected, you may be able to recover it. *(reachable commits last 90d and orphaned 30d)*


## Notes:
- *Git flow: edit -> status -> diff -> add -> commit -> branch -> merge -> push*
- **Do NOT run recovery commands on main branch**

## Explanations
- **main** : The live, final trusted version
- **other branches** : for work on something safely in project, without ruin the real version
    > when you want to add something to your project, you firts make a branch;then you change what ever you want on that version, without any harm to your real project when all your changes are done, and your test passed, you can safely merge that branch to main
- **issue** : a sticky note that says what task you are going to do
- **pull request (PR)** : for colleague/others/yourself to review changes before merge
    > `git pull` _is a git command for updating local version with GitHub Latest version. after merging a PR on GitHub, local version may still be old_

## Recovery States

| State | Tool |
| --- | --- | 
| not sure yet! | `git status` \| `git diff` \| `git log` | 
| file changed but not staged | `git restore` | 
| file staged but not commited | `git restore --staged` |
| file commited but not pushed | `git commit --amed -m "<newCommit>"` |
| file commited but need to add file to the same commit | `git commit --amed --no-edit` |
| file commited and push but need to recover | `git revert` |


### Sorces
- **📺 Git Will Finally Make Sense After This - LearnThatStack**
  - *https://www.youtube.com/watch?v=Ala6PHlYjmw*
- **📺 Git Tutorial For Dummies - Nick White**
  - *https://www.youtube.com/watch?v=mJ-qvsxPHpY*
- **🔗 md editor**
  - *https://md2file.com/editor/*

