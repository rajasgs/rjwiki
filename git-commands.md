/ [Home](index.md)

# Git Commands



```
git pull from fork parent




https://github.com/rjsgstest/git-test-sgstest
https://github.com/rajasgs/git-test



git remote add upstream git@github.com:rajasgs/git-test.git
git fetch upstream
git merge upstream/master
git pull upstream main
git push

https://stackoverflow.com/questions/13828230/pulling-changes-from-fork-parent-in-git


```




```
check available remote


git remote

git remote -v


git branch -r

git branch -l

https://stackoverflow.com/questions/10183724/list-of-remotes-for-a-git-repository





https://www.git-tower.com/learn/git/commands/git-remote/


https://stackoverflow.com/questions/73297514/fastest-way-to-check-if-a-git-server-is-available

```



```
force commit the file even thought it is .gitignore  + git add


git add --force batch/job_defs/modeltrain/resource_files/jars/rner.jar



https://stackoverflow.com/questions/8006393/force-add-despite-the-gitignore-file


```




```

how to install/upgrade in mac?
brew upgrade git
```


```
get all commits
git rev-list --all --pretty=oneline
https://stackoverflow.com/questions/1314950/git-get-all-commits-and-blobs-they-created


```




```
git init --initial-branch=main
	https://docs.github.com/en/repositories/configuring-branches-and-merges-in-your-repository/managing-branches-in-your-repository/changing-the-default-branch


```


```
how to cherry pick
git checkout p (target branch)
git cherry-pick <commit_id>
```




```
Check diff
https://stackoverflow.com/questions/436362/how-to-diff-a-commit-with-its-parent/449128#449128

```


```
How to find the parent branch?
git parent
https://stackoverflow.com/questions/3161204/find-the-parent-branch-of-a-git-branch


```




```
When did I create a branch?
git reflog --date=local
	8507e41 (HEAD -> dev, origin/dev) HEAD@{Wed Aug 10 15:09:28 2022}: commit: Bannerads runner added
	925da0f HEAD@{Wed Aug 10 15:08:05 2022}: checkout: moving from Docker-etl-dev to dev
	72a849c (origin/Docker-etl-dev, Docker-etl-dev) HEAD@{Wed Aug 10 15:07:08 2022}: reset: moving to HEAD
	72a849c (origin/Docker-etl-dev, Docker-etl-dev) HEAD@{Wed Aug 10 13:02:52 2022}: pull: Fast-forward
	1905c81 HEAD@{Wed Aug 10 13:02:48 2022}: checkout: moving from dev to Docker-etl-dev
	925da0f HEAD@{Wed Aug 10 13:02:21 2022}: commit: limtedinventory issue fixed on link_mapped
	0cbf7eb HEAD@{Wed Aug 10 13:00:23 2022}: checkout: moving from Docker-etl-dev to dev

git reflog --date=local dev
git reflog --date=local Docker-etl-dev
	https://stackoverflow.com/questions/2255416/how-to-determine-when-a-git-branch-was-created

	https://stackoverflow.com/questions/42811432/how-to-go-back-to-the-previous-master-branch
	

```


```
Create a branch from another branch
git checkout -b myfeature dev
https://stackoverflow.com/questions/4470523/create-a-branch-in-git-from-another-branch


```




```
How to rename a branch name?
https://stackoverflow.com/questions/6591213/how-do-i-rename-a-local-git-branch

```


```
Git diff and apply
git diff new-feature..new-feature2 | git apply -
```




```

```


```

```




```

```


```

```




```

```


```

```




```

```


```

```




```

```


```

```




```

```


```

```




```

```


```

```




```

```


```

```




```

```


```

```




```

```


```

```




```

```


```

```




```

```


```

```




```

```


```

```




```

```


```

```




```

```


```

```




```

```


```

```




```

```


```

```




```

```


```

```




```

```


```

```




```

```


```

```




```

```


```

```




```

```


```

```




```

```


```

```




```

```


```

```




```

```


```

```




```

```


```

```




```

```


```

```




```

```


```

```




```

```


```

```




```

```


```

```




```

```


```

```




```

```


```

```




```

```


```

```




```

```


```

```




```

```


```

```




```

```


```

```




```

```


```

```




```

```


```

```




```

```


```

```




```

```


```

```




```

```


```

```




```

```


```

```




```

```


```

```




```

```


```

```




```

```


```

```




```

```


```

```




```

```


```

```




```

```


```

```




```

```


```

```




```

```


```

```




```

```


```

```




```

```


```

```




```

```


```

```




```

```


```

```




```

```


```

```




```

```


```

```




```

```


```

```




```

```


```

```




```

```


```

```




```

```


```

```




```

```


```

```




```

```


```

```




```

```


```

```




```

```


```

```




```

```


```

```




```

```


```

```




```

```


```

```




```

```


```

```




```

```


```

```




```

```


```

```




```

```


```

```




```

```


```

```




```

```


```

```




```

```


```

```




```

```


```

```




```

```


```

```




```

```


```

```




```

```


```

```




```

```


```

```




```

```


```

```




```

```


```

```




```

```


```

```




```

```


```

```




```

```


```

```




```

```


```

```




```

```


```

```




```

```


```

```




```

```


```

```




```

```


```

```




```

```


```

```




```

```


```

```




```

```


```

```




```

```


```

```




```

```


```

```




```

```


```

```




```

```


```

```




```

```


```

```




```

```


```

```




```

```


```

```




```

```


```

```




```

```


```

```




```

```


```

```




```

```


```

```




```

```


```

```




```

```


```

```




```

```


```

```




```

```


```

```




```

```


```

```




```

```


```

```




```

```


```

```




```

```


```

```




```

```


```

```




```

```

