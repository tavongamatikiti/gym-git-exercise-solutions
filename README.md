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
```

