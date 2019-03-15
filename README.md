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

## Fork and Clone Git Workflow Repo from TS to SF

- From SF GitHub account, fork the original repo so that SF has it's own copy of the repo.
- Then clone the repo to SF computer.

## Sync Your Fork with Original Repo

**Note**: This next part is based on some great advice I found in a (stackoverflow)[https://stackoverflow.com/questions/41283955/github-keeps-saying-this-branch-is-x-commits-ahead-y-commits-behind] thread.

From the Forked Clone, on the SF computer do this before anything else after you first clone it.

```
https://github.com/TechSnazzy/git-workflow.git
```

## Edit, Add, Commit and Push your Project to the Forked Repo

```
git add .
git commit -m "Updated README to include Fork and Clone Git Workflow Repo instructions"
git push
```

## Sync Your Changes

First, do a PR and then merge the changes. Once that is done, do this.

```
git pull --rebase upstream master
git push --force-with-lease origin master
```

## Summary

1. Create repo on TS.
2. Clone repo from TS repo to TS computer.
3. Fork repo from TS to SF.
4. Clone repo from Forked SF repo to SF computer.
5. Remote add TS upstream.
6. Add, commit, push edits.
7. From SF repo, submit a PR.
8. From TS repo, merge PR changes.
9. From SF computer, rebase.