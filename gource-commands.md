---
title: Gource commands
---

/ [Home](index.md)

# Gource commands



How to setup gource in Ubuntu?
```
sudo apt-get update
sudo apt-get -y install gource
sudo apt update
```

How to setup gource in Mac?
```
brew install gource
```

How to run?
```
cd ~/tact
mkdir gource-work
cd gource-work
git clone git@github.com:tactlabs/prettymetrics.git
cd prettymetrics

gource -1280x720 --seconds-per-day 1 -o - | ffmpeg -y -r 60 -f image2pipe -vcodec ppm -i - -vcodec libx264 -preset ultrafast -pix_fmt yuv420p -crf 1 -threads 0 -bf 0 prettymetrics.mp4
```

Public libraries:
[link](https://docs.google.com/spreadsheets/d/1yJqEM4q3Pw0QqbiAHQJ_AnrBL_-qWQpq-MpInVdoU1o/)


#### Ref :
  * [1](https://installati.one/install-gource-ubuntu-22-04/)
  * [2](https://formulae.brew.sh/formula/gource)
