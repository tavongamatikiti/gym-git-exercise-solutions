# Gym Git Exercise Solutions

# Bundle 1

## Exercise 1

```shell
~/IdeaProjects/the-gym/gym-git-exercise-solutions git:[master]
git init
Initialized empty Git repository in /Users/tavongamatikiti/IdeaProjects/the-gym/gym-git-exercise-solutions/.git/

~/IdeaProjects/the-gym/gym-git-exercise-solutions git:[master]
touch README.md

~/IdeaProjects/the-gym/gym-git-exercise-solutions git:[master]
git branch -M main
error: refname refs/heads/master not found
fatal: Branch rename failed

~/IdeaProjects/the-gym/gym-git-exercise-solutions git:[master]
git add ./

~/IdeaProjects/the-gym/gym-git-exercise-solutions git:[master]
git commit -m 'Initial commit'
[master (root-commit) d34eaba] Initial commit
 2 files changed, 63 insertions(+)
 create mode 100644 .idea/workspace.xml
 create mode 100644 README.md
 
~/IdeaProjects/the-gym/gym-git-exercise-solutions git:[master]
git branch -m main

~/IdeaProjects/the-gym/gym-git-exercise-solutions git:[main]
git remote add origin https://github.com/tavongamatikiti/gym-git-exercise-solutions.git

~/IdeaProjects/the-gym/gym-git-exercise-solutions git:[main]
git push -u origin main
Counting objects: 5, done.
Delta compression using up to 8 threads.
Compressing objects: 100% (3/3), done.
Writing objects: 100% (5/5), 1.42 KiB | 0 bytes/s, done.
Total 5 (delta 0), reused 0 (delta 0)
remote: To https://github.com/tavongamatikiti/gym-git-exercise-solutions.git
 * [new branch]      main -> main
Branch main set up to track remote branch main from origin.

~/IdeaProjects/the-gym/gym-git-exercise-solutions git:[main]
git checkout -b dev

Switched to a new branch 'dev'

~/IdeaProjects/the-gym/gym-git-exercise-solutions git:[dev]
git checkout -b test

Switched to a new branch 'test'

~/IdeaProjects/the-gym/gym-git-exercise-solutions git:[test]
git checkout dev

M       README.md
Switched to branch 'dev'

~/IdeaProjects/the-gym/gym-git-exercise-solutions git:[dev]
git branch -d test

Deleted branch test (was 447456c).
```
## Exercise 2

