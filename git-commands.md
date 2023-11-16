---
title: Git Commands
---

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
Find the parent branch: (buggy as well)
git for-each-ref --format='%(refname:short)' refs/heads/* | while read b; do if r=$(git config --get branch.$b.remote); then m=$(git config --get branch.$b.merge); echo "$b -> $r/${m##*/}"; fi; done

	https://blog.liplex.de/git-show-parent-branch/

```


```
Git Rebase
https://www.atlassian.com/git/tutorials/rewriting-history/git-rebase

```




```
git bi-sect
https://git-scm.com/docs/git-bisect

```


```
Git rebase vs git merge
https://stackoverflow.com/questions/804115/when-do-you-use-git-rebase-instead-of-git-merge


```




```
(HEAD detached from refs/heads/feat-product-apply-permission-K20-1382-new)
Not sure what does it mean
	https://loekvandenouweland.com/content/head-detached-from-origin-master.html
	
```


```
When should I git pull rebase
https://stackoverflow.com/questions/2472254/when-should-i-use-git-pull-rebase

```




```
merge vs pull
	git pull origin master
	is same as
		git fetch origin
		git merge origin/master
https://stackoverflow.com/questions/21756614/difference-between-git-merge-origin-master-and-git-pull

```


```
Merge another branch changes into mine
https://help.github.com/en/articles/merging-an-upstream-repository-into-your-fork


```




```
Show which files have been changed from another branch
git diff --name-status another_branch
git diff --name-status feat-product-apply-permission-K20-1382-latest
git diff --name-status p
	https://stackoverflow.com/questions/822811/showing-which-files-have-changed-between-two-revisions
```


```
delete a branch
git branch -D branch_name

or
git push -d <remote_name> <branchname>
$ git branch -d <branchname>
https://stackoverflow.com/questions/2003505/how-do-i-delete-a-git-branch-locally-and-remotely	
	
```




```
Git stash
git stash list 
	will list all stashes
	
git stash show
	

https://git-scm.com/docs/git-stash
https://www.koskila.net/how-to-list-your-git-stashes/

```


```
Show git username
git config user.name
git config --list
https://alvinalexander.com/git/git-show-change-username-email-address

```




```
View file in another branch
https://stackoverflow.com/questions/7856416/view-a-file-in-a-different-git-branch-without-changing-branches

```


```
Undo pushed commits
https://stackoverflow.com/questions/22682870/git-undo-pushed-commits

```




```
How to revoke last pushed commit?

```


```
Get the old check point
git checkout 85d29a6c0853f85303f87091efd8b3ac9ca69766
```




```
git add .
git commit -m "Last commit revoked"fa
git push origin HEAD:master -f

```


```
how to merge my branch to master in git?
git checkout master
git pull https://github.com/ORIGINAL_OWNER/ORIGINAL_REPOSITORY.git BRANCH_NAME
git push origin master

git push --set-upstream origin qa-current
git push --set-upstream origin feat-raja-one

branches:
* feat-raja-one
  master
  qa-current
  remotes/origin/feat-raja-one
  remotes/origin/master
  remotes/origin/qa-current
  
merge branch to qa-current
git pull
git checkout qa-current
git pull
git pull https://github.com/rajasgs/merge-test feat-raja-one
git push origin qa-current

https://help.github.com/en/github/collaborating-with-issues-and-pull-requests/merging-an-upstream-repository-into-your-fork

```




```

how to mirror github repo?
    
    git clone --bare https://github.com/KwikeeLabs/PrinterSpecsETL.git
    cd PrinterSpecsETL.git
    git push --mirror https://github.com/rajasgs/PrinterSpecsETLDec2019.git
    cd ..
    rm -rf PrinterSpecsETL.git
    
        https://github.com/KwikeeLabs/PrinterSpecsETL
    
        https://help.github.com/en/github/creating-cloning-and-archiving-repositories/duplicating-a-repository
```


```

git amend
git commit --amend -m "Message"

    https://www.atlassian.com/git/tutorials/rewriting-history



```




```
Git tags
git tag v1.0
git tag -a v1.1 -m "Second version"
git tag
git show v1.0
git tag -l "v1.*"
git push origin v1.0
git push origin --tags
git push --tags
git tag -d v1.0
git push origin -d v.10
git checkout tags/v1.0
git fetch --all
	more: https://www.youtube.com/watch?v=govmXpDGLpo
	https://stackoverflow.com/questions/35979642/what-is-git-tag-how-to-create-tags-how-to-checkout-git-remote-tags
	https://devconnected.com/how-to-delete-local-and-remote-tags-on-git/
	

```


```

git submodule add https://github.com/chaconinc/DbConnector
https://github.com/KwikeeDev/rest

git submodule add git@github.com:KwikeeDev/rest.git


```




```
Test ssh is setup for Github
	ssh -T git@github.com
	It should show like below
		Hi rajasgs! You've successfully authenticated, but GitHub does not provide shell access.
	
	ssh -T git@gitlab.com
	It should show like below
		Welcome to GitLab, @rajasyn101!
```


```
how to uncommit the previous commit before push + git

git reset HEAD~1
	https://www.cluemediator.com/undo-commit-before-push-in-git

```




```
git squash
	https://www.git-tower.com/learn/git/faq/git-squash/
	

```


```
Use github.com for multiple user accounts:

~/.ssh/config:

Host github.com-rajasgs
	HostName github.com
	User git
	IdentityFile ~/.ssh/id_rsa

Host github.com-csp
	HostName github.com
	User git
	IdentityFile ~/.ssh/id_rsa_csp
	

ssh-add ~/.ssh/id_rsa_csp

view agents:
ssh-add -L

https://gist.github.com/oanhnn/80a89405ab9023894df7

Verify:
ssh -T git@github.com-rajasgs
ssh -T git@github.com-csp

ssh -T git@github.com

git clone git@github.com-csp:org-account/company-project-repo.git


```




```
git branch -v
	* main 3c7b8ba Updates for 2022-12-13
```


```
git remote -v
origin	git@github.com:rajasgs/pandas-vs-pyspark-parquet-benchmarking.git (fetch)
origin	git@github.com:rajasgs/pandas-vs-pyspark-parquet-benchmarking.git (push)


```




```
git@gitlab.com:GladsonWorkspace/analytics/localstack-examples.git
cd localstack-examples
git remote add github git@github.com:rajasgs/localstack-examples.git
git push --mirror github

```


```

git subtree

	https://www.atlassian.com/git/tutorials/git-subtree
```




```
view all subtrees:
git log | grep git-subtree-dir | tr -d ' ' | cut -d ":" -f2 | sort | uniq
	
	https://stackoverflow.com/questions/16641057/how-can-i-list-the-git-subtrees-on-the-root


```


```
subrepos

https://github.com/ingydotnet/git-subrepo#benefits

```


