## GNOME Shell Extension Radio
* Extension for listening to internet radio streams
* Supports GNOME Shell 3.18, 3.20 and 3.22 (older versions see releases)

![alt text](https://raw.githubusercontent.com/hslbck/gnome-shell-extension-radio/master/radio-extension.png)

### Installation
Prerequisites: GStreamer plugins are installed
##### Using gnome shell extension webpage
https://extensions.gnome.org/extension/836/internet-radio/
##### Arch Linux
Install [gnome-shell-extension-radio-git](https://aur.archlinux.org/packages/gnome-shell-extension-radio-git/) from [AUR](https://aur.archlinux.org).
##### Manual

You'll need the `glib-compile-schemas` and `msgfmt` commands on your system, available through `libglib` and `gettext`.

* Download source from github (clone repository or download zip)
* From the `gnome-shell-extension-radio` directory:
  * For a user only installation: `make && make install`
  * For a system-wide installation: `make && sudo make install DESTDIR=/`
* Reload the shell using X: Press `Alt+F2` write `r` and press `Enter`  
* Enable via GNOME Tweak Tool

### Features
* Manage radio station list
* Mark stations as favourites
* Middle click to start/stop last played station
* Cyrillic tag support (nielsrune): See below
* Support for multimedia keys
  * Play / Stop
  * Next / Prev cycles through the channels list (X4lldux)
* Support for title notification
* Search online radio directory https://www.radio-browser.info/ (https://github.com/hslbck/gnome-shell-extension-radio/issues/23)

### Charset convertion
Radio station streams may include tags (track artist and title).

If tags are not served in UTF-8 encoding, non-latin characters may be printed as garbage characters and must be converted to UTF-8 to make sense.

A specific source charset can optionally be set upon adding or editing each channel.
Unfortunately, charsets cannot be reliably determined automatically. Finding the right source charset for a channel's tags are therefore a matter of guessing (or guessing again). A tool like https://2cyr.com/decode/ may come useful.

Currently, this extension supports conversion of the following charsets:
* **windows-1251** (Russian, Bulgarian, Serbian Cyrillic, Macedonian)
* **koi8-r** (Russian)
* **koi8-u** (Ukrainian)

### Translation
* Open your source folder
* Run `make build` in your source directory
* The file `radio@hslbck.gmail.com.pot` should be created in the `po` folder

### Credits
nielsrune  
X4lldux  
zapashcanon  
morealaz  
##### Translations
Chinese: gmg137  
Danish: nielsrune   
French: narzb, BridouZ, thony8  
Hungarian: urbalazs  
Polish: pkomur  
Russian: stmc  
Turkish: marjinal1st  

### License
GNOME Shell Extension Radio  
Copyright (C) 2014 - 2017  hslbck

GNOME Shell Extension Radio is free software: you can redistribute it and/or modify it under the terms of the GNU General Public License as published by the Free Software Foundation, either version 3 of the License, or (at your option) any later version.

GNOME Shell Extension Radio is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the GNU General Public License for more details.

You should have received a copy of the GNU General Public License along with this program. If not, see <https://www.gnu.org/licenses/>.
