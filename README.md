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

## Bundle 3
### Exercise 1

```bash
GIS@mgrosz-lt MINGW64 ~/Documents/theGym/Git/git-exercise (main)  
$ git checkout -b ft/team-page
Switched to a new branch 'ft/team-page'
GIS@mgrosz-lt MINGW64 ~/Documents/theGym/Git/git-exercise (ft/team-page)
$ touch team.html && code team.html
GIS@mgrosz-lt MINGW64 ~/Documents/theGym/Git/git-exercise (ft/team-page)
$ git add team.html 

GIS@mgrosz-lt MINGW64 ~/Documents/theGym/Git/git-exercise (ft/team-page)
$ git commit -m "Add layout for team page"
[ft/team-page 4e972b9] Add layout for team page
 1 file changed, 24 insertions(+)
 create mode 100644 team.html
 GIS@mgrosz-lt MINGW64 ~/Documents/theGym/Git/git-exercise (ft/team-page) 
$ git push -u origin ft/team-page
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 569 bytes | 569.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.     
remote:
remote: Create a pull request for 'ft/team-page' on GitHub by visiting:  
remote:      https://github.com/Bateyjosue/git-exercise/pull/new/ft/team-page                                                                     page
remote:
To https://github.com/Bateyjosue/git-exercise.git
 * [new branch]      ft/team-page -> ft/team-page
branch 'ft/team-page' set up to track 'origin/ft/team-page'.
GIS@mgrosz-lt MINGW64 ~/Documents/theGym/Git/git-exercise (ft/team-page) 
$ git switch main
Switched to branch 'main'
M       README.md
Your branch is up to date with 'origin/main'.

GIS@mgrosz-lt MINGW64 ~/Documents/theGym/Git/git-exercise (main)
$ git checkout -b ft/contact-page
Switched to a new branch 'ft/contact-page'

GIS@mgrosz-lt MINGW64 ~/Documents/theGym/Git/git-exercise (ft/contact-page)
$ git switch ft/team-page 
Switched to branch 'ft/team-page'
M       README.md
Your branch is up to date with 'origin/ft/team-page'.

GIS@mgrosz-lt MINGW64 ~/Documents/theGym/Git/git-exercise (ft/team-page) 
$ git log
commit 4e972b90726bb81814361317cd9475125dc20715 (HEAD -> ft/team-page, origin/ft/team-page)
Author: Bateyjosue <josuebatey19@gmail.com>
Date:   Wed Jul 26 11:12:17 2023 +0200

    Add layout for team page

commit 1f2b7a2f3a169c1620e6732332c4fe8c136a5cec (origin/main, origin/HEAD)
Author: Bateyjosue <josuebatey19@gmail.com>
Date:   Wed Jul 26 11:01:20 2023 +0200

    Solve Bundle2 #Exercise2

commit bff0c5553029e02ebabce62d7988710081adea5e
Author: Bateyjosue <josuebatey19@gmail.com>
Date:   Tue Jul 25 11:54:05 2023 +0200

    Bundle 2 #Exercise 2


GIS@mgrosz-lt MINGW64 ~/Documents/theGym/Git/git-exercise (ft/team-page)
$ git switch ft/contact-page
Switched to branch 'ft/contact-page'
M       README.md

GIS@mgrosz-lt MINGW64 ~/Documents/theGym/Git/git-exercise (ft/contact-page)
$ git cherry-pick 4e972b90726bb81814361317cd9475125dc2071
[ft/contact-page 8ea6673] Add layout for team page
 Date: Wed Jul 26 11:12:17 2023 +0200
 1 file changed, 24 insertions(+)
 create mode 100644 team.html
 GIS@mgrosz-lt MINGW64 ~/Documents/theGym/Git/git-exercise (ft/contact-page)
$ touch contact.html && contact.html
bash: contact.html: command not found

GIS@mgrosz-lt MINGW64 ~/Documents/theGym/Git/git-exercise (ft/contact-page)
$ touch contact.html && code contact.html

GIS@mgrosz-lt MINGW64 ~/Documents/theGym/Git/git-exercise (ft/contact-page)
$ git add contact.html 

GIS@mgrosz-lt MINGW64 ~/Documents/theGym/Git/git-exercise (ft/contact-page)
$ git commit -m "Add contact Page and Layout "
[ft/contact-page b4612da] Add contact Page and Layout
 1 file changed, 25 insertions(+)
 create mode 100644 contact.html

GIS@mgrosz-lt MINGW64 ~/Documents/theGym/Git/git-exercise (ft/contact-page)
$ git push -u origin ft/contact-page 
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.    
Delta compression using up to 4 threads
Compressing objects: 100% (6/6), done.
Writing objects: 100% (6/6), 855 bytes | 427.00 KiB/s, done.
Total 6 (delta 3), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (3/3), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/contact-page' on GitHub by visiting:
remote:      https://github.com/Bateyjosue/git-exercise/pull/new/ft/contact-page     
remote:
To https://github.com/Bateyjosue/git-exercise.git
 * [new branch]      ft/contact-page -> ft/contact-page
branch 'ft/contact-page' set up to track 'origin/ft/contact-page'.
GIS@mgrosz-lt MINGW64 ~/Documents/theGym/Git/git-exercise (ft/contact-page)
$ git checkout -b ft/faq-page
Switched to a new branch 'ft/faq-page'

GIS@mgrosz-lt MINGW64 ~/Documents/theGym/Git/git-exercise (ft/faq-page)
$ touch faq.html && code faq.html

GIS@mgrosz-lt MINGW64 ~/Documents/theGym/Git/git-exercise (ft/faq-page)
$ git status
On branch ft/faq-page
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   README.md

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        faq.html

no changes added to commit (use "git add" and/or "git commit -a")

GIS@mgrosz-lt MINGW64 ~/Documents/theGym/Git/git-exercise (ft/faq-page)
$ git add faq.html 

GIS@mgrosz-lt MINGW64 ~/Documents/theGym/Git/git-exercise (ft/faq-page)
$ git commit -m 'Add faq page and layout'
[ft/faq-page e81782d] Add faq page and layout
 1 file changed, 26 insertions(+)
 create mode 100644 faq.html

GIS@mgrosz-lt MINGW64 ~/Documents/theGym/Git/git-exercise (ft/faq-page)
$ git push -u origin ft/faq-page
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 580 bytes | 580.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/faq-page' on GitHub by visiting:
remote:      https://github.com/Bateyjosue/git-exercise/pull/new/ft/faq-page
remote:
To https://github.com/Bateyjosue/git-exercise.git
 * [new branch]      ft/faq-page -> ft/faq-page
branch 'ft/faq-page' set up to track 'origin/ft/faq-page'.
GIS@mgrosz-lt MINGW64 ~/Documents/theGym/Git/git-exercise (ft/faq-page)
$ git revert 4e972b90726bb81814361317cd9475125dc2071
hint: Waiting for your editor to close the file... Vim: Error reading input, exiting...
Vim: Finished.
GIS@mgrosz-lt MINGW64 ~/Documents/theGym/Git/git-exercise (ft/faq-page)
$ git commit -m "Revert changes from team"
[ft/faq-page 9ecd6e2] Revert changes from team
 1 file changed, 24 deletions(-)
 delete mode 100644 team.html

GIS@mgrosz-lt MINGW64 ~/Documents/theGym/Git/git-exercise (ft/faq-page)
$ git push -u origin ft/faq-page
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Delta compression using up to 4 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (2/2), 230 bytes | 230.00 KiB/s, done.
Total 2 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/Bateyjosue/git-exercise.git
   e81782d..9ecd6e2  ft/faq-page -> ft/faq-page
branch 'ft/faq-page' set up to track 'origin/ft/faq-page'.
```

