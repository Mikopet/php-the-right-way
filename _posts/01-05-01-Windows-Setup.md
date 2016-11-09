---
isChild: true
anchor:  windows_setup
---

## Windows Telepítés {#windows_setup_title}

A [windows.php.net/download][php-downloads] címről tudod letölteni a binárist. 
Kicsomagolás után javasolt a [PATH][windows-path]-ot beállítani a PHP mappád gyökerére (ahol a php.exe is található), 
így bárhonnan futtatható lesz.

Tanuláshoz, és helyi fejlesztéshez használhatod a beépített webszervert 5.4 és afölötti PHP-val, így nem kell a 
konfigurálással foglalkoznod. Ha viszont szeretnél egy "all-in-one"-t, ami tartalmaz egy teljes webszervert és MySQL-t 
is, akkor olyan eszközökre, mint a [Web Platform Installer][wpi], [XAMPP][xampp], [EasyPHP][easyphp], 
[OpenServer][openserver] vagy [WAMP][wamp] van szükséged, ami segít, hogy a Windows fejlesztői környezeted működjön, és 
gyorsan fusson. Ezek viszont kicsit másak mint egy éles környezet, szóval vigyázz a különbözőségekre ha Windowson 
dolgozol és Linuxra készül a szoftvered.

Ha az éles rendszert Windowson akarod futtatni, akkor az IIS7 adhatja neked a legstabilabb és legjobb teljesítményt.
Tudsz használni [phpmanager][phpmanager]-t (grafikus plugin IIS7-hez) a könnyű konfiguráláshoz, kezeléshez. Gyárilag
van benne FastCGI, neked csak a PHP-t kell konfigurálni mint "handler". Támogatásért, és egyéb forrásokért itt egy 
[dedikált terület az iis.net-en][php-iis] PHP-hoz.

Alapvetően az alkalmazásod különböző területeken való futtatása furcsa hibákhoz vezethet, főként élesítéskor.
Ha Windowson fejlesztesz és Linuxra élesítesz (vagy bármi nem Windowsra), akkor érdemes fontolóra venned a 
[virtuális gépek](/#virtualization_title) használatát.

Chris Tankersley-nek van egy igen hasznos blog bejegyzése milyen eszközöket használ 
[Windowson való PHP fejlesztéskor][windows-tools].

[easyphp]: http://www.easyphp.org/
[phpmanager]: http://phpmanager.codeplex.com/
[openserver]: http://open-server.ru/
[wamp]: http://www.wampserver.com/en/
[php-downloads]: http://windows.php.net/download/
[php-iis]: http://php.iis.net/
[windows-path]: http://www.windows-commandline.com/set-path-command-line/
[windows-tools]: http://ctankersley.com/2015/07/01/developing-on-windows/
[wpi]: http://www.microsoft.com/web/downloads/platform.aspx
[xampp]: http://www.apachefriends.org/en/xampp.html
