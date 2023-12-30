---
title: Virtualenv Commands
---

/ [Home](index.md)

# Virtualenv Commands



### Basic Setup
```
mkdir /home/rajaraman/.virtualenv

pip install virtualenvwrapper

pip3 --version
  it should show like this:
  pip 20.0.2 from /usr/lib/python3/dist-packages/pip (python 3.8)

sudo pip install virtualenv

which virtualenv
	/usr/local/bin/virtualenv

sudo pip install virtualenvwrapper

ls /usr/local/bin/virtualenv
```


### Update this config in .zshrc or .bashrc
```
#Virtualenvwrapper settings:
export VIRTUALENVWRAPPER_PYTHON=/usr/bin/python3
export WORKON_HOME=$HOME/.virtualenv
export VIRTUALENVWRAPPER_VIRTUALENV=/usr/local/bin/virtualenv
source /usr/local/bin/virtualenvwrapper.sh
```

#### Ref :

  * [virtualenv-with-virtualenvwrapper-on-ubuntu-18-04](https://www.freecodecamp.org/news/virtualenv-with-virtualenvwrapper-on-ubuntu-18-04/)
  * [python-virtualenvwrapper](https://opensource.com/article/21/2/python-virtualenvwrapper)
  * [virtualenv-command-not-found](https://stackoverflow.com/questions/31133050/virtualenv-command-not-found)

  





