---
isChild: true
anchor:  composer_and_packagist
---

## Composer és Packagist {#composer_and_packagist_title}

A Composer egy **zseniális** függőségmenedzser PHP-hez. Sorold fel projekted függőségeit egy `composer.json` fájlban és néhány
egyszerű parancs használata után a Composer automatikusan letölti őket és beállítja az autoloadert számodra.

Rengeteg PHP könyvtár létezik amely kompatibilis a Composerrel, készen állva arra, hogy a projektedben használd. Ezeket
a csomagokat tartalmazza a [Packagist], a hivatalos tároló Composer-kompatibilis PHP könyvtárak számára.

### Hogyan telepítsd a Composert

Telepítheted a Composert lokálisan (a jelenlegi munkakönyvtárban) vagy globálisan (pl. /usr/local/bin, ez az ajánlott).
Tegyük fel, hogy globálisan szeretnéd telepíteni a Composert:

{% highlight console %}
curl -sS https://getcomposer.org/installer | php
mv composer.phar /usr/local/bin/composer
{% endhighlight %}

<strong>Megjegyzés:</strong> Ha a fenti nem működne jogosultságok hiánya miatt, futtasd újra a `mv`-ot `sudo`-val.

Ez letölti a `composer.phar` fájlt (egy PHP bináris archívumot). Ezt futtathatod a `php`-vel a projekted függőségeinek kezeléséhez.
<strong>Kérlek jegyezd meg:</strong> Ha direkt egy egy interpreterbe töltöd le a kódot, olvasd el előtte a kódot online a biztonság érdekében.

#### Telepítés Windows-zon

Windows felhasználók számára a legegyszerűbb módja hogy telepítsd és futtasd, hogy a [ComposerSetup]-ot használod, ami
elvégez egy globális telepítést és beállítja a `$PATH` környezeti változód, így bármely könyvtárban csak meg kell hívnod
a `composer` parancsot egy parancssorban.

### Hogyan telepítsd a Composer-t (kézzel)

A Composer kézi telepítése egy nehezebb feladat; azonban vannak különböző okok, amiért egy
fejlesztő talán inkább ezt a módszert választja az interaktív telepítési eljárással szemben.
Az interaktív telepítés ellenőrzi, hogy a PHP:

- megfelelő verziójú
- `.phar` fájlokat megfelelően tudja végrehajtani
- rendelkezik elegendő jogosultsággal bizonyos könyvtárakhoz
- egyes problémás kiterjesztéseket nem töltött be
- bizonyos `php.ini` beállításokat tartalmaz

Mivel a kézi telepítés egyik teljesülését sem ellenőrzi, neked kell eldönted, hogy ez a kompromisszum megéri-e neked.
Ebben az esetben a következő módon szerezheted be a Composert kézzel:

{% highlight console %}
curl -s https://getcomposer.org/composer.phar -o $HOME/local/bin/composer
chmod +x $HOME/local/bin/composer
{% endhighlight %}

A `$HOME/local/bin` útvonalnak (vagy általad választott könyvtárnak) be kell kerülnie a `$PATH` környezeti változóba.
Ez azt eredményezi, hogy a `composer` parancs rendelkezésre áll mindenhol.

When you come across documentation that states to run Composer as `php composer.phar install`, you can
substitute that with:

Amikor a dokumentációban azzal találkozol, hogy futtasd a Composert a `php composer.phar install` utasítással, azt helyettesítheted a következővel:

{% highlight console %}
composer install
{% endhighlight %}

Ez a szakasz a továbbiakban feltételezi, hogy a composer globálisan elérhető.

### Hogy definiáld és telepítsd a függőségeket

A Composer nyomon követi a projekt függőségeit a `composer.json` fájlban. Ezt kezelheted kézzel ha úgy tetszik,
vagy használhatod a Composert magát. A `composer require` parancs hozzáad egy függőséget a projekthez és ha nem rendelkezel
`composer.json` fájllal, létrehozza azt. Íme egy példa, amely hozzáadja a [Twig]-et függőségként a projektedhez.

