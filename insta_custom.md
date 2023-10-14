/ [Home](index.md)

# Insta Custom


Check whether you have conda env created
```
conda env list | grep "py311"

if this returns anything, you have py311 env created. 

if you don't get any results, run this command:
conda create -n py311 -y python=3.11
```

Activate conda
```
conda activate py311
```

```
pip show instaloader

it should show something like this:
  Name: instaloader
	Version: 4.10
	Summary: Download pictures (or videos) along with their captions and other metadata from Instagram.
	Home-page: https://instaloader.github.io/
	Author: Alexander Graf, André Koch-Kramer
	Author-email: mail@agraf.me, koch-kramer@web.de
	License: MIT
	Location: /opt/anaconda3/envs/py311/lib/python3.11/site-packages
	Requires: requests
	Required-by:

if no results, run this command:
pip install instaloader

Double check to make sure instaloader installed
```

Go to the base folder:
```
cd ~/tact

pwd
	it has to show something like this
	/Users/str-kwml0020/tact
```


If you haven't cloned the repo use this command:
```
git clone https://github.com/tactlabs/instaloader-custom
```

Go to the project folder
```
cd instaloader-custom
```

To collect data, run these commands:
```
# Collect all data
python custom.py <profile_name>

# Clean up after collecting data
python cleanup.py <profile_name>


Sample:
python custom.py judy.kim
python cleanup.py judy.kim
```