---
toc_depth: 3
---

# Instructions

Les instructions SQL s'écrivent d'une manière qui ressemble à celle de phrases ordinaires en anglais. Cette ressemblance voulue vise à faciliter l'apprentissage et la lecture.

---

## Commentaires

#### Description

Les commentaires en SQL peuvent être sur une seule ligne ou sur plusieurs lignes.

#### Syntaxe

- Commentaire sur une seule ligne

```sql
-- Ceci est un commentaire sur une ligne
SELECT column1, column2, ...
FROM table_name;
```

- Commentaire sur plusieurs lignes

```sql
/*
Ceci est un commentaire
sur plusieurs lignes
*/
SELECT column1, column2, ...
FROM table_name;
```

#### Compatibilité

|            |    COMPATIBLE    |
| ---------- | :--------------: |
| MySQL      | :material-check: |
| PostgreSQL | :material-check: |
| SQLite     | :material-check: |
| SQL Server | :material-check: |
| Oracle     | :material-check: |
| DB2        | :material-check: |
| MariaDB    | :material-check: |

---

## Selection de données

### SELECT

#### Description

La commande `SELECT` est utilisée pour récupérer des données à partir d'une ou plusieurs tables. Elle peut être utilisée pour récupérer toutes les colonnes ou seulement certaines colonnes.

#### Syntaxe

```sql
SELECT column1, column2, ...
FROM table_name;
```

!!! info "Remarque"

    Utilisez des alias pour rendre vos requêtes plus lisibles, surtout lorsque vous travaillez avec plusieurs tables.

#### Compatibilité

|            |    COMPATIBLE    |
| ---------- | :--------------: |
| MySQL      | :material-check: |
| PostgreSQL | :material-check: |
| SQLite     | :material-check: |
| SQL Server | :material-check: |
| Oracle     | :material-check: |
| DB2        | :material-check: |
| MariaDB    | :material-check: |

### DISTINCT

#### Description

La commande `DISTINCT` est utilisée pour récupérer des valeurs uniques.

#### Syntaxe

```sql
SELECT DISTINCT column1, column2, ...
FROM table_name;
```

!!! info "Remarque"

    La commande `DISTINCT` s'applique à toutes les colonnes spécifiées dans la requête.

!!! tip "Conseil"

    Utilisez la commande `DISTINCT` avec parcimonie, car elle peut entraîner une augmentation significative du temps d'exécution de la requête. Lorsque c'est possible, préférez l'utilisation de `GROUP BY`.

#### Compatibilité

|            |    COMPATIBLE    |
| ---------- | :--------------: |
| MySQL      | :material-check: |
| PostgreSQL | :material-check: |
| SQLite     | :material-check: |
| SQL Server | :material-check: |
| Oracle     | :material-check: |
| DB2        | :material-check: |
| MariaDB    | :material-check: |

### SQL_NO_CACHE

#### Description

La commande `SQL_NO_CACHE` est utilisée pour empêcher le cache de MySQL de stocker les résultats de la requête.

#### Syntaxe

```sql
SELECT SQL_NO_CACHE column1, column2, ...
FROM table_name;
```

!!! warning "Avertissement"

    L'utilisation de `SQL_NO_CACHE` peut ralentir les performances de votre requête, car elle empêche l'utilisation du cache.

#### Compatibilité

|            |    COMPATIBLE    |
| ---------- | :--------------: |
| MySQL      | :material-check: |
| PostgreSQL | :material-close: |
| SQLite     | :material-close: |
| SQL Server | :material-close: |
| Oracle     | :material-close: |
| DB2        | :material-close: |
| MariaDB    | :material-check: |

### WHERE

#### Description

La commande `WHERE` est utilisée pour filtrer les résultats en fonction d'une condition.

#### Syntaxe

```sql
SELECT column1, column2, ...
FROM table_name
WHERE condition;
```

!!! tip "Conseil"

    Utilisez des index sur les colonnes fréquemment utilisées dans les conditions `WHERE` pour améliorer les performances des requêtes.

#### Compatibilité

|            |    COMPATIBLE    |
| ---------- | :--------------: |
| MySQL      | :material-check: |
| PostgreSQL | :material-check: |
| SQLite     | :material-check: |
| SQL Server | :material-check: |
| Oracle     | :material-check: |
| DB2        | :material-check: |
| MariaDB    | :material-check: |

