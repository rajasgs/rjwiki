---
title: Ubuntu Commands
---

/ [Home](index.md)

# Ubuntu Commands



```
# 1

Show all libraries

dpkg -l

dpkg -l | grep "lintian"

dpkg --get-selections | grep postgres

dpkg --get-selections | grep lintian
```



```
# 2


Show local libraries
dpkg --get-selections | grep postgres
    https://askubuntu.com/questions/17823/how-to-list-all-installed-packages

```




```
# 3


Copy the installed libaries from one system to another:
dpkg --get-selections > list.txt

in the second system:
dpkg --clear-selections
sudo dpkg --set-selections < list.txt

https://askubuntu.com/questions/17823/how-to-list-all-installed-packages



```




```
# 4

lintian

lintian teams_1.5.00.23861_amd64.deb 


dpkg-deb: error: 'teams_1.5.00.23861_amd64.deb' is not a Debian format archive
Skipping teams_1.5.00.23861_amd64.deb: Non-zero status 2 from tar --wildcards -xO -f - *control:
tar: This does not look like a tar archive
tar: *control: Not found in archive
tar: Exiting with failure status due to previous errors
 at /usr/share/lintian/bin/../lib/Lintian/Processable/Installable.pm line 119.
	Lintian::Processable::Installable::init_from_file(Lintian::Processable::Installable=HASH(0x55e303f31fb8), "teams_1.5.00.23861_amd64.deb") called at /usr/bin/lintian line 762
	main::create_processable_from_file("teams_1.5.00.23861_amd64.deb") called at /usr/bin/lintian line 686
	eval {...} called at /usr/bin/lintian line 722

No packages selected.


```




```
# 5


How to install deb?

sudo dpkg -i teams_1.5.00.23861_amd64.deb 


```




```
# 


```




```
# 


```




```
# 


```




```
# 


```




```
# 


```




```
# 


```




```
# 


```




```
# 


```




```
# 


```




```
# 


```




```
# 


```




```
# 


```




```
# 


```




```
# 


```




```
# 


```




```
# 


```




```
# 


```




```
# 


```




```
# 


```




```
# 


```




```
# 


```




```
# 


```




```
# 


```




```
# 


```




```
# 


```




```
# 


```




```
# 


```




```
# 


```




```
# 


```




```
# 


```




```
# 


```




```
# 


```




```
# 


```




```
# 


```




```
# 


```




```
# 


```




```
# 


```




```
# 


```




```
# 


```




```
# 


```




```
# 


```




```
# 


```




```
# 


```




```
# 


```




```
# 


```




```
# 


```




```
# 


```




```
# 


```




```
# 


```




```
# 


```




```
# 


```




```
# 


```




```
# 


```




```
# 


```




```
# 


```




```
# 


```




```
# 


```




```
# 


```




```
# 


```




```
# 


```




```
# 


```




```
# 


```




```
# 


```




```
# 


```




```
# 


```




```
# 


```




```
# 


```




```
# 


```




```
# 


```




```
# 


```




```
# 


```




```
# 


```




```
# 


```




```
# 


```




```
# 


```




```
# 


```




```
# 


```




```
# 


```




```
# 


```




```
# 


```




```
# 


```




```
# 


```




```
# 


```




```
# 


```




```
# 


```




```
# 


```




```
# 


```