```shell
~/IdeaProjects/the-gym/gym-git-exercise-solutions git:[dev]
touch home.html

~/IdeaProjects/the-gym/gym-git-exercise-solutions git:[dev]
git add home.html

~/IdeaProjects/the-gym/gym-git-exercise-solutions git:[dev]
git stash save "Stash: home.html"

Saved working directory and index state On dev: Stash: home.html
HEAD is now at b74be49 Added dev branch and deleted test branch

~/IdeaProjects/the-gym/gym-git-exercise-solutions git:[dev]
touch about.html

~/IdeaProjects/the-gym/gym-git-exercise-solutions git:[dev]
git add about.html

~/IdeaProjects/the-gym/gym-git-exercise-solutions git:[dev]
git stash save "Stash: about.html"
Saved working directory and index state On dev: Stash: about.html
HEAD is now at b74be49 Added dev branch and deleted test branch

~/IdeaProjects/the-gym/gym-git-exercise-solutions git:[dev]
touch team.html

~/IdeaProjects/the-gym/gym-git-exercise-solutions git:[dev]
git add team.html

~/IdeaProjects/the-gym/gym-git-exercise-solutions git:[dev]
git stash save "Stash: Added team.html"
Saved working directory and index state On dev: Stash: Added team.html
HEAD is now at b74be49 Added dev branch and deleted test branch

~/IdeaProjects/the-gym/gym-git-exercise-solutions git:[dev]
git stash list

stash@{0}: On dev: Stash: Added team.html
stash@{1}: On dev: Stash: about.html
stash@{2}: On dev: Stash: home.html

~/IdeaProjects/the-gym/gym-git-exercise-solutions git:[dev]
git stash pop stash@{1}
On branch dev
Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)

        new file:   about.html

Dropped stash@{1} (58f45b50492000c31f0a90935a4e06dd8186bb5d)

~/IdeaProjects/the-gym/gym-git-exercise-solutions git:[dev]
git stash list
stash@{0}: On dev: Stash: Added team.html
stash@{1}: On dev: Stash: home.html

~/IdeaProjects/the-gym/gym-git-exercise-solutions git:[dev]
git stash pop stash@{1}
On branch dev
Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)

        new file:   about.html
        new file:   home.html

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git checkout -- <file>..." to discard changes in working directory)

        modified:   README.md

Dropped stash@{1} (a0be03e101fb93a788e9d76f75ec92ee4d516ee9)

~/IdeaProjects/the-gym/gym-git-exercise-solutions git:[dev]
git commit -m 'Created home.html, about.html and modified README.md for Exercise 2'
[dev 4ab0aa3] Created home.html, about.html and modified README.md for Exercise 2
 2 files changed, 19 insertions(+)
 create mode 100644 about.html
 create mode 100644 home.html
 
 ~/IdeaProjects/the-gym/gym-git-exercise-solutions git:[dev]
git push
fatal: The current branch dev has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin dev

~/IdeaProjects/the-gym/gym-git-exercise-solutions git:[dev]
 git push --set-upstream origin dev
Counting objects: 7, done.
Delta compression using up to 8 threads.
Compressing objects: 100% (7/7), done.
Writing objects: 100% (7/7), 942 bytes | 0 bytes/s, done.
Total 7 (delta 2), reused 0 (delta 0)
remote: Resolving deltas: 100% (2/2), completed with 1 local object.
remote: 
remote: Create a pull request for 'dev' on GitHub by visiting:
remote:      https://github.com/tavongamatikiti/gym-git-exercise-solutions/pull/new/dev
remote: 
To https://github.com/tavongamatikiti/gym-git-exercise-solutions.git
 * [new branch]      dev -> dev
Branch dev set up to track remote branch dev from origin.

~/IdeaProjects/the-gym/gym-git-exercise-solutions git:[dev]
git stash list
 
stash@{0}: On dev: Stash: Added team.html

~/IdeaProjects/the-gym/gym-git-exercise-solutions git:[dev]
git stash pop stash@{0}
On branch dev
Your branch is up-to-date with 'origin/dev'.
Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)

        new file:   team.html

Dropped stash@{0} (5222d0d641b70f122cc91a6e444069a48f8a892d)

~/IdeaProjects/the-gym/gym-git-exercise-solutions git:[dev]
git reset --hard HEAD
HEAD is now at 4ab0aa3 Created home.html, about.html and modified README.md for Exercise 2
```

# Bundle 2

## Exercise 1

```shell
~/IdeaProjects/the-gym/gym-git-exercise-solutions git:[dev]
git checkout main

Switched to branch 'main'
Your branch is up-to-date with 'origin/main'.

~/IdeaProjects/the-gym/gym-git-exercise-solutions git:[main]
git checkout -b ft/bundle-2
Switched to a new branch 'ft/bundle-2'

~/IdeaProjects/the-gym/gym-git-exercise-solutions git:[ft/bundle-2]
touch services.html

~/IdeaProjects/the-gym/gym-git-exercise-solutions git:[ft/bundle-2]
git add services.html

~/IdeaProjects/the-gym/gym-git-exercise-solutions git:[ft/bundle-2]
git commit -m "Add services.html page with initial content"
[ft/bundle-2 7116044] Add services.html page with initial content
 1 file changed, 12 insertions(+)
 create mode 100644 services.html
```

## Exercise 2