### AND & OR

#### Description

Les opérateurs `AND` et `OR` sont utilisés pour combiner plusieurs conditions dans une clause `WHERE`.

#### Syntaxe

```sql
SELECT column1, column2, ...
FROM table_name
WHERE condition1 AND condition2;
```

!!! info "Remarque"

    Soyez attentif à l'ordre des conditions lorsque vous utilisez `AND` et `OR`, car cela peut affecter les résultats de la requête.

#### Compatibilité

|            |    COMPATIBLE    |
| ---------- | :--------------: |
| MySQL      | :material-check: |
| PostgreSQL | :material-check: |
| SQLite     | :material-check: |
| SQL Server | :material-check: |
| Oracle     | :material-check: |
| DB2        | :material-check: |
| MariaDB    | :material-check: |

### IN

#### Description

La commande `IN` est utilisée pour spécifier plusieurs valeurs possibles pour une colonne.

#### Syntaxe

```sql
SELECT column1, column2, ...
FROM table_name
WHERE column_name IN (value1, value2, ...);
```

#### Compatibilité

|            |    COMPATIBLE    |
| ---------- | :--------------: |
| MySQL      | :material-check: |
| PostgreSQL | :material-check: |
| SQLite     | :material-check: |
| SQL Server | :material-check: |
| Oracle     | :material-check: |
| DB2        | :material-check: |
| MariaDB    | :material-check: |

### BETWEEN

#### Description

La commande `BETWEEN` est utilisée pour filtrer les résultats dans une plage de valeurs.

#### Syntaxe

```sql
SELECT column1, column2, ...
FROM table_name
WHERE column_name BETWEEN value1 AND value2;
```

#### Compatibilité

|            |    COMPATIBLE    |
| ---------- | :--------------: |
| MySQL      | :material-check: |
| PostgreSQL | :material-check: |
| SQLite     | :material-check: |
| SQL Server | :material-check: |
| Oracle     | :material-check: |
| DB2        | :material-check: |
| MariaDB    | :material-check: |

### LIKE

#### Description

La commande `LIKE` est utilisée pour rechercher un modèle spécifié dans une colonne.

#### Syntaxe

```sql
SELECT column1, column2, ...
FROM table_name
WHERE column_name LIKE pattern;
```

!!! tip "Conseil"

    Utilisez des caractères génériques (`%` et `_`) avec précaution, car ils peuvent ralentir les performances des requêtes.

#### Compatibilité

|            |    COMPATIBLE    |
| ---------- | :--------------: |
| MySQL      | :material-check: |
| PostgreSQL | :material-check: |
| SQLite     | :material-check: |
| SQL Server | :material-check: |
| Oracle     | :material-check: |
| DB2        | :material-check: |
| MariaDB    | :material-check: |

### Wildcards (%, \_)

#### Description

Les caractères génériques `%` et `_` sont utilisés avec la commande `LIKE` pour rechercher des modèles.

#### Syntaxe

```sql
SELECT column1, column2, ...
FROM table_name
WHERE column_name LIKE 'a%';
```

#### Compatibilité

|            |    COMPATIBLE    |
| ---------- | :--------------: |
| MySQL      | :material-check: |
| PostgreSQL | :material-check: |
| SQLite     | :material-check: |
| SQL Server | :material-check: |
| Oracle     | :material-check: |
| DB2        | :material-check: |
| MariaDB    | :material-check: |

### IS NULL / IS NOT NULL

#### Description

Les commandes `IS NULL` et `IS NOT NULL` sont utilisées pour filtrer les résultats en fonction de la présence ou de l'absence de valeurs nulles.

#### Syntaxe

```sql
SELECT column1, column2, ...
FROM table_name
WHERE column_name IS NULL;
```

#### Compatibilité

|            |    COMPATIBLE    |
| ---------- | :--------------: |
| MySQL      | :material-check: |
| PostgreSQL | :material-check: |
| SQLite     | :material-check: |
| SQL Server | :material-check: |
| Oracle     | :material-check: |
| DB2        | :material-check: |
| MariaDB    | :material-check: |

