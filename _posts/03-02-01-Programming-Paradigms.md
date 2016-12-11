---
isChild: true
anchor:  programming_paradigms
---

## Programozási paradigmák {#programming_paradigms_title}

A PHP egy rugalmas, dinamikus nyelv, sokféle programozási technikát támogat. Az évek folyamán nagyon sokat fejlődött, nevezetesen 2004-ben a PHP 5.0-ban megjelent egy stabil objektum-orientált modell, 2009-ben a PHP 5.3-ban a névtelen függvények és a névterek 2012-ben pedig a PHP 5.4-ben a trait-ek.

### Objektum-orientált programozás

A PHP teljes objektum-orientált programozási jellemzőkkel rendelkezik, többek között támogatja az osztályokat, absztrakt osztályokat, interfészeket, öröklést, kivitelezőket (constructor), klónozást, kivételeket, és így tovább.

* [Tanulj meg többet az objektum-orientált PHP-ról][oop]
* [Tanulj meg többet a Traits-ről][traits]

### Funkcionális programozás

A PHP támogatja a first-class függvényeket, amelyek olyan függvények amiket hozzárendelhetünk egy változóhoz. A felhasználó által meghatározott és a beépített függvények is lehetnek referenciaként letárolva egy változóban és hivatkozhatunk rájuk dinamikusan.
Függvények átathatóak paraméterként más függvényeknek (ezt _Higher-order Functions_-nek hívják), illetbe függvények visszaadhatnak függvényt végeredményül.

A rekurzió egy funkció ami megengedi a függvényeknek, hogy meghívják önmagukat, ez támogatott PHP-ban is habár a legtöbb PHP kód a folytonosságra fókuszál.

Az új névtelen függvények (closures támogatással) az 5.3-as (2009) verzióban jelentek meg.

A PHP 5.4 lehetőséget adott a bind closures használatára objektum hatáskörön, illetve fejlesztette a callables támogatottságát, hogy szinonímaként használhassuk névtelen függvényeknél minden esetben.

* Olvass többet a [Funkcionális programozásról PHP-ban](/pages/Functional-Programming.html)
* [Olvass a névtelen függvényekről][anonymous-functions]
* [Olvass a Closure osztályról][closure-class]
* [Részletesen a Closure-ről az RFC-ben][closures-rfc]
* [Olvass a Callables-ről][callables]
* [Olvass a dinamikus függvényhívásról a `call_user_func_array()`-el][call-user-func-array]

### Meta programozás

A PHP támogatja a meta programozás különféle fajtáit a Reflection API-tól a Magic metódusokig. Eg nagy halom Magic metódus elérhető a PHP-ban mint a `__get()`, `__set()`, `__clone()`, `__toString()`, `__invoke()`, stb. amelyekkel befolyásolhatjuk egy osztály viselkedését. A Ruby fejlesztők gyarkan hiányolják a `method_missing`-et, de elérhető változatai a `__call()` és `__callStatic()`.

* [Olvass többet a Magic metódusokról][magic-methods]
* [ROlvas többet a Reflection-ről][reflection]
* [Olvass többet az Overloading-ról][overloading]


[oop]: http://php.net/language.oop5
[traits]: http://php.net/language.oop5.traits
[anonymous-functions]: http://php.net/functions.anonymous
[closure-class]: http://php.net/class.closure
[closures-rfc]: https://wiki.php.net/rfc/closures
[callables]: http://php.net/language.types.callable
[call-user-func-array]: http://php.net/function.call-user-func-array
[magic-methods]: http://php.net/language.oop5.magic
[reflection]: http://php.net/intro.reflection
[overloading]: http://php.net/language.oop5.overloading