```shell
~/IdeaProjects/the-gym/gym-git-exercise-solutions git:[ft/bundle-2]
git checkout main
Switched to branch 'main'
Your branch is up-to-date with 'origin/main'.

~/IdeaProjects/the-gym/gym-git-exercise-solutions git:[main]
git pull origin main
remote: Enumerating objects: 1, done.
remote: Counting objects: 100% (1/1), done.
remote: Total 1 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
Unpacking objects: 100% (1/1), done.
From https://github.com/tavongamatikiti/gym-git-exercise-solutions
 * branch            main       -> FETCH_HEAD
   a498b2a..19d98ac  main       -> origin/main
Updating a498b2a..19d98ac
Fast-forward
 README.md     | 34 ++++++++++++++++++++++++++++++++--
 services.html | 12 ++++++++++++
 2 files changed, 44 insertions(+), 2 deletions(-)
 create mode 100644 services.html
 
 ~/IdeaProjects/the-gym/gym-git-exercise-solutions git:[main]
git checkout -b ft/service-redesign
M       README.md
Switched to a new branch 'ft/service-redesign'

~/IdeaProjects/the-gym/gym-git-exercise-solutions git:[ft/service-redesign]
git add services.html

~/IdeaProjects/the-gym/gym-git-exercise-solutions git:[ft/service-redesign]
git commit -m 'Added tagline on line 11'
[ft/service-redesign 4eaf515] Added tagline on line 11
 1 file changed, 1 insertion(+)
 
 ~/IdeaProjects/the-gym/gym-git-exercise-solutions git:[ft/service-redesign]
git push --set-upstream origin ft/service-redesign
Counting objects: 3, done.
Delta compression using up to 8 threads.
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 370 bytes | 0 bytes/s, done.
Total 3 (delta 2), reused 0 (delta 0)
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
remote: 
remote: Create a pull request for 'ft/service-redesign' on GitHub by visiting:
remote:      https://github.com/tavongamatikiti/gym-git-exercise-solutions/pull/new/ft/service-redesign
remote: 
To https://github.com/tavongamatikiti/gym-git-exercise-solutions.git
 * [new branch]      ft/service-redesign -> ft/service-redesign
Branch ft/service-redesign set up to track remote branch ft/service-redesign from origin.

~/IdeaProjects/the-gym/gym-git-exercise-solutions git:[ft/service-redesign]
git checkout main
Switched to branch 'main'
Your branch is up-to-date with 'origin/main'.

~/IdeaProjects/the-gym/gym-git-exercise-solutions git:[main]
git add services.html

~/IdeaProjects/the-gym/gym-git-exercise-solutions git:[main]
git commit -m 'Added p tag on line 11'
[main 1e37b4f] Added p tag on line 11
 1 file changed, 1 insertion(+)
 
 ~/IdeaProjects/the-gym/gym-git-exercise-solutions git:[main]
git push origin main
Counting objects: 6, done.
Delta compression using up to 8 threads.
Compressing objects: 100% (6/6), done.
Writing objects: 100% (6/6), 606 bytes | 0 bytes/s, done.
Total 6 (delta 4), reused 0 (delta 0)
remote: Resolving deltas: 100% (4/4), completed with 2 local objects.
To https://github.com/tavongamatikiti/gym-git-exercise-solutions.git
   19d98ac..38c4943  main -> main
   
~/IdeaProjects/the-gym/gym-git-exercise-solutions git:[main]
git checkout ft/service-redesign
Switched to branch 'ft/service-redesign'
Your branch is up-to-date with 'origin/ft/service-redesign'.

~/IdeaProjects/the-gym/gym-git-exercise-solutions git:[ft/service-redesign]
git diff main

diff --git a/services.html b/services.html
index db0e9ca..6794ba4 100644
--- a/services.html
+++ b/services.html
@@ -8,6 +8,6 @@
 <body>
     <h1>Our Services</h1>
     <p>Welcome to our services page. We offer a range of professional solutions tailored to your needs.</p>
-    <p>Welcome to our services page. Check out the changes!</p>
+    <p>We will be showing you list of what we offer to our customers</p>
 </body>
 </html>
 
 ~/IdeaProjects/the-gym/gym-git-exercise-solutions git:[ft/service-redesign]
git merge main

Updating 71ab696..6344f16
Fast-forward
 services.html | 2 +-
 1 file changed, 1 insertion(+), 1 deletion(-)


~/IdeaProjects/the-gym/gym-git-exercise-solutions git:[ft/service-redesign]
git push origin ft/service-redesign
Counting objects: 1, done.
Writing objects: 100% (1/1), 243 bytes | 0 bytes/s, done.
Total 1 (delta 0), reused 0 (delta 0)
remote: To https://github.com/tavongamatikiti/gym-git-exercise-solutions.git
   4eaf515..71ab696  ft/service-redesign -> ft/service-redesign
```

# Bundle 3

## Exercise 1