### GROUP BY

#### Description

La commande `GROUP BY` est utilisée pour regrouper les résultats par une ou plusieurs colonnes.

#### Syntaxe

```sql
SELECT column1, column2, ...
FROM table_name
GROUP BY column1, column2, ...;
```

!!! Tip "Conseil"

    Utilisez `GROUP BY` avec des fonctions d'agrégation comme `COUNT`, `SUM`, `AVG`, etc., pour obtenir des résultats significatifs.

#### Compatibilité

|            |    COMPATIBLE    |
| ---------- | :--------------: |
| MySQL      | :material-check: |
| PostgreSQL | :material-check: |
| SQLite     | :material-check: |
| SQL Server | :material-check: |
| Oracle     | :material-check: |
| DB2        | :material-check: |
| MariaDB    | :material-check: |

### WITH ROLLUP

#### Description

La commande `WITH ROLLUP` est utilisée avec `GROUP BY` pour générer des sous-totaux et des totaux.

#### Syntaxe

```sql
SELECT column1, column2, ...
FROM table_name
GROUP BY column1, column2, ...
WITH ROLLUP;
```

#### Compatibilité

|            |    COMPATIBLE    |
| ---------- | :--------------: |
| MySQL      | :material-check: |
| PostgreSQL | :material-check: |
| SQLite     | :material-check: |
| SQL Server | :material-check: |
| Oracle     | :material-check: |
| DB2        | :material-check: |
| MariaDB    | :material-check: |

### HAVING

#### Description

La commande `HAVING` est utilisée pour filtrer les groupes de résultats créés par `GROUP BY`.

#### Syntaxe

```sql
SELECT column1, column2, ...
FROM table_name
GROUP BY column1, column2, ...
HAVING condition;
```

!!! tip "Conseil"

    Utilisez `HAVING` pour filtrer les résultats après l'application des fonctions d'agrégation.

#### Compatibilité

|            |    COMPATIBLE    |
| ---------- | :--------------: |
| MySQL      | :material-check: |
| PostgreSQL | :material-check: |
| SQLite     | :material-check: |
| SQL Server | :material-check: |
| Oracle     | :material-check: |
| DB2        | :material-check: |
| MariaDB    | :material-check: |

### ORDER BY

#### Description

La commande `ORDER BY` est utilisée pour trier les résultats par une ou plusieurs colonnes.
Utilisez `ASC` pour trier par ordre croissant et `DESC` pour trier par ordre décroissant.

#### Syntaxe

```sql
SELECT column1, column2, ...
FROM table_name
ORDER BY column1, column2, ... ASC|DESC;
```

#### Compatibilité

|            |    COMPATIBLE    |
| ---------- | :--------------: |
| MySQL      | :material-check: |
| PostgreSQL | :material-check: |
| SQLite     | :material-check: |
| SQL Server | :material-check: |
| Oracle     | :material-check: |
| DB2        | :material-check: |
| MariaDB    | :material-check: |

### AS (alias)

#### Description

La commande `AS` est utilisée pour renommer une colonne ou une table avec un alias.

#### Syntaxe

```sql
SELECT column1 AS alias1, column2 AS alias2, ...
FROM table_name;
```

!!! tip "Conseil"

    Utilisez des alias pour rendre vos requêtes plus lisibles et plus faciles à comprendre.

#### Compatibilité

|            |    COMPATIBLE    |
| ---------- | :--------------: |
| MySQL      | :material-check: |
| PostgreSQL | :material-check: |
| SQLite     | :material-check: |
| SQL Server | :material-check: |
| Oracle     | :material-check: |
| DB2        | :material-check: |
| MariaDB    | :material-check: |

### LIMIT

#### Description

La commande `LIMIT` est utilisée pour spécifier le nombre maximum de résultats à retourner.

#### Syntaxe

```sql
SELECT column1, column2, ...
FROM table_name
LIMIT number;
```

#### Compatibilité

|            |    COMPATIBLE    |
| ---------- | :--------------: |
| MySQL      | :material-check: |
| PostgreSQL | :material-check: |
| SQLite     | :material-check: |
| SQL Server | :material-check: |
| Oracle     | :material-check: |
| DB2        | :material-check: |
| MariaDB    | :material-check: |

