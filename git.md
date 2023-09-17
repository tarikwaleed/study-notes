# Cheat Sheet
## delete branch locally
`git branch -d localBranchName`
## delete branch remotely
`git push origin --delete remoteBranchName`
- refresh branch list
`git fetch -p`

## delete all branshes expect master
```shell
git branch | grep -v "master" | xargs git branch -D
```
## delete all branshes expect master and develop
```shell
git branch | grep -vE "master|develop" | xargs git branch -D
```
## show content of specific file in prevouis commits
```shell
git cat-file -p HEAD~4:registration/admin.py
git cat-file -p c22dd60:registration/admin.py
```

## rebase steps
```shell
on feature_branch
git rebase master
git switch master
git rebase feature_branch
```
## code review

```shell
git checkout --track feature-xyz origin/feature-xyz
```
**OR** using my fish alias
```shell
gt feature-xyz origin/feature-xyz
```







