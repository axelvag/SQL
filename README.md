# SQL Exercice

### Table of Contents ALL EXERCICE

- [Exercice_Book](#------------------------------Exercice_Book------------------------------)
- [Exercice_Enquete_SQL](#------------------------------Exercice_Enquete_SQL------------------------------)
- [Exercice_Execute_Query](#------------------------------Exercice_Execute_Query------------------------------)
- [Exercice_Relational_Schema](#------------------------------Exercice_Relational_Schema------------------------------)


## In general

To present the SQL language we will use the DB Browser for SQLite software and we will take the example of work and author relationships: 

	auteurs(id_auteur:entier, auteur:caractères[128], naissance:année, mort:année)
 
	ouvrages(numero:entier, titre:texte, date:année, #id_auteur:entier)

Noticed :
SQLite implements a limited number of data types. In particular, there is no string limited to a predefined number of characters or year type. However, it remains possible to use these types in the definition of the relational schema, but you must keep in mind that these will be automatically converted into text or integer.

Creating a database and tables (CREATE)
To create a database, you simply start by defining its relational schema in the RDBMS. This can be done using graphical tools or directly in SQL language.
This first step consists of creating a new database, then creating the tables that constitute it by defining their relational schema and specifying the primary and foreign keys (reference integrity constraint).


### ------------------------------Exercice_Book------------------------------

With this little tutorial I learned the syntax for:
 - Creating a database
   ```
   	CREATE TABLE "auteurs" (
	"id_auteur"	INTEGER NOT NULL,
	"nom"	VARCHAR(128),
	"naissance"	YEAR,
	"mort"	YEAR,
	PRIMARY KEY("id_auteur")
	);
   ```
 - Works published after 1865 in ascending order of the year of publication.
   ```SELECT * FROM ouvrages WHERE parution > 1865 ORDER BY parution;```
 - Deletion of works whose author_id is not 75 (Victor Hugo).
   ```DELETE FROM auteurs WHERE id_auteur <> 75;```



### ------------------------------Exercice_Enquete_SQL------------------------------

I had to help a Police Inspector, for this you have at your disposal a huge database containing a lot of information about the inhabitants of SQL City, as well as the archives of incidents that have already occurred in this city.
All the clues to this mystery are buried in this enormous database, and I had to use SQL commands to navigate this vast web of information.

### ------------------------------Exercice_Execute_Query------------------------------

Learn how to use DB Browser for SQLite.

The DB Browser for SQLite software allows you to execute SQL queries on a database in SQLite format.

### ------------------------------Exercice_Relational_Schema------------------------------

Summary of knowledge from all previous exercises:
 - Give the name of a relation corresponding to a table
 - What are the attributes of a relationship with its domain
 - Give the inputs (t-tuple or tuples)
 - Give the relational diagram of a relationship

## Starting ##

```bash
# Clone this project
$ git clone https://github.com/axelvag/SQL SQL

# Access
$ cd SQL

# Choose a project
$ cd [project_name]

# Open the subject
$ cat [file.pdf]


```
