# Fonctions

## Fonctions d’agrégation

Les fonctions d’agrégation permettent de calculer une valeur unique à partir d’un ensemble de valeurs. Elles sont souvent utilisées avec la clause `GROUP BY` pour regrouper les lignes en fonction de certaines colonnes.

### AVG

#### Description

La fonction `AVG()` calcule la moyenne des valeurs d’une colonne numérique.

#### Syntaxe

```sql
SELECT AVG(column_name) FROM table_name;
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

### COUNT

#### Description

La fonction `COUNT()` compte le nombre de lignes dans un ensemble de résultats.

#### Syntaxe

```sql
SELECT COUNT(column_name) FROM table_name;
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

### MAX

#### Description

La fonction `MAX()` renvoie la valeur maximale d’une colonne.

#### Syntaxe

```sql
SELECT MAX(column_name) FROM table_name;
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

### MIN

#### Description

La fonction `MIN()` renvoie la valeur minimale d’une colonne.

#### Syntaxe

```sql
SELECT MIN(column_name) FROM table_name;
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

### SUM

#### Description

La fonction `SUM()` calcule la somme des valeurs d’une colonne numérique.

#### Syntaxe

```sql
SELECT SUM(column_name) FROM table_name;
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

## Fonctions de chaînes de caractères

### CONCAT

#### Description

La fonction `CONCAT()` concatène deux chaînes de caractères ou plus.

#### Syntaxe

```sql
SELECT CONCAT(string1, string2, ...);
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

### LENGTH

#### Description

La fonction `LENGTH()` renvoie la longueur d'une chaîne de caractères.

#### Syntaxe

```sql
SELECT LENGTH(string);
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

### REPLACE

#### Description

La fonction `REPLACE()` remplace toutes les occurrences d'une sous-chaîne dans une chaîne par une autre sous-chaîne.

#### Syntaxe

```sql
SELECT REPLACE(string, substring, new_substring);
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

### SOUNDEX

#### Description

La fonction `SOUNDEX()` renvoie une chaîne de caractères représentant le code SOUNDEX d'une chaîne donnée.

#### Syntaxe

```sql
SELECT SOUNDEX(string);
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

### SUBSTRING

#### Description

La fonction `SUBSTRING()` extrait une sous-chaîne d'une chaîne de caractères.

#### Syntaxe

```sql
SELECT SUBSTRING(string, start, length);
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

### LEFT

#### Description

La fonction `LEFT()` renvoie les premiers caractères d'une chaîne de caractères.

#### Syntaxe

```sql
SELECT LEFT(string, number_of_chars);
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

### RIGHT

#### Description

La fonction `RIGHT()` renvoie les derniers caractères d'une chaîne de caractères.

#### Syntaxe

```sql
SELECT RIGHT(string, number_of_chars);
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

### REVERSE

#### Description

La fonction `REVERSE()` renverse l'ordre des caractères dans une chaîne de caractères.

#### Syntaxe

```sql
SELECT REVERSE(string);
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

### TRIM

#### Description

La fonction `TRIM()` supprime les espaces au début et à la fin d'une chaîne de caractères.

#### Syntaxe

```sql
SELECT TRIM(string);
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

### LTRIM

#### Description

La fonction `LTRIM()` supprime les espaces au début d'une chaîne de caractères.

#### Syntaxe

```sql
SELECT LTRIM(string);
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

### RTRIM

#### Description

La fonction `RTRIM()` supprime les espaces à la fin d'une chaîne de caractères.

#### Syntaxe

```sql
SELECT RTRIM(string);
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

### LPAD

#### Description

La fonction `LPAD()` remplit une chaîne de caractères avec une autre chaîne jusqu'à une longueur spécifiée (à gauche).

#### Syntaxe

```sql
SELECT LPAD(string, length, pad_string);
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

### UPPER

#### Description

La fonction `UPPER()` convertit une chaîne de caractères en majuscules.

#### Syntaxe

```sql
SELECT UPPER(string);
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

### LOWER

#### Description

La fonction `LOWER()` convertit une chaîne de caractères en minuscules.

#### Syntaxe

```sql
SELECT LOWER(string);
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

### UCASE

#### Description

La fonction `UCASE()` est un alias de `UPPER()`.

#### Syntaxe

```sql
SELECT UCASE(string);
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

### LCASE

#### Description

La fonction `LCASE()` est un alias de `LOWER()`.

#### Syntaxe

```sql
SELECT LCASE(string);
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

### LOCATE

#### Description

La fonction `LOCATE()` renvoie la position de la première occurrence d'une sous-chaîne dans une chaîne.

#### Syntaxe

```sql
SELECT LOCATE(substring, string);
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

