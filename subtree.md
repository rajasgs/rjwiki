---
title: Subtree
---

/ [Home](index.md)

# Subrepo



```
Create a child repo:
Repo-A-ML-Utils
	git@github.com:rajasgs/repo-a-ml-utils.git

Create a parent repo:
Repo-B-Notebooks
	git@github.com:rajasgs/repo-b-notebooks.git

cd repo-b-notebooks
git subtree add --prefix mlutils git@github.com:rajasgs/repo-a-ml-utils.git master --squash

to pull all child repo updates in parent's repo:
git subtree pull --prefix mlutils git@github.com:rajasgs/repo-a-ml-utils.git master --squash
```

view subtrees:
```
code ~/.gitconfig

[alias]
    ls-subtrees = !git log --format=%b | awk '/git-subtree-dir/{ print $NF }' | sort --unique
```

#### Ref :

  * [git ls-subtrees](https://stackoverflow.com/questions/16641057/how-can-i-list-the-git-subtrees-on-the-root)

