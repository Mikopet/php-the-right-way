---
isChild: true
anchor:  namespaces
---

## Névterek {#namespaces_title}

Mint már említettük, a PHP közösségben rengeteg fejlesztő hoz létre rengeteg kódot. Ez azt jelenti, hogy egy könyvtár PHP
kódjában használhatja ugyanazt az osztály nevet, mint ami egy másik könyvtárban használatos. Amikor két könyvtár használja
ugyanazt a névtet, azok ütköznek és ez gondot okoz.

A névterek megoldják ezt a problémát. Amint az a PHP referencia kézikönyvben le van írva, a névterek működésben
az operációs rendszerek könyvtáraival hasonlatosak; két fájl azonos névvel szerepelhet két külön könyvtárban. Hasonlóképpen,
két azonos nevű PHP osztály létezhet külön PHP névterekben. Ez ennyire egyszerű.

Fontos, hogy úgy hozd létre a névtereket a kódodban, hogy azt más fejlesztők használhassák saját kódjukban anélkül,
hogy attól kellene tartaniuk az ütközik más könyvtárakkal.

Az egyik javasolt módja, hogy a [PSR-4] [psr4] -ben vázolt névtereket használj, amelynek célja hogy egy szabványos fájl, osztály és
névtér egyezmény kialakításával lehetővé tegye a plug-and-play kódot.

2014 októberébenben a PHP-FIG elavultá tette az előző autoloading szabványt: [PSR-0] [psr0], amelynek helyébe a
[PSR-4] [psr4] lép. Jelenleg még mindkettő használható, mivel PSR-4 igényli a PHP 5.3 verióját és sok PHP 5.2 verzión futó projekt használja a
PSR-0-t. Ha szeretnél használni egy autoloader szabványt egy új alkalmazáshoz vagy csomaghoz, akkor szinte biztosan érdekelni fog a PSR-4.

* [Read about Namespaces][namespaces]
* [Read about PSR-0][psr0]
* [Read about PSR-4][psr4]


[namespaces]: http://php.net/language.namespaces
[psr0]: https://github.com/php-fig/fig-standards/blob/master/accepted/PSR-0.md
[psr4]: https://github.com/php-fig/fig-standards/blob/master/accepted/PSR-4-autoloader.md
