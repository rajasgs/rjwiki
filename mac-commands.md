/ [Home](index.md)

## Title


Check brew services
```
	brew services list
```
		https://stackoverflow.com/questions/39397646/i-cannot-start-rabbitmq-on-my-mac


How to kill freezing apps?
	https://osxdaily.com/2012/03/02/force-quit-mac-apps/


```
ls -hal /tmp/abc
```

```
history 20
```
    - 20 recent searches


how to kill port / port kill / kill port:
```
netstat -vanp tcp | grep 3000
sudo lsof -i tcp:5432
kill 8787
or
lsof -t -i:8000
or
kill $(lsof -t -i:1090)
```
    https://stackoverflow.com/questions/3855127/find-and-kill-process-locking-port-3000-on-mac


```
kill python / pkill / pythonkill
	pkill -9 python
```


Show hidden files
```
Command + Shift + > 
```


```
cmd + d - vertical tab
cmd + shift +d - horizontal tab
```
    https://www.iterm2.com/documentation/2.1/documentation-one-page.html


Vox player
```
    downlowd the pref from here
    https://vox.rocks/mac-music-player/control-extension-download?fromplayer=1&vuid=ag-mac-0c1c38e7-fc01-4ec9-9655-a15fec268aea
    https://vox.rocks/forum/t/vox-media-buttons/6105
```



How to get the developer tools in Chrome on Mac / Dev tools / dev_tools chrome / 
```
Option + Command + i
```


multiple comments in VS code?
```
Command + /
```
https://stackoverflow.com/questions/45250088/how-can-i-comment-multiple-lines-in-visual-studio-code/45250111



Find Access ids
```
ps -A | grep -m1 BlueStack | awk '{print $1}'
ps -A | grep -m1 firefox | awk '{print $1}'
```



Screenshot:
```
Cmd + Shift + 3
	-> will be saved in your desktop
Command-Control-Shift-3
```
	https://www.itg.ias.edu/content/keyboard-shortcuts-capture-screen-shot-mac-os-x
	

Screenshot specific section to clipboard
```
Command-Control-Shift-4
```


Kill app in mac
```
Cmd + opt + esc and then kill 
```
	https://www.hongkiat.com/blog/force-quit-mac-app/
	


Open chrome
```
Opt + Command + J
```
	

Open multiple Eclipse instance / how to open multiple ecplise instance
```
cd /Applications/
open -n Eclipse1.app
open -n /Applications/Eclipse1.app
```
	https://stackoverflow.com/questions/118243/open-multiple-eclipse-workspaces-on-the-mac


```
du -sh *
```
	will get the folder and sizes
	

Find class file
```
find . -type f -name '*class'
```
	

Find and Delete
```
find . -type f -name '*html' -delete
```


find text in all files
```
grep -r 'some text' .
```
    https://superuser.com/questions/162999/how-to-find-files-with-certain-text-in-the-terminal

