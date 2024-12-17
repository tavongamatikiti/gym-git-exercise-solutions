# Gym Git Exercise Solutions

# Exercise 1

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
# Exercise 2

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
```