```shell
~/IdeaProjects/the-gym/gym-git-exercise-solutions git:[ft/service-redesign]
git checkout -b ft/team-page
Switched to a new branch 'ft/team-page'

~/IdeaProjects/the-gym/gym-git-exercise-solutions git:[ft/team-page]
touch team.html

~/IdeaProjects/the-gym/gym-git-exercise-solutions git:[ft/team-page]
git add team.html

~/IdeaProjects/the-gym/gym-git-exercise-solutions git:[ft/team-page]
git add team.html

~/IdeaProjects/the-gym/gym-git-exercise-solutions git:[ft/team-page]
git commit -m "Add team.html page with team introduction"

[ft/team-page 5354b69] Add team.html page with team introduction
 1 file changed, 12 insertions(+)
 create mode 100644 team.html
 
~/IdeaProjects/the-gym/gym-git-exercise-solutions git:[ft/team-page]
git push origin ft/team-page

Counting objects: 3, done.
Delta compression using up to 8 threads.
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 511 bytes | 0 bytes/s, done.
Total 3 (delta 1), reused 0 (delta 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote: 
remote: Create a pull request for 'ft/team-page' on GitHub by visiting:
remote:      https://github.com/tavongamatikiti/gym-git-exercise-solutions/pull/new/ft/team-page
remote: 
To https://github.com/tavongamatikiti/gym-git-exercise-solutions.git
 * [new branch]      ft/team-page -> ft/team-page
 
~/IdeaProjects/the-gym/gym-git-exercise-solutions git:[ft/team-page]
git checkout main
Switched to branch 'main'
Your branch is up-to-date with 'origin/main'.

~/IdeaProjects/the-gym/gym-git-exercise-solutions git:[main]
git checkout -b ft/contact-page
Switched to a new branch 'ft/contact-page'

~/IdeaProjects/the-gym/gym-git-exercise-solutions git:[ft/contact-page]
git checkout ft/team-page
Switched to branch 'ft/team-page'

~/IdeaProjects/the-gym/gym-git-exercise-solutions git:[ft/team-page]
git log 
commit 5354b699267af8de8ee72273c32b60f3124af245
Author: tavongamatikiti <tavongamatikiti@fgmail.com>
Date:   Tue Dec 17 15:10:27 2024 +0200

    Add team.html page with team introduction

commit 17bf33c37b829a3a018f071046f95f55f1238f99
Author: tavongamatikiti <tavongamatikiti@fgmail.com>
Date:   Tue Dec 17 15:06:10 2024 +0200

    Updated README for Exercise 2.2

commit 6344f16c7b9156d61ce472649c76add3e5fcc7fb
:
commit 5354b699267af8de8ee72273c32b60f3124af245
Author: tavongamatikiti <tavongamatikiti@fgmail.com>
Date:   Tue Dec 17 15:10:27 2024 +0200

    Add team.html page with team introduction

commit 17bf33c37b829a3a018f071046f95f55f1238f99
Author: tavongamatikiti <tavongamatikiti@fgmail.com>
Date:   Tue Dec 17 15:06:10 2024 +0200

    Updated README for Exercise 2.2

commit 6344f16c7b9156d61ce472649c76add3e5fcc7fb


~/IdeaProjects/the-gym/gym-git-exercise-solutions git:[ft/team-page]
git checkout ft/contact-page
Switched to branch 'ft/contact-page'

~/IdeaProjects/the-gym/gym-git-exercise-solutions git:[ft/contact-page]
git cherry-pick 5354b699267af8de8ee72273c32b60f3124af245
[ft/contact-page 4a5ee7f] Add team.html page with team introduction
 Date: Tue Dec 17 15:10:27 2024 +0200
 1 file changed, 12 insertions(+)
 create mode 100644 team.html

~/IdeaProjects/the-gym/gym-git-exercise-solutions git:[ft/contact-page]
git add contact.html

~/IdeaProjects/the-gym/gym-git-exercise-solutions git:[ft/contact-page]
git commit -m "Added contact.html page with contact details"
[ft/contact-page ed47fdb] Added contact.html page with contact details
 1 file changed, 13 insertions(+)
 create mode 100644 contact.html
 
~/IdeaProjects/the-gym/gym-git-exercise-solutions git:[ft/contact-page]
git push origin ft/contact-page
Counting objects: 6, done.
Delta compression using up to 8 threads.
Compressing objects: 100% (6/6), done.
Writing objects: 100% (6/6), 1.00 KiB | 0 bytes/s, done.
Total 6 (delta 1), reused 0 (delta 0)
remote: Resolving deltas: 100% (1/1), done.
remote: 
remote: Create a pull request for 'ft/contact-page' on GitHub by visiting:
remote:      https://github.com/tavongamatikiti/gym-git-exercise-solutions/pull/new/ft/contact-page
remote: 
To https://github.com/tavongamatikiti/gym-git-exercise-solutions.git
 * [new branch]      ft/contact-page -> ft/contact-page
 
~/IdeaProjects/the-gym/gym-git-exercise-solutions git:[ft/contact-page]
git checkout -b ft/faq-page
Switched to a new branch 'ft/faq-page'

~/IdeaProjects/the-gym/gym-git-exercise-solutions git:[ft/faq-page]
touch faq.html

~/IdeaProjects/the-gym/gym-git-exercise-solutions git:[ft/faq-page]
git add faq.html

~/IdeaProjects/the-gym/gym-git-exercise-solutions git:[ft/faq-page]
git commit -m "Add faq.html with FAQ content"

[ft/faq-page d63ee06] Add faq.html with FAQ content
 1 file changed, 15 insertions(+)
 create mode 100644 faq.html
 
~/IdeaProjects/the-gym/gym-git-exercise-solutions git:[ft/faq-page]
git push origin ft/faq-page

Counting objects: 3, done.
Delta compression using up to 8 threads.
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 534 bytes | 0 bytes/s, done.
Total 3 (delta 1), reused 0 (delta 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote: 
remote: Create a pull request for 'ft/faq-page' on GitHub by visiting:
remote:      https://github.com/tavongamatikiti/gym-git-exercise-solutions/pull/new/ft/faq-page
remote: 
To https://github.com/tavongamatikiti/gym-git-exercise-solutions.git
 * [new branch]      ft/faq-page -> ft/faq-page
 
~/IdeaProjects/the-gym/gym-git-exercise-solutions git:[ft/faq-page]
git checkout ft/team-page

Switched to branch 'ft/team-page'

~/IdeaProjects/the-gym/gym-git-exercise-solutions git:[ft/team-page]
git revert 5354b699267af8de8ee72273c32b60f3124af245
[ft/team-page db99423] Revert "Add team.html page with team introduction"
 1 file changed, 12 deletions(-)
 delete mode 100644 team.html

~/IdeaProjects/the-gym/gym-git-exercise-solutions git:[ft/team-page]
git push origin ft/team-page

Counting objects: 2, done.
Delta compression using up to 8 threads.
Compressing objects: 100% (2/2), done.
Writing objects: 100% (2/2), 267 bytes | 0 bytes/s, done.
Total 2 (delta 1), reused 0 (delta 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/tavongamatikiti/gym-git-exercise-solutions.git
   5354b69..db99423  ft/team-page -> ft/team-page
```
---

