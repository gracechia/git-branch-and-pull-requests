# Git Branch and Pull Requests

## Branches
Branching allows you to diverge from the main line of development and continue to do work and experiment without messing up the main line.

Git stores data as a series of snapshots, with pointers to versions of files. A branch is a lightweight pointer that refers to a particular commit.

The default branch name in Git is `master` or `main`. It's not special in any way other then it's automatically created when you use git commit. Most people don't bother to change it.

## Create a branch and switch to it
```
# This creates the branch and switches to it
git checkout -b my-branch
```

## Switching between branches
Switching branches changes the files in your working directory.
```
# Switching to master or main branch
git checkout master
```

```
# Switching to my-branch
git checkout my-branch
```

## Create a pull request
1. Create a branch called `feature-branch` and switch to it with `git checkout -b feature-branch`
2. Open file that you would like to make changes to. In this case, the file demonstrated here would be `model.py`
3. Write changes to `model.py` and save the file
4. `git add .` or `git add --patch` to add the changes in the working directory to the staging area
5. Commit the changes locally and write your commit message using `git commit -m "commit msg here"`
6. Push your branch to GitHub (remote repository) using `git push -u origin feature-branch`
7. Follow url and create a pull request

## Git & pull request practice
Pair Programming - 30 min

**Partner One**
* On GitHub, create a new public repo called `cold_day`
* Add your partner as a collaborator to the repo so they can write to it
* `git clone` this repo to your local machine and `cd` into it
* Create a branch called `line_one` and switch to it with `git checkout -b`
* Create a new file called `git_haiku.txt` and open it
* Write the first line of the Haiku, save it, then `git add` and `git commit` the changes locally
* Use `git push` to push changes to GitHub
* Follow GitHub url and `create a pull request`. Share the GitHub link to the pull request with Partner Two
* Switch to your `master` or `main` branch with `git checkout`

**Partner Two**
* Clone the repo using `git clone` and `cd` into it
* Run `git remote -v` to see the origin of this repo
* Open the GitHub link to the pull request that was created by Partner One. Check that Partner One has indeed added the first line of the Haiku and `merge pull request`
* `git pull` to get the latest updates to the `master` or `main` branch
* Create a branch called `line_two` and switch to it with git checkout -b
* Open `git_haiku.txt`
* Write the second line of the Haiku, save it, then `git add` and `git commit` the changes locally
* Use `git push` to push changes to GitHub
* Follow GitHub url and `create a pull request`. Share the GitHub link to the pull request with Partner Two
* Switch to your `master` or `main` branch with `git checkout`

**Partner One**
* Open the GitHub link to the pull request that was created by Partner Two. Check that Partner Two has indeed added the second line of the Haiku and `merge pull request`
* `git pull` to get the latest updates from Partner Two
* Repeat steps to add line_three and push back to the GitHub repo

**Partner Two**
* `git pull` to get a copy of the final Haiku

## Inspiration
```
An old silent pond...
A frog jumps into the pond,
splash! Silence again.

Basho Matsuo
```
Source: http://examples.yourdictionary.com/examples-of-haiku-poems.html
