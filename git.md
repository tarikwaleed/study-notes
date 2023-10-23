# Cheat Sheet
- delete branch locally
`git branch -d localBranchName`
- delete branch remotely
`git push origin --delete remoteBranchName`
- refresh branch list
`git fetch -p`

- delete all branshes expect master
```shell
git branch | grep -v "master" | xargs git branch -D
```
- delete all branshes expect master and develop
```shell
git branch | grep -vE "master|develop" | xargs git branch -D
```
- show content of specific file in prevouis commits
```shell
git cat-file -p HEAD~4:registration/admin.py
git cat-file -p c22dd60:registration/admin.py
```

- rebase steps
```shell
on `feature_branch`
git rebase <main_branch>
git switch <main_branch>
git rebase <feature_branch>
```
- code review
```shell
git fetch
```


```shell
git switch -c feature/branch --track origin/feature/branch
```
**OR** using my fish alias
```shell
gt feature-xyz origin/feature-xyz
```
- to cherry-pick a specefic file from a specefic commit into your working directory
```shell
git checkout <commit_hash> -- /relative/path/to/file.py
```
- to undo the last commit
```shell
# Uncommit the changes
git reset --soft HEAD~1

# Completely delete the changes
git reset --hard HEAD~1

# then
git push origin -f
```



<h1 style="color:navy">Topics to understand</h1>
- [ ]  git worktree








