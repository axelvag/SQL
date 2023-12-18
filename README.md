# SQL Exercice

## In general

Pour présenter le langage SQL nous utiliserons le logiciel DB Browser for SQLite et nous reprendrons l'exemple des relations ouvrages et auteurs : 

	auteurs(id_auteur:entier, auteur:caractères[128], naissance:année, mort:année)
 
	ouvrages(numero:entier, titre:texte, date:année, #id_auteur:entier)

Remarque : 
SQLite implémente un nombre restreint de types de données. En particulier il n'existe pas de chaîne limitée à un nombre prédéfini de caractères ni de type année. Il reste cependant possible d'utiliser ces types dans la définition du schéma relationnel, mais il faut garder à l'esprit que ceux-ci se verront convertis automatiquement en texte ou en entier.

Création d'une base de données et des tables (CREATE)
Pour créer une base de données on commence tout simplement par définir son schéma relationnel dans le SGBDR. Ceci peut se faire à l'aide d'outils graphiques ou bien directement en langage SQL.
Cette première étape consiste à créer une nouvelle base de données, puis à créer les tables qui la constituent en définissant leur schéma relationnel et en précisant les clés primaires et étrangères (contrainte d'intégrité de référence). 


### Table of Contents ALL EXERCICE

- [Exercice_Book](#------------------------------Exercice_Book------------------------------)
- [Exercice_Enquete_SQL](#------------------------------Exercice_Enquete_SQL------------------------------)
- [Exercice_Execute_Query](#------------------------------Exercice_Execute_Query------------------------------)
- [Exercice_Relational_Schema](#------------------------------Exercice_Relational_Schema------------------------------)

### ------------------------------Exercice_Book------------------------------

Avec ce petit TD j'ai appris la synthaxe pour:
 - La création d'une base de donnée
   ```
   	CREATE TABLE "auteurs" (
	"id_auteur"	INTEGER NOT NULL,
	"nom"	VARCHAR(128),
	"naissance"	YEAR,
	"mort"	YEAR,
	PRIMARY KEY("id_auteur")
	);
   ```
 - Les ouvrages parus après 1865 dans l’ordre croissant de l’année de parution.
   ```SELECT * FROM ouvrages WHERE parution > 1865 ORDER BY parution;```
 - Suppression des ouvrages dont le id_auteur n'est pas 75 (Victor Hugo).
   ```DELETE FROM auteurs WHERE id_auteur <> 75;```



### ------------------------------Exercice_Enquete_SQL------------------------------

J'ai dû aider un inspecteur de Police, pour cela vous avez à votre disposition une énorme base de données contenant de nombreuses informations sur les habitants de SQL City, ainsi que les archives des incidents déjà survenus dans cette ville.
Tous les indices de ce mystère sont enterrés dans cette énorme base de données, et j'ai dû utiliser des commandes SQL pour naviguer dans ce vaste réseau d'informations.

### ------------------------------Exercice_Execute_Query------------------------------

Apprendre à utiliser DB Browser for SQLite.

Le logiciel DB Browser for SQLite permet d’exécuter des requêtes SQL sur une base de données au format SQLite.

### ------------------------------Exercice_Relational_Schema------------------------------



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
