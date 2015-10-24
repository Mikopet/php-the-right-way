---
isChild: true
anchor:  namespaces
---

## Névterek {#namespaces_title}

Mint már említettük, a PHP közösség több tagja készít rengeteg kódot. Ez azt jelenti, hogy egy könyvtár PHP
kódjában talán ugyanaz az osztálynév van használva, mint egy másikban. Ha több könyvtár használja ugyanabban a névtérben, azok ütköznek
és problémát okoznak.

A _névterek_ megoldják ezt a problémát. Ahogy a PHP referecina kézikönyv írja, a névterek az operációs rendszerek
könyvtáraihoz hasonlatosak; két fájl ugyanazzal a névvel létezhet külön könyvtárakban. Ugyanígy, két azonos nevű PHP
osztály létezhet külön névterekben. Ez ilyen egyszerű.

Nagyon fontos, hogy úgy alakítsd ki a névtereket a kódodban, hogy azok használhatóak legyenek más fejlesztők által is az ütközés
veszélye nélkül.

Névterek használatának egy ajánlott útja fel lett vázolva a [PSR-4][psr4]-ben, amelynek célja egy szabványos, fájl, osztály és
névtér egyezmény létrehozása, mely lehetővé teszi plug-and-play kódok létrehozását.

2014 októberében a PHP-FIG elavultként jelölte meg az előző autoloading szabványt, a [PSR-0][psr0]-t, amelyet a [PSR-4][psr4] vált fel.
Jelenleg mindkettő használható, mivel a PSR-4 igényli a PHP 5.3-as verzióját és több, csak PHP 5.2-n futó projekt implementálta
a PSR-0-t. Ha autolader szabványt szeretnél használni egy új alkalmazásban vagy csomagban, akkor szinte biztosan a PSR-4-et szeretnéd használni.

* [Read about Namespaces][namespaces]
* [Read about PSR-0][psr0]
* [Read about PSR-4][psr4]


[namespaces]: http://php.net/language.namespaces
[psr0]: https://github.com/php-fig/fig-standards/blob/master/accepted/PSR-0.md
[psr4]: https://github.com/php-fig/fig-standards/blob/master/accepted/PSR-4-autoloader.md
