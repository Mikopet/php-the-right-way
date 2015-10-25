---
title:  Databases
anchor: databases
---

# Adatbázisok {#databases_title}

Gyakran fogsz a PHP kódodban adatbázisokat használni az adatok tartós tárolására. Többféle lehetőséged van csatalkozni és műveleteket végezni az adatbázisodon. Az ajánlott lehetőség **PHP 5.1.0 -et követően** a native driver-ek használata volt, mint pl.: [mysqli], [pgsql], [mssql], stb.

A native driver-ek nagyszerűek, ha csak _egy_ adatbázist használsz az alkalmazásodban, de, ha például, MySQL-t és egy kis MSSQL-t is használsz, vagy Oracle adatbázishoz kell csatlakoznod, akkor nem használhatod ugyanazt a drivert. Meg kell tanulnod egy teljesen új API-t mindegyik adatbázishoz &mdash; és ez elég nagy ostobaság.


[mysqli]: http://php.net/mysqli
[pgsql]: http://php.net/pgsql
[mssql]: http://php.net/mssql
