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

### Exercise 2
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

## Bundle 2
### Exercise 1

```bash
bundle-exercise git:(dev) git checkout -b ft/bundle-2
Switched to a new branch 'ft/bundle-2'
➜  bundle-exercise git:(ft/bundle-2) touch services.html && code services.html
➜  bundle-exercise git:(ft/bundle-2) ✗ git status
On branch ft/bundle-2
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        services.html

nothing added to commit but untracked files present (use "git add" to track)
➜  bundle-exercise git:(ft/bundle-2) ✗ git add .
➜  bundle-exercise git:(ft/bundle-2) ✗ git commit -m "Add File services.html"
[ft/bundle-2 582629d] Add File services.html
 1 file changed, 21 insertions(+)
 create mode 100644 services.html
➜  bundle-exercise git:(ft/bundle-2) git push
fatal: The current branch ft/bundle-2 has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/bundle-2

➜  bundle-exercise git:(ft/bundle-2) git push -u origin ft/bundle-2 
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 548 bytes | 548.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote: 
remote: Create a pull request for 'ft/bundle-2' on GitHub by visiting:
remote:      https://github.com/Bateyjosue/git-exercise/pull/new/ft/bundle-2
remote: 
To https://github.com/Bateyjosue/git-exercise.git
 * [new branch]      ft/bundle-2 -> ft/bundle-2
Branch 'ft/bundle-2' set up to track remote branch 'ft/bundle-2' from 'origin'.
➜  bundle-exercise git:(ft/bundle-2) 
```

### Exercise 2

```bash
$ git switch main
Already on 'main'
Your branch is up to date with 'origin/main'.

GIS@mgrosz-lt MINGW64 ~/Documents/theGym/Git/git-exercise (main)
$ git pull origin main
From https://github.com/Bateyjosue/git-exercise
 * branch            main       -> FETCH_HEAD
Already up to date.

GIS@mgrosz-lt MINGW64 ~/Documents/theGym/Git/git-exercise (main)
$ git checkout -b ft/service-redesign
Switched to a new branch 'ft/service-redesign'

GIS@mgrosz-lt MINGW64 ~/Documents/theGym/Git/git-exercise (ft/service-redesign)
$ code services.html 

GIS@mgrosz-lt MINGW64 ~/Documents/theGym/Git/git-exercise (ft/service-redesign)
$ git status
On branch ft/service-redesign
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   README.md
        modified:   services.html

no changes added to commit (use "git add" and/or "git commit -a")
$ git switch main 
Switched to branch 'main'
M       README.md
Your branch is up to date with 'origin/main'.

GIS@mgrosz-lt MINGW64 ~/Documents/theGym/Git/git-exercise (main)
$ git add services.html 

GIS@mgrosz-lt MINGW64 ~/Documents/theGym/Git/git-exercise (main)
$ git commit -m "Change title of the sercise card"
[main 9564f6a] Change title of the sercise card
 1 file changed, 3 insertions(+)

GIS@mgrosz-lt MINGW64 ~/Documents/theGym/Git/git-exercise (main)
$ git push 
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 350 bytes | 350.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/Bateyjosue/git-exercise.git
   701c297..9564f6a  main -> main
   GIS@mgrosz-lt MINGW64 ~/Documents/theGym/Git/git-exercise (main)
$ git switch ft/service-redesign 
Switched to branch 'ft/service-redesign'
M       README.md
Your branch is up to date with 'origin/ft/service-redesign'.

GIS@mgrosz-lt MINGW64 ~/Documents/theGym/Git/git-exercise (ft/service-redesign)
$ git diff main
diff --git a/services.html b/services.html
index 0c1d064..c93580d 100644
--- a/services.html
+++ b/services.html
@@ -18,7 +18,7 @@
         </nav>
     </header>
     <main>
-        <h1>Services Offer</h1>
+        <h1>Services</h1>
     </main>
 </body>
 </html>
\ No newline at end of file
GIS@mgrosz-lt MINGW64 ~/Documents/theGym/Git/git-exercise (ft/service-redesign)
$ git merge main
Auto-merging services.html
CONFLICT (content): Merge conflict in services.html
Automatic merge failed; fix conflicts and then commit the result.

GIS@mgrosz-lt MINGW64 ~/Documents/theGym/Git/git-exercise (ft/service-redesign|MERGING)
$ git add services.html 

GIS@mgrosz-lt MINGW64 ~/Documents/theGym/Git/git-exercise (ft/service-redesign|MERGING)
$ git commit -m "Fix Merge Conflict"
[ft/service-redesign dc463c8] Fix Merge Conflict
GIS@mgrosz-lt MINGW64 ~/Documents/theGym/Git/git-exercise (ft/service-redesign)
$ git push
Enumerating objects: 1, done.
Counting objects: 100% (1/1), done.
Writing objects: 100% (1/1), 222 bytes | 222.00 KiB/s, done.
Total 1 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/Bateyjosue/git-exercise.git
   ddb53dd..dc463c8  ft/service-redesign -> ft/service-redesign
```