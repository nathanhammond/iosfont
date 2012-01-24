# iosfont v0.0.3
**THIS SCRIPT IS NOT YET COMPLETE. IT DOES NOT YET DO EVERYTHING THE README ADVERTISES!**

iosfont is a script designed to make it easy to install and uninstall fonts on iOS devices.

## WARNING!
Before messing with any system files on iOS you should fully back up your iOS device. No, seriously! By using this code you acknowledge that I will not be held responsible for you willfully ignoring my warning and losing files. I may instead laugh at you for trusting code you found on the Internet to work!

Installing fonts that iOS doesn't know what to do with may put your iOS device into a respring loop. So far that has not been a problem as SSH has remained available. To fix this simply run ```iosfont revert [hostname]``` and wait for your device to recover.

## Dependencies
- POSIX Environment
- Python 2
- fontforge (http://fontforge.sourceforge.net/) (```brew install fontforge```)
- paramiko (http://www.lag.net/paramiko/) (```easy_install paramiko```)
- plutil (Preinstalled on OS X)
- Jailbroken iOS Device (http://www.iclarified.com/jailbreak/)
- OpenSSH installed on your iOS device (Anyone know a good link?)
- Netatalk installed on your iOS device (Anyone know a good link?)
- Your machine's SSH key stored on your iOS device (Anyone know a good link?)

## Installation
    wget https://raw.github.com/nathanhammond/iosfont/master/iosfont
    chmod +x iosfont
    mv iosfont /usr/local/bin/

## Usage
*You should use the .local address assigned to your phone (via Netatalk) as the hostname.*

```iosfont backup [hostname]```
Saves the current iOS font config files in ~/.iosfont/

```iosfont restore [hostname]```
Restores the default iOS font config files from ~/.iosfont/

```iosfont revert [hostname]```
Reverts the the most recent install operation, copying iOS font config files from ~/.iosfont/

```iosfont install [hostname] Roboto.ttf```
Install the font Roboto.ttf to your iPhone.

```iosfont install [hostname] Roboto*.ttf```
Shell expansion/multiple arguments work.

```iosfont uninstall [hostname] Roboto.ttf```
Remove the font Roboto.ttf from your iPhone.

```iosfont update```
Updates the iosfont script.

```iosfont version```
Returns the version of the iosfont script you are running.

## Miscellaneous
- This script was tested with Google's new Android font, Roboto. You can download Roboto from here: http://www.fontsquirrel.com/fonts/roboto
- This script has only been tested on OS X 10.6.8 and iOS 5.0.1. YMMV.
- This is the first time I've written more than ten lines of Python code in one sitting. Any Pythonistas out there may send me pull requests to show me how to do things in a more Pythonic way.
- Information sourced from these fine places:
  - http://www.enjoygadgets.com/blog/gadgets/2011/01/06/how-to-add-fonts-to-your-iphone/
  - http://www.typophile.com/node/81351
  - http://jessenoller.com/2009/02/05/ssh-programming-with-paramiko-completely-different/

## Support development of this library!
The time I have spent working on this library is non-trivial. However, instead of asking for donations, it seems a good fit to have referral links to places where you can buy fonts. You can support my development of this library by using these referral links when you purchase fonts or webfont services:
- [Fonts.com](http://www.kqzyfj.com/click-5625191-5765012 "Fonts.com referral link.")<img src="http://www.tqlkg.com/image-5625191-5765012" width="1" height="1" border="0"/>
- [ITCFonts.com](http://www.kqzyfj.com/click-5625191-5529320 "ITCFonts.com referral link.")<img src="http://www.tqlkg.com/image-5625191-5529320" width="1" height="1" border="0"/>
- [Linotype.com](http://www.kqzyfj.com/click-5625191-10532874 "Linotype.com referral link.")<img src="http://www.tqlkg.com/image-5625191-10532874" width="1" height="1" border="0"/>

## MIT License
Copyright (c) 2012 Nathan Hammond

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.