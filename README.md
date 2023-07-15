# Git Exercises

## Bundle 1
### Exercise 1

```bash
➜  Excercise mkdir bundle-exercise
➜  Excercise cd bundle-exercise 
➜  bundle-exercise git init
hint: Using 'master' as the name for the initial branch. This default branch name
hint: is subject to change. To configure the initial branch name to use in all
hint: of your new repositories, which will suppress this warning, call:
hint: 
hint: 	git config --global init.defaultBranch <name>
hint: 
hint: Names commonly chosen instead of 'master' are 'main', 'trunk' and
hint: 'development'. The just-created branch can be renamed via this command:
hint: 
hint: 	git branch -m <name>
Initialized empty Git repository in /home/josuebatey/Documents/TheGym/Git/Excercise/bundle-exercise/.git/
➜  bundle-exercise git:(master) git branch -M main
➜  bundle-exercise git:(main) touch README.md
➜  bundle-exercise git:(main) ✗ git add .
➜  bundle-exercise git:(main) ✗ git commit -m "Add README.md file"
[main (root-commit) 5193683] Add README.md file
 1 file changed, 25 insertions(+)
 create mode 100644 README.md
➜  bundle-exercise git:(main) git remote add origin https://github.com/Bateyjosue/git-exercise.git
➜  bundle-exercise git:(main) git push -u origin main
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Delta compression using up to 4 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 653 bytes | 653.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/Bateyjosue/git-exercise.git
 * [new branch]      main -> main
Branch 'main' set up to track remote branch 'main' from 'origin'.
➜  bundle-exercise git:(main) 
➜  bundle-exercise git:(main) git checkout -b dev
Switched to a new branch 'dev'
➜  bundle-exercise git:(dev) ✗ git push -u origin dev 
Total 0 (delta 0), reused 0 (delta 0), pack-reused 0
remote: 
remote: Create a pull request for 'dev' on GitHub by visiting:
remote:      https://github.com/Bateyjosue/git-exercise/pull/new/dev
remote: 
To https://github.com/Bateyjosue/git-exercise.git
 * [new branch]      dev -> dev
Branch 'dev' set up to track remote branch 'dev' from 'origin'.
➜  bundle-exercise git:(dev) ✗ git checkout -b test
Switched to a new branch 'test'
➜  bundle-exercise git:(test) ✗ git push -u origin test
Total 0 (delta 0), reused 0 (delta 0), pack-reused 0
remote: 
remote: Create a pull request for 'test' on GitHub by visiting:
remote:      https://github.com/Bateyjosue/git-exercise/pull/new/test
remote: 
To https://github.com/Bateyjosue/git-exercise.git
 * [new branch]      test -> test
Branch 'test' set up to track remote branch 'test' from 'origin'.
➜  bundle-exercise git:(test) ✗ git switch dev 
M       README.md
Switched to branch 'dev'
Your branch is up to date with 'origin/dev'.
➜  bundle-exercise git:(dev) ✗ git push -u origin --delete test
To https://github.com/Bateyjosue/git-exercise.git
 - [deleted]         test
```

### Exercise 1
```bash
➜  bundle-exercise git:(dev) touch home.html && code home.html
➜  bundle-exercise git:(dev) ✗ git status
On branch dev
Your branch is up to date with 'origin/dev'.

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        home.html

nothing added to commit but untracked files present (use "git add" to track)

➜  bundle-exercise git:(dev) ✗ git add .
➜  bundle-exercise git:(dev) ✗ git stash
Saved working directory and index state WIP on dev: ab016c2 Bundle 1 | Exercise 1
➜  bundle-exercise git:(dev) git stash list
➜  bundle-exercise git:(dev) ✗ git add about.html 
➜  bundle-exercise git:(dev) ✗ git stash save "About"
Saved working directory and index state On dev: About
➜  bundle-exercise git:(dev) touch team.html
➜  bundle-exercise git:(dev) ✗ code team.html 
➜  bundle-exercise git:(dev) ✗ git status
On branch dev
Your branch is up to date with 'origin/dev'.

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        team.html

nothing added to commit but untracked files present (use "git add" to track)
➜  bundle-exercise git:(dev) ✗ git add .
➜  bundle-exercise git:(dev) ✗ git status
On branch dev
Your branch is up to date with 'origin/dev'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   team.html

➜  bundle-exercise git:(dev) ✗ git stash save "Team"
Saved working directory and index state On dev: Team

➜  bundle-exercise git:(dev) ✗ git stash list
➜  bundle-exercise git:(dev) ✗ git stash pop stash@{1}
On branch dev
Your branch is up to date with 'origin/dev'.

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   about.html

no changes added to commit (use "git add" and/or "git commit -a")
Dropped stash@{1} (9ef7b6742d23efdf967bfe42a2a3127c2cd99f45)
➜  bundle-exercise git:(dev) ✗ git stash list
➜  bundle-exercise git:(dev) ✗ git stash pop stash@{1}
On branch dev
Your branch is up to date with 'origin/dev'.

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   home.html

no changes added to commit (use "git add" and/or "git commit -a")
Dropped stash@{1} (9ef7b6742d23efdf967bfe42a2a3127c2cd99f45)
➜  bundle-exercise git:(dev) ✗ git add .
➜  bundle-exercise git:(dev) ✗ git commit -m "Restore Files about.html and home.html"
➜  bundle-exercise git:(dev) ✗ git push
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Delta compression using up to 4 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 653 bytes | 653.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/Bateyjosue/git-exercise.git
 * [new branch]      main -> dev
Branch 'dev' set up to track remote branch 'dev' from 'origin'.
➜  bundle-exercise git:(dev) ✗ git stash pop
On branch dev
Your branch is up to date with 'origin/dev'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   team.html

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   README.md

Dropped refs/stash@{0} (8a75b0b6f8f9fe620053a24afb56b4cd3936d57e)
➜  bundle-exercise git:(dev) ✗ git status
On branch dev
Your branch is up to date with 'origin/dev'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   team.html

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   README.md

➜  bundle-exercise git:(dev) ✗ git reset --hard
HEAD is now at 6e41833 Design the Bottom Section
➜  bundle-exercise git:(dev) ✗ 
```