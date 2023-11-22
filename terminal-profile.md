---
title: Terminal Profile
---

/ [Home](index.md)

# Terminal Profile


```
sudo apt-get update
sudo apt-get -y install gconf2
```


```
dconf dump /org/gnome/terminal/ > gnome_terminal_settings_tact.txt
dconf load /org/gnome/terminal/ < gnome_terminal_settings_tact.txt
```

#### Ref :

  * [https://installati.one/install-gconf2-ubuntu-20-04/](https://installati.one/install-gconf2-ubuntu-20-04/)
  * []()
