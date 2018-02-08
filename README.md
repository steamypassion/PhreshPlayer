# Phreshplayer

![PhreshPlayer logo](https://github.com/Phreshhh/phreshplayer/blob/master/app/img/phreshplayer-icon.png)  

Inspired by [mpv](https://mpv.io/) player (with old hud) - I'm really liked it.. :( and [DAUM PotPlayer](https://potplayer.daum.net/).

Developed using [GitHub's Electron](https://electronjs.org/).

**Keep It Simple!**

I'm sick of so much bullsh.t features in modern mediaplayers like kmp, vlc, etc.
Filters, useless view modes and more..

At last time I used PotPlayer but at this time is overhyped too.

The lot of extra features is it would be awesome, but finaly the program can't do that normally what it created first.
So I make my own..

I don't planning more features to the updates (exept audioTrack support/changes if will supported..), only neccessary bux fixes.

The Phresh media player is a simple and intuitive desktop app for Windows, Mac and Linux. It plays media files.. end of story.

In turn, I pays great attention to the naturality, easy and clear usage with much (and usual) keyboard shortcuts and some mouse gestures.

The player has an right click menu also for more powerful support the handling.

PhreshPlayer knows read the '.srt' subtitles also.

## A feature though!

Still I see today '.avi' and '.wmv' files, so..

.. if you drop an (or more) '.avi' or '.wmv' file into the player,
then convert files to '.mp4' automatically (and add it to playlist also automatically after conversion).

**WARNING! High CPU usage while coonverting. [FFmpeg](https://ffmpeg.org/)**

The conversion unfortunately work only Linux and Windows. As far as I know, not works on MacOS and the CPU limit works on Linux only.

### Supported file types
- mp4
- webm
- mkv (aac audio only. ac3 not, but you can convert to aac)
- m4v
- ogg (ogv)
- mov
- mp3
- flac

### Shortcuts

|key|action|
|---|---|
|l|toggle (show/hide) playlist|
|f|toggle fullscreen|
|enter|toggle fullscreen|
|esc|exit fullscreen|
|m|toggle mute|
|up|volume increase|
|down|volume decrease|
|left|seek -5 sec|
|right|seek +5 sec|
|p|previous video|
|b|previous video|
|n|next video|
|space|toggle play/pause|
|t|toggle always on top|
|q|quit|

### Mouse events

|event|action|
|---|---|
|mouse move|show controls (auto hide after 1 sec)|
|leave cursor on controls box|show controls (still visible)|
|left doubleclick|toggle fullscreen|
|scroll up|volume increase|
|scroll down|volume decrease|
|left click on progressbar|seek to the point|
|right click|menu open|

### File/Folder drops

|place|action|
|---|---|
|videoplayer area|clear actual playlist, and refill with the new files|
|playlist area|append files to the actual playlist|

The application can read folders also, but just 1 level deep:
- .
- ..
- Folder
  - Folder2
    - file level 3
  - file level 2
  - file2 level 2


- file  level 1
- file2 level 1

level 1 and level 2 files will append also to the playlist if you drop in at the same time, but  level 3 file in Folder2 won't.

### 'Sorry bro no mana..'

The electron (and the original too) Chromium/Chrome currently not support multi audio tracks in html 5 video players, so the language change unavilable yet in multi language videos.. :(

*Unfortunately I can't test on MacOS, so if you want better support for Mac, buy me a MacBook.. :D .. Or write to me the problems and deficiency what you found and i'll try to fix it.*

## Screenshots

![PhreshPlayer - Player](https://github.com/Phreshhh/phreshplayer/blob/master/screenshots/1_player-only.jpg)  
![PhreshPlayer - Player+Controlbox+Tooltip+Notify](https://github.com/Phreshhh/phreshplayer/blob/master/screenshots/2_player+controlbox+tooltip+toast.jpg)  
![PhreshPlayer - Playing video](https://github.com/Phreshhh/phreshplayer/blob/master/screenshots/3_play-video.jpg)  
![PhreshPlayer - Show subtitle](https://github.com/Phreshhh/phreshplayer/blob/master/screenshots/4_subtitles.jpg)   
![PhreshPlayer - Right click menu](https://github.com/Phreshhh/phreshplayer/blob/master/screenshots/5_rightclickmenu.jpg)   
![PhreshPlayer - Convert video (while playing other)](https://github.com/Phreshhh/phreshplayer/blob/master/screenshots/6_convert-while-playing.jpg)   
![PhreshPlayer - Still converting (after modal closed)](https://github.com/Phreshhh/phreshplayer/blob/master/screenshots/7_still-converting-after-close-modal.jpg)   
![PhreshPlayer - After conversion (auto add to playlist and) play the video](https://github.com/Phreshhh/phreshplayer/blob/master/screenshots/8_after-conversion-play-video.jpg)   

## Licence
Copyright (c) 2018, Krisztián Kis - Phresh-IT. All rights reserved.

Licensed under the [MIT](https://github.com/Phreshhh/phreshplayer/blob/master/LICENSE.md) License.

## Builds
[PhreshPlayer v1.0.0](https://github.com/Phreshhh/phreshplayer/releases/tag/v1.0.0)

## Web

[Phresh-IT](http://phresh-it.hu/)

[PhreshPlayer](http://phresh-it.hu/apps/phreshplayer/)

## Dev

Clone or download the repo and navigate in console to the program's root folder.

### Install

```
npm install
```

### Run

```
npm start
```

*Repair bindig error on startup. (if you got it, on Windows). Depency: Microsoft Visual C++ Build Tools 2015*

```
cd node_modules/win-mouse

node-gyp rebuild --target=1.7.9 --arch=x64 --dist-url="https://atom.io/download/atom-shell" --msvs_version=2015

cd ../../
```

### Build

```
npm run dist
```