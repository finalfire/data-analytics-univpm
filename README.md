# Repository per il corso di Data Analytics (AA 2023/24, Ingegneria Gestionale @ UNIVPM)

## Risorse utili

- [Lista di dataset (semplici) in formato CSV](https://people.sc.fsu.edu/~jburkardt/data/csv/csv.html)

## Snippet

- Creazione tabelle `Dipendente` e `Progetto`

```SQL
CREATE TABLE "Libreria"."Dipendente" (
	Id SERIAL PRIMARY KEY,
	Nome VARCHAR NOT NULL,
	Cognome VARCHAR NOT NULL,
	AnnoAssunzione integer NOT NULL,
	Salario numeric NOT NULL
)
```

```SQL
CREATE TABLE "Libreria"."Progetto" (
	Id SERIAL PRIMARY KEY,
	Nome VARCHAR NOT NULL,
	Descrizione VARCHAR,
	AnniProduzione integer NOT NULL,
	Manager integer NOT NULL,
	FOREIGN KEY (Manager) REFERENCES "Libreria"."Dipendente" (Id)
)
```