## Lezione 18/10/2023

```SQL
-- Restituire i clienti che hanno fatto almeno 2 ordini

SELECT "Cliente", COUNT(*)
FROM "Libreria"."Ordini"
GROUP BY "Cliente"
HAVING COUNT(*) >= 2
```

```SQL
-- Restituire la somma totale delle quantità vendute "per ogni" cliente

SELECT "Cliente", MAX("Quantita") AS "Quantita massima venduta"
FROM "Libreria"."Ordini"
GROUP BY "Cliente"
```

```SQL
-- Restituire i progetti e il manager assegnato ad ognuno di esso
-- e restituire solo il nome del progetto, e il nome e cognome del manager

SELECT P."nome" AS "Nome Progetto", D."nome" AS "Nome Manager", D."cognome" AS "Cognome Manager"
FROM "Lezione1810"."Progetto" AS P, "Lezione1810"."Dipendente" AS D
WHERE P."manager" = D."id"
```

```SQL

```