### CASE

#### Description

La commande `CASE` est utilisée pour créer des conditions if-then-else dans les requêtes SQL.

#### Syntaxe

```sql
SELECT column1,
       CASE
           WHEN condition1 THEN result1
           WHEN condition2 THEN result2
           ELSE result3
       END
FROM table_name;
```

#### Compatibilité

|            |    COMPATIBLE    |
| ---------- | :--------------: |
| MySQL      | :material-check: |
| PostgreSQL | :material-check: |
| SQLite     | :material-check: |
| SQL Server | :material-check: |
| Oracle     | :material-check: |
| DB2        | :material-check: |
| MariaDB    | :material-check: |

### UNION

#### Description

La commande `UNION` est utilisée pour combiner les résultats de deux ou plusieurs requêtes `SELECT`.

#### Syntaxe

```sql
SELECT column1, column2, ...
FROM table_name1
UNION
SELECT column1, column2, ...
FROM table_name2;
```

#### Compatibilité

|            |    COMPATIBLE    |
| ---------- | :--------------: |
| MySQL      | :material-check: |
| PostgreSQL | :material-check: |
| SQLite     | :material-check: |
| SQL Server | :material-check: |
| Oracle     | :material-check: |
| DB2        | :material-check: |
| MariaDB    | :material-check: |

### UNION ALL

#### Description

La commande `UNION ALL` est utilisée pour combiner les résultats de deux ou plusieurs requêtes `SELECT`, y compris les doublons.

#### Syntaxe

```sql
SELECT column1, column2, ...
FROM table_name1
UNION ALL
SELECT column1, column2, ...
FROM table_name2;
```

#### Compatibilité

|            |    COMPATIBLE    |
| ---------- | :--------------: |
| MySQL      | :material-check: |
| PostgreSQL | :material-check: |
| SQLite     | :material-check: |
| SQL Server | :material-check: |
| Oracle     | :material-check: |
| DB2        | :material-check: |
| MariaDB    | :material-check: |

### INTERSECT

#### Description

La commande `INTERSECT` est utilisée pour retourner les résultats communs à deux ou plusieurs requêtes `SELECT`.

#### Syntaxe

```sql
SELECT column1, column2, ...
FROM table_name1
INTERSECT
SELECT column1, column2, ...
FROM table_name2;
```

#### Compatibilité

|            |    COMPATIBLE    |
| ---------- | :--------------: |
| MySQL      | :material-close: |
| PostgreSQL | :material-check: |
| SQLite     | :material-check: |
| SQL Server | :material-check: |
| Oracle     | :material-check: |
| DB2        | :material-check: |
| MariaDB    | :material-close: |

### EXCEPT / MINUS

#### Description

La commande `EXCEPT` (ou `MINUS` dans certains systèmes) est utilisée pour retourner les résultats de la première requête `SELECT` qui ne sont pas présents dans la seconde.

#### Syntaxe

```sql
SELECT column1, column2, ...
FROM table_name1
EXCEPT
SELECT column1, column2, ...
FROM table_name2;
```

#### Compatibilité

|            |    COMPATIBLE    |
| ---------- | :--------------: |
| MySQL      | :material-close: |
| PostgreSQL | :material-check: |
| SQLite     | :material-check: |
| SQL Server | :material-check: |
| Oracle     | :material-check: |
| DB2        | :material-check: |
| MariaDB    | :material-close: |

---

## Modifications de données

### INSERT INTO

#### Description

La commande `INSERT INTO` est utilisée pour insérer de nouvelles lignes dans une table.

#### Syntaxe

```sql
INSERT INTO table_name (column1, column2, ...)
VALUES (value1, value2, ...);
```

#### Compatibilité

|            |    COMPATIBLE    |
| ---------- | :--------------: |
| MySQL      | :material-check: |
| PostgreSQL | :material-check: |
| SQLite     | :material-check: |
| SQL Server | :material-check: |
| Oracle     | :material-check: |
| DB2        | :material-check: |
| MariaDB    | :material-check: |

### ON DUPLICATE KEY UPDATE

#### Description

La commande `ON DUPLICATE KEY UPDATE` est utilisée pour mettre à jour les colonnes si une clé dupliquée est trouvée lors de l'insertion.