### Exercise 2

```bash
PS C:\Users\GIS\Documents\theGym\Git\git-exercise> git checkout -b ft/home-page-redesign
Switched to a new branch 'ft/home-page-redesign'
PS C:\Users\GIS\Documents\theGym\Git\git-exercise> 
GIS@mgrosz-lt MINGW64 ~/Documents/theGym/Git/git-exercise (ft/home-page-redesign)
$ git switch main
Switched to branch 'main'
Your branch is ahead of 'origin/main' by 1 commit.
  (use "git push" to publish your local commits)

GIS@mgrosz-lt MINGW64 ~/Documents/theGym/Git/git-exercise (main)
$ git add .

GIS@mgrosz-lt MINGW64 ~/Documents/theGym/Git/git-exercise (main)
$ git commit -m 'Update readme file'
[main 4c018cb] Update readme file
 1 file changed, 9 insertions(+) 
GIS@mgrosz-lt MINGW64 ~/Documents/theGym/Git/git-exercise (main)
$ git push
Enumerating objects: 11, done.
Counting objects: 100% (11/11), done.
Delta compression using up to 4 threads
Compressing objects: 100% (9/9), done.
Writing objects: 100% (9/9), 2.44 KiB | 625.00 KiB/s, done.
Total 9 (delta 3), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (3/3), completed with 1 local object.
To https://github.com/Bateyjosue/git-exercise.git
   1f2b7a2..766b8fd  main -> main

GIS@mgrosz-lt MINGW64 ~/Documents/theGym/Git/git-exercise (main)
$ git switch ft/home-page-redesign 
Switched to branch 'ft/home-page-redesign'

GIS@mgrosz-lt MINGW64 ~/Documents/theGym/Git/git-exercise (ft/home-page-redesign)
$ git rebase main
Successfully rebased and updated refs/heads/ft/home-page-redesign.
GIS@mgrosz-lt MINGW64 ~/Documents/theGym/Git/git-exercise (ft/home-page-redesign)
$ git add home.html 

GIS@mgrosz-lt MINGW64 ~/Documents/theGym/Git/git-exercise (ft/home-page-redesign)
$ git commit -m "Add main content to home page"
[ft/home-page-redesign 889b9a8] Add main content to home page
 1 file changed, 4 insertions(+)

GIS@mgrosz-lt MINGW64 ~/Documents/theGym/Git/git-exercise (ft/home-page-redesign)
$ git push
fatal: The current branch ft/home-page-redesign has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/home-page-redesign

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.

GIS@mgrosz-lt MINGW64 ~/Documents/theGym/Git/git-exercise (ft/home-page-redesign)                                                                         ig
$ git push -u origin ft/home-page-redesign
Enumerating objects: 16, done.
Counting objects: 100% (16/16), done.
Delta compression using up to 4 threads
Compressing objects: 100% (14/14), done.
Writing objects: 100% (14/14), 1.71 KiB | 583.00 KiB/s, done.
Total 14 (delta 7), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (7/7), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/home-page-redesign' on GitHub by visiting:                                                                          ng
remote:      https://github.com/Bateyjosue/git-exercise/pull/new/ft/home-page-redesign                                                                    -r
remote:
To https://github.com/Bateyjosue/git-exercise.git
 * [new branch]      ft/home-page-redesign -> ft/home-page-redesign
branch 'ft/home-page-redesign' set up to track 'origin/ft/home-page-redesign'.                                           
```

