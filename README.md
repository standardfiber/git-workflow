# Git WorkFlow

## Create Original Repo on GitHub (A)

## Clone Original Repo (A)

```
git clone https://github.com/A/some-repo.git
```

## Edit, Add, Commit, Push Cloned Project (A)

```
git add .
git commit -m "This is Some Repo"
git push
```

## Fork Original Repo on GitHub (B)

## Clone Forked Repo (B)

```
git clone https://some/B/repo.git
```

## Edit, Add, Commit, Push Cloned Project (B)

```
git add .
git commit -m "Some kind of updates on B"
git push
```

## Add a Remote and Sync

```
git remote add SRTS https://github.com/B/some-repo.git
git remote -v
git pull SRTS master
git push
```

## Remove a Remote if Needed

```
git remote rm SR
```