#### Syntaxe

```sql
INSERT INTO table_name (column1, column2, ...)
VALUES (value1, value2, ...)
ON DUPLICATE KEY UPDATE column1 = value1, column2 = value2, ...;
```

#### Compatibilité

|            |    COMPATIBLE    |
| ---------- | :--------------: |
| MySQL      | :material-check: |
| PostgreSQL | :material-close: |
| SQLite     | :material-close: |
| SQL Server | :material-close: |
| Oracle     | :material-close: |
| DB2        | :material-close: |
| MariaDB    | :material-check: |

### UPDATE

#### Description

La commande `UPDATE` est utilisée pour modifier les données existantes dans une table.

#### Syntaxe

```sql
UPDATE table_name
SET column1 = value1, column2 = value2, ...
WHERE condition;
```

#### Compatibilité

|            |    COMPATIBLE    |
| ---------- | :--------------: |
| MySQL      | :material-check: |
| PostgreSQL | :material-check: |
| SQLite     | :material-check: |
| SQL Server | :material-check: |
| Oracle     | :material-check: |
| DB2        | :material-check: |
| MariaDB    | :material-check: |

### DELETE

#### Description

La commande `DELETE` est utilisée pour supprimer des lignes d'une table.

#### Syntaxe

```sql
DELETE FROM table_name
WHERE condition;
```

#### Compatibilité

|            |    COMPATIBLE    |
| ---------- | :--------------: |
| MySQL      | :material-check: |
| PostgreSQL | :material-check: |
| SQLite     | :material-check: |
| SQL Server | :material-check: |
| Oracle     | :material-check: |
| DB2        | :material-check: |
| MariaDB    | :material-check: |

### MERGE

#### Description

La commande `MERGE` est utilisée pour insérer ou mettre à jour des données en fonction de la correspondance des conditions.

#### Syntaxe

```sql
MERGE INTO table_name
USING table_name
ON condition
WHEN MATCHED THEN
    UPDATE SET column1 = value1, column2 = value2, ...
WHEN NOT MATCHED THEN
    INSERT (column1, column2, ...)
    VALUES (value1, value2, ...);
```

#### Compatibilité

|            |    COMPATIBLE    |
| ---------- | :--------------: |
| MySQL      | :material-close: |
| PostgreSQL | :material-close: |
| SQLite     | :material-close: |
| SQL Server | :material-check: |
| Oracle     | :material-check: |
| DB2        | :material-check: |
| MariaDB    | :material-close: |

---

## Manipulation de la structure

### TRUNCATE TABLE

#### Description

La commande `TRUNCATE TABLE` est utilisée pour supprimer toutes les lignes d'une table sans enregistrer les suppressions individuellement.

#### Syntaxe

```sql
TRUNCATE TABLE table_name;
```

#### Compatibilité

|            |    COMPATIBLE    |
| ---------- | :--------------: |
| MySQL      | :material-check: |
| PostgreSQL | :material-check: |
| SQLite     | :material-check: |
| SQL Server | :material-check: |
| Oracle     | :material-check: |
| DB2        | :material-check: |
| MariaDB    | :material-check: |

### CREATE DATABASE

#### Description

La commande `CREATE DATABASE` est utilisée pour créer une nouvelle base de données.

#### Syntaxe

```sql
CREATE DATABASE database_name;
```

#### Compatibilité

|            |    COMPATIBLE    |
| ---------- | :--------------: |
| MySQL      | :material-check: |
| PostgreSQL | :material-check: |
| SQLite     | :material-check: |
| SQL Server | :material-check: |
| Oracle     | :material-check: |
| DB2        | :material-check: |
| MariaDB    | :material-check: |

### DROP DATABASE

#### Description

La commande `DROP DATABASE` est utilisée pour supprimer une base de données existante.

#### Syntaxe

```sql
DROP DATABASE database_name;
```

#### Compatibilité

|            |    COMPATIBLE    |
| ---------- | :--------------: |
| MySQL      | :material-check: |
| PostgreSQL | :material-check: |
| SQLite     | :material-check: |
| SQL Server | :material-check: |
| Oracle     | :material-check: |
| DB2        | :material-check: |
| MariaDB    | :material-check: |

