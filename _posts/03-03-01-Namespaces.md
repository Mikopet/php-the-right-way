---
isChild: true
anchor:  namespaces
---

## Névterek {#namespaces_title}

Mint már említettük, a PHP közösség több tagja készít rengeteg féle kódot. Ez azt jelenti, hogy egy könyvtár PHP
kódjában talán ugyanaz az osztálynév van használva, mint egy másikban. Ha több könyvtár használja ugyanabban a 
névtérben, azok ütköznek és problémát okoznak.

A _névterek_ megoldják ezt a problémát. Ahogy a PHP referecina kézikönyv írja, a névterek az operációs rendszerek
könyvtáraihoz hasonlatosak; két fájl ugyanazzal a névvel létezhet külön könyvtárakban. Ugyanígy, két azonos nevű PHP
osztály létezhet külön névterekben. Ez ilyen egyszerű.

Nagyon fontos, hogy úgy alakítsd ki a névtereket a kódodban, hogy azok használhatóak legyenek más fejlesztők által 
is az ütközés veszélye nélkül.

Névterek használatának egy ajánlott útja fel lett vázolva a [PSR-4][psr4]-ben, amelynek célja egy szabványos, fájl, 
osztály és névtér egyezmény létrehozása, mely lehetővé teszi plug-and-play kódok létrehozását.

2014 októberében a PHP-FIG elavultként jelölte meg az előző autoloading szabványt: a [PSR-0][psr0]-t.
Mind a PSR-0 és a PSR-4 is tökéletesen használható. Az utóbbi igényli a PHP 5.3-at, de sok 5.2-es projekt a PSR-0-át 
implementálja.

Ha autolader szabványt szeretnél használni egy új alkalmazásban vagy csomagban, akkor a PSR-4-et nézd meg.

* [Read about Namespaces][namespaces]
* [Read about PSR-0][psr0]
* [Read about PSR-4][psr4]


[namespaces]: http://php.net/language.namespaces
[psr0]: http://www.php-fig.org/psr/psr-0/
[psr4]: http://www.php-fig.org/psr/psr-4/
