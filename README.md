# Git Workflow

The goal of this project is to explain a basic Git workflow as I understand it. I will deal with 2 GitHub accounts for this explanation (**TechSnazzy (TS)** and **SanFrancisco (SF)**). And each of those accounts will have their own computer that will hold the cloned project folders. So for example, there will be **TS computer** and **SF computer**.

## Create a New Repository

- On TS GitHub, create a repo called: `git-workflow`.
- Then on the TS computer, create a project folder that contains `index.html` and `README.md`.
- **Note**: `index.html` should include a simple boilerplate just so that it contains something we can edit later.
- Initialize the project and push to GitHub.

```
cd <your_project_folder>
git init
git add .
git commit -m "First commit"
git push
git remote add origin https://github.com/TechSnazzy/git-workflow.git
git push -u origin master
```

## Fork and Clone Git Workflow Repo

- From SF GitHub account, fork the original repo so that SF has it's own copy of the repo.
- Then clone the repo to SF computer.

## Sync Your Fork with Original Repo

Note: This part I found on a (stackoverflow)[https://stackoverflow.com/questions/41283955/github-keeps-saying-this-branch-is-x-commits-ahead-y-commits-behind] thread.

From the Forked Clone on SF computer do this before anything else after the first clone.

```
https://github.com/TechSnazzy/git-workflow.git
```

## Edit, Add, Commit and Push your Project to the Forked Repo

```
git add .
git commit -m "Updated README to include Fork and Clone Git Workflow Repo instructions"
git push
```

<!-- ## Issue a Pull Request from Forked Repo to Original Repo

So now the SF repo is ahead by one commit. You now need to issue a pull request fromt eh SF repo to let it know that you've pushed your commits to the SF repo and that now the TS repo should pull those commits to it's own orignal repo. Does that make sense?

Then from the TS repo, you'll need to login and merge the pull request and then confirm that merge has completed. Once that is done, then the TS repo -->

## Sync Your Changes

```
git pull --rebase upstream master
git push --force-with-lease origin master
```