### CREATE TABLE

#### Description

La commande `CREATE TABLE` est utilisée pour créer une nouvelle table dans une base de données.

#### Syntaxe

```sql
CREATE TABLE table_name (
    column1 datatype,
    column2 datatype,
    ...
);
```

#### Compatibilité

|            |    COMPATIBLE    |
| ---------- | :--------------: |
| MySQL      | :material-check: |
| PostgreSQL | :material-check: |
| SQLite     | :material-check: |
| SQL Server | :material-check: |
| Oracle     | :material-check: |
| DB2        | :material-check: |
| MariaDB    | :material-check: |

### PRIMARY KEY

#### Description

La commande `PRIMARY KEY` est utilisée pour définir une colonne ou un ensemble de colonnes comme clé primaire de la table.

#### Syntaxe

```sql
CREATE TABLE table_name (
    column1 datatype PRIMARY KEY,
    column2 datatype,
    ...
);
```

#### Compatibilité

|            |    COMPATIBLE    |
| ---------- | :--------------: |
| MySQL      | :material-check: |
| PostgreSQL | :material-check: |
| SQLite     | :material-check: |
| SQL Server | :material-check: |
| Oracle     | :material-check: |
| DB2        | :material-check: |
| MariaDB    | :material-check: |

### AUTO_INCREMENT

#### Description

La commande `AUTO_INCREMENT` est utilisée pour générer automatiquement une valeur unique pour une colonne.

#### Syntaxe

```sql
CREATE TABLE table_name (
    column1 datatype AUTO_INCREMENT PRIMARY KEY,
    column2 datatype,
    ...
);
```

#### Compatibilité

|            |    COMPATIBLE    |
| ---------- | :--------------: |
| MySQL      | :material-check: |
| PostgreSQL | :material-check: |
| SQLite     | :material-check: |
| SQL Server | :material-check: |
| Oracle     | :material-check: |
| DB2        | :material-check: |
| MariaDB    | :material-check: |

### ALTER TABLE

#### Description

La commande `ALTER TABLE` est utilisée pour modifier la structure d'une table existante.

#### Syntaxe

```sql
ALTER TABLE table_name
ADD column_name datatype;
```

#### Compatibilité

|            |    COMPATIBLE    |
| ---------- | :--------------: |
| MySQL      | :material-check: |
| PostgreSQL | :material-check: |
| SQLite     | :material-check: |
| SQL Server | :material-check: |
| Oracle     | :material-check: |
| DB2        | :material-check: |
| MariaDB    | :material-check: |

### DROP TABLE

#### Description

La commande `DROP TABLE` est utilisée pour supprimer une table existante.

#### Syntaxe

```sql
DROP TABLE table_name;
```

!!! warning "Avertissement"

    La commande `DROP TABLE` supprimera définitivement la table et toutes ses données. Assurez-vous d'avoir une sauvegarde avant de l'utiliser.

#### Compatibilité

|            |    COMPATIBLE    |
| ---------- | :--------------: |
| MySQL      | :material-check: |
| PostgreSQL | :material-check: |
| SQLite     | :material-check: |
| SQL Server | :material-check: |
| Oracle     | :material-check: |
| DB2        | :material-check: |
| MariaDB    | :material-check: |

---

## Jointures

### INNER JOIN

#### Description

La commande `INNER JOIN` est utilisée pour retourner les lignes qui ont des valeurs correspondantes dans les deux tables.

#### Syntaxe

```sql
SELECT column1, column2, ...
FROM table1
INNER JOIN table2
ON table1.column_name = table2.column_name;
```

#### Compatibilité

|            |    COMPATIBLE    |
| ---------- | :--------------: |
| MySQL      | :material-check: |
| PostgreSQL | :material-check: |
| SQLite     | :material-check: |
| SQL Server | :material-check: |
| Oracle     | :material-check: |
| DB2        | :material-check: |
| MariaDB    | :material-check: |

### CROSS JOIN

#### Description

La commande `CROSS JOIN` est utilisée pour retourner le produit cartésien des deux tables.

#### Syntaxe

```sql
SELECT column1, column2, ...
FROM table1
CROSS JOIN table2;
```

#### Compatibilité