## Exercise 2

```shell
~/IdeaProjects/the-gym/gym-git-exercise-solutions git:[ft/faq-page]
git checkout -b ft/home-page-redesign
Switched to a new branch 'ft/home-page-redesign'

~/IdeaProjects/the-gym/gym-git-exercise-solutions git:[ft/home-page-redesign]
git checkout main

Switched to branch 'main'
Your branch is up-to-date with 'origin/main'.

~/IdeaProjects/the-gym/gym-git-exercise-solutions git:[main]
touch index.html

~/IdeaProjects/the-gym/gym-git-exercise-solutions git:[main]
git add index.html

~/IdeaProjects/the-gym/gym-git-exercise-solutions git:[main]
git commit -m 'Added home page content on main branch'
[main caec639] Added home page content on main branch
 1 file changed, 58 insertions(+)
 create mode 100644 index.html
 
~/IdeaProjects/the-gym/gym-git-exercise-solutions git:[main]
git push
Counting objects: 3, done.
Delta compression using up to 8 threads.
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 976 bytes | 0 bytes/s, done.
Total 3 (delta 0), reused 0 (delta 0)
remote: To https://github.com/tavongamatikiti/gym-git-exercise-solutions.git
   2352188..caec639  main -> main
   
~/IdeaProjects/the-gym/gym-git-exercise-solutions git:[main]
git checkout ft/home-page-redesign
Switched to branch 'ft/home-page-redesign'

~/IdeaProjects/the-gym/gym-git-exercise-solutions git:[ft/home-page-redesign]
git rebase origin/main

First, rewinding head to replay your work on top of it...
Applying: Add team.html page with team introduction
Applying: Added contact.html page with contact details
Applying: Add faq.html with FAQ content

~/IdeaProjects/the-gym/gym-git-exercise-solutions git:[ft/home-page-redesign]
git add index.html

~/IdeaProjects/the-gym/gym-git-exercise-solutions git:[ft/home-page-redesign]
git commit -m 'Added new line on 51'
[ft/home-page-redesign 2f396f1] Added new line on 51
 1 file changed, 1 insertion(+)
 
~/IdeaProjects/the-gym/gym-git-exercise-solutions git:[ft/home-page-redesign]
git push origin ft/home-page-redesign
Counting objects: 12, done.
Delta compression using up to 8 threads.
Compressing objects: 100% (12/12), done.
Writing objects: 100% (12/12), 1.77 KiB | 0 bytes/s, done.
Total 12 (delta 4), reused 0 (delta 0)
remote: Resolving deltas: 100% (4/4), completed with 1 local object.
remote: 
remote: Create a pull request for 'ft/home-page-redesign' on GitHub by visiting:
remote:      https://github.com/tavongamatikiti/gym-git-exercise-solutions/pull/new/ft/home-page-redesign
remote: 
To https://github.com/tavongamatikiti/gym-git-exercise-solutions.git
 * [new branch]      ft/home-page-redesign -> ft/home-page-redesign
```