{% highlight console %}
composer require twig/twig:~1.8
{% endhighlight %}

Alternatívaként a `composer init` parancs végigvezet téged egy teljes `composer.json` fájl létrehozásán.
Akárhogy is, ha egyszer már létrehoztad a `composer.json` fájlt, meg tudod mondani a Composernek hogy töltse le és
telepítse a függőségeket a `vendor/` könyvtárba. Ez vonatkozik a letöltött projektekre is, melyek tartalmaznak
`composer.json` fájlt:

{% highlight console %}
composer install
{% endhighlight %}

Ezután adjuk hozzá a következő sort az alkalmazás fő PHP fájljához; ez megmodnja a PHP-nek, hogy használja a Composer
autoloaderét a projekt függőségeihez.

{% highlight php %}
<?php
require 'vendor/autoload.php';
{% endhighlight %}

Mostmár használhatod a projekted függőségeit és azok be lesznek töltve, amikor szükség van rájuk.

### Függőségek frissítése

A Composer létrehoz egy `composer.lock` fájlt, mely tárolja a pontos verzióját minden letöltött csomagnak mikor először
futtattad a `composer install`-t. Ha más programozókkal dolgozol a projekten és a `composer.lock` fájl része a terjesztésednek,
mikor futtatják a `composer install`-t, ugyanazt a verziót kapják minden függőségből, mint te.
Ha módosítani szeretnéd a függőségeket, futtasd a `composer update`-et.

Ez leginkább akkor hasznos, mikor rugalmasan határozod meg a verzió követelményeket. Például a `~1.8` verzió
követelmény azt jelenti, hogy "bármi, ami újabb mint `1.8.0`, de kevesebb mint `2.0.x-dev`". Használhatod a
`*` helyettesítő karaktert is, mint pl. `1.8.*`. Most a Composer `composer update` parancsa frissíteni fogja az összes függőséget
a legújabb verzióra, amely illeszkedik a megadott korlátozásokra.

### Frissítési értesésítések

Ahhoz, hogy kapj értesítést az új verziókról, iratkozz fel a [VersionEye]-re, amely egy olyan internetes szolgáltatás,
mely figyeli a GitHub és BitBucket accountod `composer.json` fájljait és egy e-mailt küld az új csomag verziókkal.

### A függőségek biztonsági kockázatának ellenőrzése

A [Security Advisories Checker] egy webes szolgáltatás és parancssori eszköz, mely megvizsgálja a `composer.lock` fájlodat és jelzi, ha frissíteni
kell a függőségeket.

### Globális függőségek kezelése Composerrel

Composer tud kezelni globális függőségeket és binárisokat is. Használata egyszerű, csak annyit kell tenned, hogy
egy `global` prefixet használsz a parancsoknál. Ha például a PHPUnitot szeretnéd telepíteni és azt globálisan
elérhetővé tenni, az alábbi paranccsal teheted meg:

{% highlight console %}
composer global require phpunit/phpunit
{% endhighlight %}

Ez létrehoz egy `~/.composer` könyvtárat, ahol a globális függőségek laknak. Ahhoz, hogy a telepített
csomagok binárisai mindenhol elérhetőek legyenek, hozzáadhatjuk a `~/.composer/vendor/bin` könyvtárat
a `$PATH` változóhoz.

* [Tanulj többet a Composer-ről]

[Packagist]: http://packagist.org/
[Twig]: http://twig.sensiolabs.org
[VersionEye]: https://www.versioneye.com/
[Security Advisories Checker]: https://security.sensiolabs.org/
[Tanulj többet a Composer-ről]: http://getcomposer.org/doc/00-intro.md
[ComposerSetup]: https://getcomposer.org/Composer-Setup.exe
