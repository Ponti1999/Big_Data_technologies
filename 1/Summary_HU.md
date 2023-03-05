---
author: Albert Dávid
neptun code: H1B5EF
date: 2023.03.05.
---

# Elmélet

- Entity - egyedi valóságban létező dolog
- Entity type - entity-ket közös tulajdonságok alapján leíró csoport
  - Logikai kategória
  - Ugyanolyan attribútumokkal leírt objektumok
  - Például: Tej, kenyér, csoki → Termék
- Entity Instance - egy Entyt type egyik specifikus példánya
- ER (Entity Relationship) diagram - egy adatmodell, amelyben az entitások és azok közötti kapcsolatok láthatók


## Levels Of Data Modeling
1. Conceptual data model - egyedek és a legmagasabb szintű kapcsolatok beazonosítja
2. Logical data model - az egyedek attribútumai is jelen vannak
3. Physical data model - DBRMS szinen (függ attól, hogy milyen rendszerben lesz megvalósítva)

Erőse gyedhalmazok: van primary key(), ami egyedi az egyedeknek)<br/>
Gyenge egyedhalmazok: nincs primary key() (jele: négyzet a négyzetben)<br/>
Foreign key: egy másik tábla egyedi kulcsa
- a másiik táblában is kulcsnak kell lennie (vagy elég csak egyedinek lennie)
- a másik táblában is léteznie kell az értéknek (esetleg null is lehet)

ISA kapcsolat - öröklődés

## Normalizálás
Functional dependency: egy attribútum egy másik attribútum függvénye
(egy relációban az attribútommok hogy függnek egymástól pl.: ha tudjuk a termék id-t, akkor tudjuk a termék nevét/márkáját is)

## 1NF - atomi adatok tárolása (attr. - nem lehet összetett / nem tartalmazhat több értéket)
Megoldási lehetőségek:
- horizontális - több attribútum egy táblában (több attr.-ok bevezeése)
- vertikális - az öszetett attr. szétszedése (több táblába szedése, új sorok/egyedek jönnek létre)

## 2NF - 1NF + a nem kuécs attr.-ok funkcionális függvénye a prim kulcs-tól
Ha 1NF és egyszerű a prim kulcs, akkor a 2NF biztosan teljesül (csak összetett prim kulcs esetén kell vizsgálni)<br/>
Megoldás:
- Megkeresni a függést, ami sérti a 2NF-t, és kiszervezni egy új táblába

## 3NF - 2NF + nem lehet funkc. függés a nem kulcs attr.-ok között
Megoldás:
- Hasonló módon mint a 2NF-nél kiszervezni külön táblába

## BCNF - 3NF-re hasonlít - "Ha van függőség a táblázatban, akkor az kulcs-függőség" (kicsit szigorúbb, mint a 3NF)

## SQL
1. DDL - Data Definition Language
   - Adatbázis objektumok manipulálása (kreálása, szerkezetének módosítása, törölése)
2. DML - Data Manipulation Language
   - Adatok manipulálása (insert, update, delete)
3. DCL - Data Control Language
   - Jogosultságok kezelése (grant, revoke)
4. TCL - Transaction Control Language
   - Tranzakciók kezelése (commit, rollback)