# Bundle 4

## Exercise 1

```shell
~/IdeaProjects/the-gym/gym-git-exercise-solutions git:[ft/home-page-redesign]
git checkout main
Switched to branch 'main'
Your branch is up-to-date with 'origin/main'.

~/IdeaProjects/the-gym/gym-git-exercise-solutions git:[main]
git remote add git-copy https://github.com/tavongamatikiti/git-exercise-clone.git

~/IdeaProjects/the-gym/gym-git-exercise-solutions git:[main]
git remote
git-copy
origin

~/IdeaProjects/the-gym/gym-git-exercise-solutions git:[main]
git add index.html

~/IdeaProjects/the-gym/gym-git-exercise-solutions git:[main]
git commit -m 'New line on 51'
[main 6bfc680] New line on 51
 1 file changed, 1 insertion(+)
 
~/IdeaProjects/the-gym/gym-git-exercise-solutions git:[main]
git push origin main
Counting objects: 3, done.
Delta compression using up to 8 threads.
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 289 bytes | 0 bytes/s, done.
Total 3 (delta 2), reused 0 (delta 0)
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/tavongamatikiti/gym-git-exercise-solutions.git
   5bde690..6bfc680  main -> main
   
~/IdeaProjects/the-gym/gym-git-exercise-solutions git:[main]
git push git-copy
Counting objects: 53, done.
Delta compression using up to 8 threads.
Compressing objects: 100% (51/51), done.
Writing objects: 100% (53/53), 10.16 KiB | 0 bytes/s, done.
Total 53 (delta 20), reused 0 (delta 0)
remote: Resolving deltas: 100% (20/20), done.
To https://github.com/tavongamatikiti/git-exercise-clone.git
 * [new branch]      main -> main
 
 ~/IdeaProjects/the-gym/gym-git-exercise-solutions git:[ft/footer]
git checkout main
Switched to branch 'main'
Your branch is up-to-date with 'origin/main'.

~/IdeaProjects/the-gym/gym-git-exercise-solutions git:[main]
git checkout -b ft/squashing
M       README.md
Switched to a new branch 'ft/squashing'

~/IdeaProjects/the-gym/gym-git-exercise-solutions git:[ft/squashing]
git merge --squash ft/footer
Squash commit -- not updating HEAD
Automatic merge went well; stopped before committing as requested

~/IdeaProjects/the-gym/gym-git-exercise-solutions git:[ft/squashing]
git commit -m "footer changes squashing"
[ft/squashing 696086a] footer changes squashing
 1 file changed, 83 insertions(+)
 create mode 100644 footer.html
 
~/IdeaProjects/the-gym/gym-git-exercise-solutions git:[ft/squashing]
git push origin ft/squashing
Counting objects: 6, done.
Delta compression using up to 8 threads.
Compressing objects: 100% (6/6), done.
Writing objects: 100% (6/6), 1.56 KiB | 0 bytes/s, done.
Total 6 (delta 2), reused 0 (delta 0)
remote: Resolving deltas: 100% (2/2), completed with 1 local object.
remote: 
remote: Create a pull request for 'ft/squashing' on GitHub by visiting:
remote:      https://github.com/tavongamatikiti/gym-git-exercise-solutions/pull/new/ft/squashing
remote: 
To https://github.com/tavongamatikiti/gym-git-exercise-solutions.git
 * [new branch]      ft/squashing -> ft/squashing
```
