---
anchor: code_style_guide
---

# Kódolási stílus {#code_style_guide_title}

A PHP közösség nagy én különböző, számtalan könyvtárból, keretrendszerből és komponensből áll. A fejlesztők válogathatnak
ezekből és tetszés szerint felhasználhatják saját projektjeikben. Fontos, hogy a PHP kód ragaszkodik bizonyos kódolási stílushoz
ami könnyebbé teszi más fejlesztők számára annak értelmezését és fel könnyen fel tudják használni saját projektjeikben.

A [Framework Interop Group][fig] javasolt és elfogadott egy sorozat ajánlást ami nem csak a kódolási stílusra tér ki. Ezek a
[PSR-0][psr0], [PSR-1][psr1], [PSR-2][psr2] és [PSR-4][psr4]. Ezek az ajánlások tulajdonképpen meghatározott szabályok amit
a legtöbb projekt mint Drupal, Zend, Symfony, Laravel, CakePHP, phpBB, AWS SDK, FuelPHP, Lithium, stb. elfogadtak. Használhatod
őket saját projektjeidben mint egy kódolási szabvány vagy folytathatod a saját stílusod.

Érdemes úgy kódolnod PHP-ban, hogy az valamilyen ismert szabványt kövessen. Ez lehet akármilyen kombinációja a PSR-nak, vagy
hasnálhatod a PEAR vagy Zend által kiadottakat. Ez azt eredményezi, hogy más fejlesztők könnyedén értelmezik az általad kiadott kódot és az alkalmazások esetén következetességet biztosít különböző komponensek között amikor sok harmadik féltől származó kóddal dolgozunk.


* [Olvass a PSR-0-ról][psr0]
* [Olvass a PSR-1-ről][psr1]
* [Olvass a PSR-2-ről][psr2]
* [Olvass a PSR-4-ről][psr4]
* [Olvass a PEAR Coding Standards-ről][pear-cs]
* [Olvass a Symfony Coding Standards-ről][symfony-cs]

Használhatsz [PHP_CodeSniffer][phpcs]-t hogy ellenőrizd a kódod meg felel-e a valamilyen kódolási szabványnak, és kiegészítéseket szerkesztőkhöz mint a [Sublime Text][st-cs] hogy valós visszajelzést kapj.

A következő eszközökkel automatikusan javíthatod a kódodat:

- Van a [PHP Coding Standards Fixer][phpcsfixer], aminek van egy nagyon jól tesztelt kódbázisa,
- Vagy a [PHP Code Beautifier and Fixer][phpcbf], amit alapból tartalmaz a PHP_CodeSniffer, hogy javítsa a kódot eszerint.

Illetve parancssorból futtathatod a phpcs parancsot:

    phpcs -sw --standard=PSR2 file.php

Megmutatja a hibákat és részletezi hogyan javíthatod meg.
Ez a parancs akkor is jó lehet, ha együtt használjuk egy git hook-al, ugyanis bizonyos branch-okba a kód addig nem kerül bele ameddig az általa jelzet hibák ki nem lesznek javítva.

Ha van PHP_CodeSniffer, akkor egy újabb paranccsal javíthatod őket amikor jelentésre kerülnek:
[PHP Code Beautifier and Fixer][phpcbf].

    phpcbf -w --standard=PSR2 file.php

Egy másik opció a [PHP Coding Standards Fixer][phpcsfixer].
Ez Megmutatja milyen hibák vannak a kód struktúrájában mielőtt javítja őket.

    php-cs-fixer fix -v --level=psr2 file.php

Az angol nyelv az előnyben részesített a szinbólumok elnevezésére. Kommentek írhatok egyéb nyelveken figyelembe véve azt, hogy kik fogják illetve kik akarják azt olvasni.


[fig]: http://www.php-fig.org/
[psr0]: http://www.php-fig.org/psr/psr-0/
[psr1]: http://www.php-fig.org/psr/psr-1/
[psr2]: http://www.php-fig.org/psr/psr-2/
[psr4]: http://www.php-fig.org/psr/psr-4/
[pear-cs]: http://pear.php.net/manual/en/standards.php
[symfony-cs]: http://symfony.com/doc/current/contributing/code/standards.html
[phpcs]: http://pear.php.net/package/PHP_CodeSniffer/
[phpcbf]: https://github.com/squizlabs/PHP_CodeSniffer/wiki/Fixing-Errors-Automatically
[st-cs]: https://github.com/benmatselby/sublime-phpcs
[phpcsfixer]: http://cs.sensiolabs.org/
