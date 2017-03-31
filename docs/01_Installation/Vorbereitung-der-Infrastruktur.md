# Vorbereitung der Infrastruktur

## Allgemeines 
Für die Verwendung des Factfinders sollen und werden keine zusätzlichen Tools benötigt, da er in die Shop Logic eingebunden wird.

## Systemanforderungen 
Im folgenden werden in Kurzform die benötigten Komponenten aufgeführt:

* Benötigte Shop Komponenten
    * Core mit einer Version > 5.5.62
    * XS-Studio mit einer Version > 1.2.62

Bower wird mit NPM installiert:
`npm install -g bower`

![Auswahl der Optionen](https://c1.staticflickr.com/9/8735/17155976651_3a2946f5ac_b.jpg)

## Probleme / FAQ

### Chromium + Flash Plugin Problem
Bei der Verwendung des Chromium Browsers auf Ubuntu muss ggf. das Flash Plugin manuell nachinstalliert werden. Dies kann man an folgender Meldung erkennen:

![Plugin not supported](http://techhelpkb.com/wp-content/uploads/2015/04/java-plug-in-not-supported.png)

Problemlösungsseiten:
* [askubuntu.com](http://askubuntu.com/questions/449103/chromium-34-and-later-cannot-detect-flash-plugin)
* [itsfoss.com](http://itsfoss.com/fix-flash-player-issue-chromium-in-ubuntu-14-04/)

ggf. müssen die benötigten Bibliotheken
* [libappindicator1](http://packages.ubuntu.com/de/trusty/libappindicator1)
* [libindicator7](http://packages.ubuntu.com/de/trusty/libindicator7)

manuell nachinstalliert werden.