|            |    COMPATIBLE    |
| ---------- | :--------------: |
| MySQL      | :material-check: |
| PostgreSQL | :material-check: |
| SQLite     | :material-check: |
| SQL Server | :material-check: |
| Oracle     | :material-check: |
| DB2        | :material-check: |
| MariaDB    | :material-check: |

### LEFT JOIN

#### Description

La commande `LEFT JOIN` est utilisée pour retourner toutes les lignes de la table de gauche et les lignes correspondantes de la table de droite.

#### Syntaxe

```sql
SELECT column1, column2, ...
FROM table1
LEFT JOIN table2
ON table1.column_name = table2.column_name;
```

#### Compatibilité

|            |    COMPATIBLE    |
| ---------- | :--------------: |
| MySQL      | :material-check: |
| PostgreSQL | :material-check: |
| SQLite     | :material-check: |
| SQL Server | :material-check: |
| Oracle     | :material-check: |
| DB2        | :material-check: |
| MariaDB    | :material-check: |

### RIGHT JOIN

#### Description

La commande `RIGHT JOIN` est utilisée pour retourner toutes les lignes de la table de droite et les lignes correspondantes de la table de gauche.

#### Syntaxe

```sql
SELECT column1, column2, ...
FROM table1
RIGHT JOIN table2
ON table1.column_name = table2.column_name;
```

#### Compatibilité

|            |    COMPATIBLE    |
| ---------- | :--------------: |
| MySQL      | :material-check: |
| PostgreSQL | :material-check: |
| SQLite     | :material-check: |
| SQL Server | :material-check: |
| Oracle     | :material-check: |
| DB2        | :material-check: |
| MariaDB    | :material-check: |

### FULL JOIN

#### Description

La commande `FULL JOIN` est utilisée pour retourner toutes les lignes lorsque qu'il y a une correspondance dans une des tables.

#### Syntaxe

```sql
SELECT column1, column2, ...
FROM table1
FULL JOIN table2
ON table1.column_name = table2.column_name;
```

#### Compatibilité

|            |    COMPATIBLE    |
| ---------- | :--------------: |
| MySQL      | :material-close: |
| PostgreSQL | :material-check: |
| SQLite     | :material-check: |
| SQL Server | :material-check: |
| Oracle     | :material-check: |
| DB2        | :material-check: |
| MariaDB    | :material-close: |

### SELF JOIN

#### Description

La commande `SELF JOIN` est utilisée pour joindre une table à elle-même.

#### Syntaxe

```sql
SELECT column1, column2, ...
FROM table1 T1, table1 T2
WHERE condition;
```

#### Compatibilité

|            |    COMPATIBLE    |
| ---------- | :--------------: |
| MySQL      | :material-check: |
| PostgreSQL | :material-check: |
| SQLite     | :material-check: |
| SQL Server | :material-check: |
| Oracle     | :material-check: |
| DB2        | :material-check: |
| MariaDB    | :material-check: |

### NATURAL JOIN

#### Description

La commande `NATURAL JOIN` est utilisée pour retourner les lignes avec des valeurs correspondantes dans les colonnes ayant le même nom.

#### Syntaxe

```sql
SELECT column1, column2, ...
FROM table1
NATURAL JOIN table2;
```

#### Compatibilité

|            |    COMPATIBLE    |
| ---------- | :--------------: |
| MySQL      | :material-check: |
| PostgreSQL | :material-check: |
| SQLite     | :material-check: |
| SQL Server | :material-check: |
| Oracle     | :material-check: |
| DB2        | :material-check: |
| MariaDB    | :material-check: |

---

## Sous-requêtes

### SELECT

#### Description

Une sous-requête `SELECT` est utilisée pour retourner des données à utiliser dans une autre requête.

#### Syntaxe

```sql
SELECT column1, column2, ...
FROM table_name
WHERE column_name = (SELECT column_name FROM table_name WHERE condition);
```

#### Compatibilité

|            |    COMPATIBLE    |
| ---------- | :--------------: |
| MySQL      | :material-check: |
| PostgreSQL | :material-check: |
| SQLite     | :material-check: |
| SQL Server | :material-check: |
| Oracle     | :material-check: |
| DB2        | :material-check: |
| MariaDB    | :material-check: |

### EXISTS