### INSTR

#### Description

La fonction `INSTR()` renvoie la position de la première occurrence d'une sous-chaîne dans une chaîne.

#### Syntaxe

```sql
SELECT INSTR(string, substring);
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

## Fonctions mathématiques / numérique

### RAND

#### Description

La fonction `RAND()` renvoie un nombre aléatoire entre 0 et 1.

#### Syntaxe

```sql
SELECT RAND();
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

### ROUND

#### Description

La fonction `ROUND()` arrondit un nombre à un nombre spécifié de décimales.

#### Syntaxe

```sql
SELECT ROUND(number, decimals);
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

## Fonctions de dates et d’heures

### DATE_FORMAT

#### Description

La fonction `DATE_FORMAT()` permet de formater une date selon un modèle spécifié.

#### Syntaxe

```sql
SELECT DATE_FORMAT(date, format);
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

### DATEDIFF

#### Description

La fonction `DATEDIFF()` renvoie la différence en jours entre deux dates.

#### Syntaxe

```sql
SELECT DATEDIFF(date1, date2);
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

### DAYOFWEEK

#### Description

La fonction `DAYOFWEEK()` renvoie le jour de la semaine pour une date donnée (1 = dimanche, 2 = lundi, ...).

#### Syntaxe

```sql
SELECT DAYOFWEEK(date);
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

### MONTH

#### Description

La fonction `MONTH()` renvoie le mois d'une date donnée.

#### Syntaxe

```sql
SELECT MONTH(date);
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

### NOW

#### Description

La fonction `NOW()` renvoie la date et l'heure actuelles.

#### Syntaxe

```sql
SELECT NOW();
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

### SEC_TO_TIME

#### Description

La fonction `SEC_TO_TIME()` convertit un nombre de secondes en une valeur de temps au format 'HH:MM:SS'.

#### Syntaxe

```sql
SELECT SEC_TO_TIME(seconds);
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

### TIMEDIFF

#### Description

La fonction `TIMEDIFF()` renvoie la différence entre deux valeurs de temps.

#### Syntaxe

```sql
SELECT TIMEDIFF(time1, time2);
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

### TIMESTAMP

#### Description

La fonction `TIMESTAMP()` renvoie une valeur de date et d'heure.

#### Syntaxe

```sql
SELECT TIMESTAMP(date, time);
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

### YEAR

#### Description

La fonction `YEAR()` renvoie l'année d'une date donnée.

#### Syntaxe

```sql
SELECT YEAR(date);
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

## Fonctions de chiffrements

### MD5

#### Description

La fonction `MD5()` calcule le hachage MD5 d'une chaîne de caractères.

#### Syntaxe

```sql
SELECT MD5(string);
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

---

## Fonctions de conversion

### CAST

#### Description

La fonction `CAST()` convertit une valeur d'un type de données en un autre type de données.

#### Syntaxe

```sql
SELECT CAST(expression AS data_type);
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

### CONVERT

#### Description

La fonction `CONVERT()` convertit une valeur d'un type de données en un autre type de données.

#### Syntaxe

```sql
SELECT CONVERT(expression, data_type);
```

#### Compatibilité

|            |    COMPATIBLE    |
| ---------- | :--------------: |
| MySQL      | :material-check: |
| PostgreSQL | :material-close: |
| SQLite     | :material-close: |
| SQL Server | :material-check: |
| Oracle     | :material-close: |
| DB2        | :material-close: |
| MariaDB    | :material-check: |

---

## Fonctions de gestion des valeurs NULL

### ISNULL

#### Description

La fonction `ISNULL()` remplace les valeurs NULL par une valeur spécifiée.

#### Syntaxe

```sql
SELECT ISNULL(expression, value);
```

#### Compatibilité

|            |    COMPATIBLE    |
| ---------- | :--------------: |
| MySQL      | :material-close: |
| PostgreSQL | :material-close: |
| SQLite     | :material-close: |
| SQL Server | :material-check: |
| Oracle     | :material-close: |
| DB2        | :material-close: |
| MariaDB    | :material-close: |

---

## Fonctions de regroupement

### GROUP_CONCAT

#### Description

La fonction `GROUP_CONCAT()` renvoie une chaîne de caractères qui contient les valeurs concaténées d'une colonne pour chaque groupe.

#### Syntaxe

```sql
SELECT GROUP_CONCAT(column_name) FROM table_name GROUP BY column_name;
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

---

## Fonctions de métadonnées

### VERSION

#### Description

La fonction `VERSION()` renvoie la version du serveur de base de données.

#### Syntaxe

```sql
SELECT VERSION();
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