## Bundle 4
### Exercise 1

```bash
GIS@mgrosz-lt MINGW64 ~/Documents/theGym/Git/git-exercise (ft/home-page-redesign)
$ git switch main 
Switched to branch 'main'
M       README.md
Your branch is up to date with 'origin/main'.

GIS@mgrosz-lt MINGW64 ~/Documents/theGym/Git/git-exercise (main)
$ git status

GIS@mgrosz-lt MINGW64 ~/Documents/theGym/Git/git-exercise (main)
$ git remote -v
origin  https://github.com/Bateyjosue/git-exercise.git (fetch)
origin  https://github.com/Bateyjosue/git-exercise.git (push)

GIS@mgrosz-lt MINGW64 ~/Documents/theGym/Git/git-exercise (main)
$ git remote add git-copy https://github.com/Bateyjosue/git-exercise-copy.git

GIS@mgrosz-lt MINGW64 ~/Documents/theGym/Git/git-exercise (main)
$ git remote -v
git-copy        https://github.com/Bateyjosue/git-exercise-copy.git (fetch)  
git-copy        https://github.com/Bateyjosue/git-exercise-copy.git (push)   
origin  https://github.com/Bateyjosue/git-exercise.git (fetch)
origin  https://github.com/Bateyjosue/git-exercise.git (push)

GIS@mgrosz-lt MINGW64 ~/Documents/theGym/Git/git-exercise (main)
$ git status
On branch main
Your branch is up to date with 'origin/main'.

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   home.html

no changes added to commit (use "git add" and/or "git commit -a")

GIS@mgrosz-lt MINGW64 ~/Documents/theGym/Git/git-exercise (main)
$ git add .

GIS@mgrosz-lt MINGW64 ~/Documents/theGym/Git/git-exercise (main)
$ git commit -m "Add the link to the faq page"
[main a4210ed] Add the link to the faq page
 1 file changed, 2 insertions(+), 1 deletion(-)

GIS@mgrosz-lt MINGW64 ~/Documents/theGym/Git/git-exercise (main)
$ git remote set-url --add --push origin https://github.com/Bateyjosue/git-exercise.git

GIS@mgrosz-lt MINGW64 ~/Documents/theGym/Git/git-exercise (main)
$ git remote set-url --add --push origin https://github.com/Bateyjosue/git-exercise-copy.git

GIS@mgrosz-lt MINGW64 ~/Documents/theGym/Git/git-exercise (main)
$ git push -u origin main
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 312 bytes | 312.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.        
To https://github.com/Bateyjosue/git-exercise.git
   1d80f2e..a4210ed  main -> main
branch 'main' set up to track 'origin/main'.
Enumerating objects: 56, done.
Counting objects: 100% (56/56), done.
Delta compression using up to 4 threads
Compressing objects: 100% (43/43), done.
Writing objects: 100% (56/56), 11.63 KiB | 1.66 MiB/s, done.
Total 56 (delta 22), reused 25 (delta 9), pack-reused 0
remote: Resolving deltas: 100% (22/22), done.
To https://github.com/Bateyjosue/git-exercise-copy.git
 * [new branch]      main -> main
branch 'main' set up to track 'origin/main'.
```