#### Description

La commande `EXISTS` est utilisée pour tester l'existence de lignes dans une sous-requête.

#### Syntaxe

```sql
SELECT column1, column2, ...
FROM table_name
WHERE EXISTS (SELECT column_name FROM table_name WHERE condition);
```

#### Compatibilité

|            |    COMPATIBLE    |
| ---------- | :--------------: |
| MySQL      | :material-check: |
| PostgreSQL | :material-check: |
| SQLite     | :material-check: |
| SQL Server | :material-check: |
| Oracle     | :material-check: |
| DB2        | :material-check: |
| MariaDB    | :material-check: |

### ALL

#### Description

La commande `ALL` est utilisée pour comparer une valeur à toutes les valeurs d'un ensemble de résultats.

#### Syntaxe

```sql
SELECT column1, column2, ...
FROM table_name
WHERE column_name > ALL (SELECT column_name FROM table_name WHERE condition);
```

#### Compatibilité

|            |    COMPATIBLE    |
| ---------- | :--------------: |
| MySQL      | :material-check: |
| PostgreSQL | :material-check: |
| SQLite     | :material-check: |
| SQL Server | :material-check: |
| Oracle     | :material-check: |
| DB2        | :material-check: |
| MariaDB    | :material-check: |

### ANY / SOME

#### Description

Les commandes `ANY` et `SOME` sont utilisées pour comparer une valeur à n'importe quelle valeur d'un ensemble de résultats.

#### Syntaxe

```sql
SELECT column1, column2, ...
FROM table_name
WHERE column_name > ANY (SELECT column_name FROM table_name WHERE condition);
```

#### Compatibilité

|            |    COMPATIBLE    |
| ---------- | :--------------: |
| MySQL      | :material-check: |
| PostgreSQL | :material-check: |
| SQLite     | :material-check: |
| SQL Server | :material-check: |
| Oracle     | :material-check: |
| DB2        | :material-check: |
| MariaDB    | :material-check: |

---

## Index

### CREATE INDEX

#### Description

La commande `CREATE INDEX` est utilisée pour créer un index sur une table pour améliorer la vitesse des opérations de recherche.

#### Syntaxe

```sql
CREATE INDEX index_name
ON table_name (column1, column2, ...);
```

!!! tip "Conseil"

    Créez des index sur les colonnes fréquemment utilisées dans les clauses `WHERE` et `JOIN` pour améliorer les performances des requêtes.

#### Compatibilité

|            |    COMPATIBLE    |
| ---------- | :--------------: |
| MySQL      | :material-check: |
| PostgreSQL | :material-check: |
| SQLite     | :material-check: |
| SQL Server | :material-check: |
| Oracle     | :material-check: |
| DB2        | :material-check: |
| MariaDB    | :material-check: |

### EXPLAIN

#### Description

La commande `EXPLAIN` est utilisée pour obtenir des informations sur la manière dont MySQL exécute une requête.

#### Syntaxe

```sql
EXPLAIN SELECT column1, column2, ...
FROM table_name;
```

!!! info "Remarque"

    Utilisez `EXPLAIN` pour analyser et optimiser vos requêtes SQL.

#### Compatibilité

|            |    COMPATIBLE    |
| ---------- | :--------------: |
| MySQL      | :material-check: |
| PostgreSQL | :material-check: |
| SQLite     | :material-check: |
| SQL Server | :material-check: |
| Oracle     | :material-check: |
| DB2        | :material-check: |
| MariaDB    | :material-check: |

---

## Autres

### OPTIMIZE

#### Description

La commande `OPTIMIZE` est utilisée pour optimiser une table en réorganisant son stockage physique.

#### Syntaxe

```sql
OPTIMIZE TABLE table_name;
```

!!! tip "Conseil"

    Exécutez régulièrement `OPTIMIZE TABLE` sur vos tables pour maintenir des performances optimales.

#### Compatibilité

|            |    COMPATIBLE    |
| ---------- | :--------------: |
| MySQL      | :material-check: |
| PostgreSQL | :material-check: |
| SQLite     | :material-check: |
| SQL Server | :material-check: |
| Oracle     | :material-check: |
| DB2        | :material-check: |
| MariaDB    | :material-check: |
