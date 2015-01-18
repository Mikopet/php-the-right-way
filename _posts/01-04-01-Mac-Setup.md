---
isChild: true
anchor:  mac_setup
---

## Mac Telepítés {#mac_setup_title}

Az OS X előre csomagolt PHP-val jön, bár ez egy kicsit mindig le van maradva a legutolsó stabil verziótól.
A Mountain Lion-nak 5.3.10, Mavericks-nek 5.4.17, a Yosemite-nak pedig 5.5.9, de mióta kijött a PHP 5.6, ez nem elég.

Több megoldás is van, hogyan telepítheted a PHP-t OS X-en.

### Telepítsd a PHP-t Homebrew által

A [Homebrew] egy erőteljes csomagkezelő OS X-re, ami segíthet neked a PHP és különféle kiegészítőinek telepítésében.
A [Homebrew PHP] egy lerakat, ami PHP-val kapcsolatos "formulákat" tartalmaz a Homebrew számára, és általa telepítheted a PHP-t.

Ezen a ponton telepítheted a `php53`, `php54`, `php55` vagy a `php56`-ot is a `brew install` paranccsal, és válthatsz 
köztük a `PATH` változó módosításával.

### Telepítsd a PHP-t phpbrew által

A [phpbrew] egy eszköz a PHP verzióinak telepítéséhez és kezeléséhez. Ez nagyon hasznos tud lenni, ha két különböző
alkalmazás/projekt igényli az eltérő PHP verziókat, és nem virtuális gépeket használsz.

### Fordítsd forrásból

Mégegy megoldás, ami irányítást ad a telepített PHP verzió fölött, nem más, mint [fordítsd le magadnak][mac-compile].
Ebben az esetben győződj meg róla, hogy telepítve van az [Xcode][xcode-gcc-substitution] vagy az Apple pót megoldása, a
["Command Line Tools for XCode"], ami letölthető az Apple Mac Fejlesztői Központból.

### All-in-One telepítők

A fentebb említett megoldások főleg a PHP-t magát érintik, és nem foglalkoznak olyan dolgokkal, mint az Apache, Nginx
vagy egy SQL server. Az "All-in-one" megoldások, mint a [MAMP][mamp-downloads] és [XAMPP][xampp] feltelepítenek más 
szoftvereket is neked, és összekötik azokat. De ez a könnyítés a rugalmasság csökkenésével jár.


[Homebrew]: http://brew.sh/
[Homebrew PHP]: https://github.com/Homebrew/homebrew-php#installation
[phpbrew]: https://github.com/phpbrew/phpbrew
[mac-compile]: http://php.net/install.macosx.compile
[xcode-gcc-substitution]: https://github.com/kennethreitz/osx-gcc-installer
["Command Line Tools for XCode"]: https://developer.apple.com/downloads
[mamp-downloads]: http://www.mamp.info/en/downloads/
[xampp]: http://www.apachefriends.org/en/xampp.html