### Exercise 2

```bash
GIS@mgrosz-lt MINGW64 ~/Documents/theGym/Git/git-exercise (main)
$ git checkout -m ft/footer
error: pathspec 'ft/footer' did not match any file(s) known to git

GIS@mgrosz-lt MINGW64 ~/Documents/theGym/Git/git-exercise (main)
$ git checkout -b ft/footer
Switched to a new branch 'ft/footer'

GIS@mgrosz-lt MINGW64 ~/Documents/theGym/Git/git-exercise (ft/footer)
$ code home.html 

GIS@mgrosz-lt MINGW64 ~/Documents/theGym/Git/git-exercise (ft/footer)
$ git statuts
git: 'statuts' is not a git command. See 'git --help'.

The most similar command is
        status

GIS@mgrosz-lt MINGW64 ~/Documents/theGym/Git/git-exercise (ft/footer)
$ git status
On branch ft/footer
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   home.html

no changes added to commit (use "git add" and/or "git commit -a")

GIS@mgrosz-lt MINGW64 ~/Documents/theGym/Git/git-exercise (ft/footer)
$ git add home.html 

GIS@mgrosz-lt MINGW64 ~/Documents/theGym/Git/git-exercise (ft/footer)
$ git commit -m "Add Footer Layou in home page"
[ft/footer 9aa42d0] Add Footer Layou in home page
 1 file changed, 7 insertions(+)

GIS@mgrosz-lt MINGW64 ~/Documents/theGym/Git/git-exercise (ft/footer)
$ code about.html 

GIS@mgrosz-lt MINGW64 ~/Documents/theGym/Git/git-exercise (ft/footer)
$ git status
On branch ft/footer
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)        
        modified:   about.html

no changes added to commit (use "git add" and/or "git commit -a")

GIS@mgrosz-lt MINGW64 ~/Documents/theGym/Git/git-exercise (ft/footer)
$ git add about.html 

GIS@mgrosz-lt MINGW64 ~/Documents/theGym/Git/git-exercise (ft/footer)
$ git commit -m "Design Footer Layout"
[ft/footer bf68ecc] Design Footer Layout
 1 file changed, 7 insertions(+)

GIS@mgrosz-lt MINGW64 ~/Documents/theGym/Git/git-exercise (ft/footer)
$ git status
On branch ft/footer
nothing to commit, working tree clean

GIS@mgrosz-lt MINGW64 ~/Documents/theGym/Git/git-exercise (ft/footer)
$ git push -u origin ft/footer 
Enumerating objects: 9, done.
Counting objects: 100% (9/9), done.
Delta compression using up to 4 threads
Compressing objects: 100% (6/6), done.
Writing objects: 100% (6/6), 748 bytes | 374.00 KiB/s, done.
Total 6 (delta 3), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (3/3), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/footer' on GitHub by visiting:
remote:      https://github.com/Bateyjosue/git-exercise/pull/new/ft/footer
remote:
To https://github.com/Bateyjosue/git-exercise.git
 * [new branch]      ft/footer -> ft/footer
branch 'ft/footer' set up to track 'origin/ft/footer'.
Enumerating objects: 9, done.
Counting objects: 100% (9/9), done.
Delta compression using up to 4 threads
Compressing objects: 100% (6/6), done.
Writing objects: 100% (6/6), 748 bytes | 249.00 KiB/s, done.
Total 6 (delta 3), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (3/3), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/footer' on GitHub by visiting:
remote:      https://github.com/Bateyjosue/git-exercise-copy/pull/new/ft/foote
remote:
To https://github.com/Bateyjosue/git-exercise-copy.git
 * [new branch]      ft/footer -> ft/footer
branch 'ft/footer' set up to track 'origin/ft/footer'.
GIS@mgrosz-lt MINGW64 ~/Documents/theGym/Git/git-exercise (ft/footer)
$ git switch main 
Switched to branch 'main'
M       README.md
Your branch is up to date with 'origin/main'.

GIS@mgrosz-lt MINGW64 ~/Documents/theGym/Git/git-exercise (main)
$ git checkout -b ft/squashing
Switched to a new branch 'ft/squashing'

GIS@mgrosz-lt MINGW64 ~/Documents/theGym/Git/git-exercise (ft/squashing)
$ git status
On branch ft/squashing
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   README.md

no changes added to commit (use "git add" and/or "git commit -a")

GIS@mgrosz-lt MINGW64 ~/Documents/theGym/Git/git-exercise (ft/squashing)
$ git merge --squash ft/footer
Updating 541d21d..bf68ecc
Fast-forward
Squash commit -- not updating HEAD
 about.html | 7 +++++++
 home.html  | 7 +++++++
 2 files changed, 14 insertions(+)

GIS@mgrosz-lt MINGW64 ~/Documents/theGym/Git/git-exercise (ft/squashing)
$ git status
On branch ft/squashing
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   about.html
        modified:   home.html

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   README.md


GIS@mgrosz-lt MINGW64 ~/Documents/theGym/Git/git-exercise (ft/squashing)
$ git commit -m "Footer changes squashing"
[ft/squashing 4877ef3] Footer changes squashing
 2 files changed, 14 insertions(+)
```