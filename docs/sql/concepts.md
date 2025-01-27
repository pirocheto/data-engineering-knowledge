# Concepts

## ACID

Les propriétés ACID sont des caractéristiques garanties par les systèmes de gestion de bases de données relationnelles pour garantir la fiabilité des transactions.

- **Atomicité** : Une transaction est une unité de travail qui doit être exécutée dans son intégralité ou pas du tout.
- **Cohérence** : Une transaction doit passer d'un état cohérent à un autre état cohérent.
- **Isolation** : Les transactions concurrentes ne doivent pas interférer les unes avec les autres.
- **Durabilité** : Les modifications apportées par une transaction doivent être persistantes.

## Groupes de commandes

Les commandes SQL sont généralement regroupées en quatre catégories principales en fonction de leur fonctionnalité.

### DML - Data Manipulation Language

- `SELECT` : Récupérer des données.
- `INSERT` : Insérer des données.
- `UPDATE` : Mettre à jour des données.
- `DELETE` : Supprimer des données.

### DDL - Data Definition Language

- `CREATE` : Créer des objets.
- `ALTER` : Modifier des objets.
- `DROP` : Supprimer des objets.
- `TRUNCATE` : Vider des objets.

### DCL - Data Control Language

- `GRANT` : Accorder des privilèges.
- `REVOKE` : Révoquer des privilèges.

### TCL - Transaction Control Language

- `COMMIT` : Valider une transaction.
- `ROLLBACK` : Annuler une transaction.
- `SAVEPOINT` : Créer un point de sauvegarde.
- `SET TRANSACTION` : Définir des propriétés de transaction.

L'objectif et le contexte dans lequel une commande est utilisée définie souvent sa catégorie.
Les groupes SQL (DQL, DML, DDL, DCL, TCL) ne sont pas complètement hermétiques. Les commandes comme SELECT ou les fonctions SQL agissent souvent comme des outils transversaux.
