# MMS Frontend Installationsanleitung

## Allgemeines 
Für die Installation des AHOI-MMS-Frontend-Tools werden verschiedene Basiskomponenten benötigt um die Funktionalität herzustellen. Aufgrund essentieller Probleme mit Windows wird das AHOI-MMS-Frontend-Tool vorerst nur für UNIX basierte Plattformen angeboten. 
Ferner benötigt man aktuell noch einen [GitHub Account](https://www.github.com) um die benötigten Framework Komponenten mit GIT erhalten zu können.

## Systemanforderungen 
Im folgenden werden in Kurzform die benötigten Komponenten aufgeführt:

* Benötigte Frameworks
    * NodeJS
        * inklusive Node Package Manager (NPM)
    * Bower
    * Grunt
    * Gulp

* Kernkomponenten
    * gulpsetup
    * mmsfrontend

## Installation unter Linux 

### Allgemeines
Sollte es beim Installationsprozess zu Fehlern des folgenden Typs kommen hier liegt das mit hoher Wahrscheinlichkeit daran, dass die Berechtigungen auf den Installationsordner fehlen, bzw nicht im benötigten Umfang zur Verfügung stehen.

`npm ERR! Error: EACCES, symlink '../lib/node_modules/XYZ'`

Abhilfe schafft hier die Besitzübernahme des `node_modules` Ordners sowie dessen Unterordnern mit dem folgenden Befehl.

`sudo chown -R $USER /usr/local/lib/node_modules/`

### Installation von NodeJS

Node.js kann in Linux direkt per Konsole installiert werden, die dafür benötigten Sourcen können wie folgt über das Advanced Packaging Tool (APT) heruntergeladen und installiert werden:

`sudo apt-get update
sudo apt-get install -y nodejs`

Eine weitere benötigte Komponente ist der Node Package Manager (NPM), mit diesem können die weiteren auf NodeJS basierenden Tools wie Bower oder Grunt installiert werden. Normalerweise wird NPM automatisch mit NodeJS installiert, ob dies der Fall ist kann man mit dem folgenden Befehl herausfinden:

`npm -v`

Wird eine Versionsnummer angezeigt ist NPM bereits installiert, sollte der NPM nicht gefunden werden können, muss er mit dem Befehl: 

`sudo apt-get install npm`

manuell nachinstalliert werden. 


### Installation von Bower
Bower ist ein Open Source Paketverwaltungstool welches das vereinfachte Installieren und Aktualisieren von Programmbibliotheken und Frameworks ermöglicht. Es benötigt NodeJS und wird über Konsolenbefehle bedient. In der Konfigurationsdatei (bower.json) werden die für das Projekt benötigten Libraries sowie Frameworks für das Projekt definiert und automatisch eingebunden. 

Bower wird mit NPM installiert:

`npm install -g bower`

Ob die Installation erfolgreich war kann man adäquat zu NPM mit dem Befehl

`bower -v`

überprüfen.

### Installation von gulp
Gulp wird als Prozessautomatisierer benötigt und kann wie gewohnt mit NPM installiert werden.

`npm install -g gulp`


### Installation von Grunt
Grunt ist ein der Taskrunner der es ermöglicht wiederkehrende Schritte in Build-Prozessen zu automatisieren. 

Grunt wird genauso wie bower mit Hilfe des NPM installiert der Befehl für die Installation ist nahezu gleich wie bei bower und gulp. 

`npm install -g grunt`

Standardmäßig wird grunt bzw. das grunt command line interface (CLI), wie alle NodeJS Module in den Ordner "/usr/local/lib/node_modules" installiert. Will man nun prüfen ob grunt fehlerfrei installiert wurde kann man dies tun indem man den Befehl

`grunt -v`

im Ordner 

`/usr/local/lib/node_modules/grunt-cli`

ausführen. Dort werden Fehler angezeigt sollten noch welchen bestehen.

### Klonen und einrichten des gulpsetups sowie des mmsfrontends
Nachdem nun die für die Installation der für die Ausführung benötigten Komponenten abgeschlossen ist, können die Kernkomponenten aus den jeweiligen GIT Repositories auf den lokalen Rechner geklont werden.

Das gulpsetup wird zuerst aus dem Repository geklont:

`git clone https://github.com/fokkerone/gulpsetup.git`

Anschließend dann das mmsfrontend

`git clone https://github.com/fokkerone/mmsfrontend.git`

wobei hier noch der branch gewechselt werden muss

`git checkout Dev`

Final müssen daraufhin noch in beiden geklonten Repositories mit dem NPM gebaut werden. Dazu muss jeweils im Ordner `$PFAD_ZUM_GIT_ORDNER/gulpsetup` sowie `$PFAD_ZUM_GIT_ORDNER/mmsfrontend` der Befehl:

`npm install amok grunt-cli bower-installer -g`

ausgeführt werden.

### Installationsabschluß & Verwendung des mmsfrontend-Generators
Um nun den Server für die Entwicklung zu starten muss per Shell in den Ordner

 `$PFAD_ZUM_GIT_ORDNER/mmsfrontend` 
 
 gewechselt und der Befehl 
 
 `node $PFAD_ZUM_GIT_ORDNER/gulpsetup` 
 
ausgeführt werden. War der Installationsvorgang erfolgreich wird ahoi gestartet und ein Auswahlmenü angezeigt.

![Auswahl der Optionen](https://c1.staticflickr.com/9/8735/17155976651_3a2946f5ac_b.jpg)

Zuerst sollte immer der Updater durch die Auswahl des Menüpunkts *Update Development Environment* ausgeführt werden. Die benötigten Komponenten werden daraufhin upgedated und neu gebaut

![Update Development Environment](https://c1.staticflickr.com/9/8718/16536445603_999174be2e_b.jpg)

Nach dem Update kann der Server dann mit dem Menüpunkt *Start Development* gestartet werden.

![Server Started](https://c2.staticflickr.com/8/7640/17155978701_0f8310fc10_b.jpg)

Hier kann nun in der Shell oder durch Eingabe der Adresse [http://localhost:9999](http://localhost:9999) im Browser die Übersicht gestartet werden.

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