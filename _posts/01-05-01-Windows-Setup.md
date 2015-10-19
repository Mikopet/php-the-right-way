---
isChild: true
anchor:  windows_setup
---

## Windows Telepítés {#windows_setup_title}

A PHP többféleképp elérhető a Windowshoz. Például [letöltheted a binárist][php-downloads] és mostanáig használhattad
a '.msi' telepítőt, ami már nem támogatott, és megállt a PHP 5.3-nál.

Tanuláshoz, és helyi fejlesztéshez használhatod a beépített webszervert 5.4 és afölötti PHP-val, így nem kell a 
konfigurálással foglalkoznod. Ha viszont szeretnél egy "all-in-one"-t, ami tartalmaz egy teljes webszervert és MySQL-t is,
akkor olyan eszközökre, mint a [Web Platform Installer][wpi], [XAMPP][xampp], [EasyPHP][easyphp] vagy [WAMP][wamp] 
van szükséged, ami segít, hogy a Windows fejlesztői környezeted működjön, és gyorsan fusson. Ezek viszont kicsit
másak mint egy éles környezet, szóval vigyázz a különbözőségekre ha Windowson dolgozol és Linuxra készül a szoftvered.

Ha az éles rendszert Windowson akarod futtatni, akkor az IIS7 adhatja neked a legstabilabb és legjobb teljesítményt.
Tudsz használni [phpmanager][phpmanager]-t (grafikus plugin IIS7-hez) a könnyű konfiguráláshoz, kezeléshez. Gyárilag
van benne FastCGI, neked csak a PHP-t kell konfigurálni mint "handler". Támogatásért, és egyéb forrásokért
itt egy [dedikált terület az iis.net-en][php-iis] PHP-hoz.


[php-downloads]: http://windows.php.net
[wpi]: http://www.microsoft.com/web/downloads/platform.aspx
[xampp]: http://www.apachefriends.org/en/xampp.html
[easyphp]: http://www.easyphp.org/
[wamp]: http://www.wampserver.com/en/
[phpmanager]: http://phpmanager.codeplex.com/
[php-iis]: http://php.iis.net/
