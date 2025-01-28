# Installation d'un environnement d'apprentissage

Cette section présente les étapes pour installer et configurer un environnement de développement pour vous entraîner à écrire et exécuter des requêtes SQL sur votre machine. Ici nous nous concentrons l'installation d'un environnement d'apprentissage en favorisant la simplicité et la rapidité de mise en place.

!!! info ""

    Garder en tête que SQL est un langage standardisé, mais chaque SGBDR (Système de Gestion de Base de Données Relationnelles) a ses spécificités. Dans un environnement de production, vous devrez choisir un SGBDR en fonction de vos besoins et de vos contraintes.

## Installer un SGBDR

Il existe de nombreux systèmes de gestion de bases de données relationnelles (SGBDR) sur le marché, tels que MySQL, PostgreSQL, SQLite, Oracle, DB2, SQL Server, Sybase, MS Access, Teradata, Firebird, Apache Hive, Phoenix, Presto, etc. Chaque SGBDR a ses propres caractéristiques, avantages et inconvénients. Vous devez choisir le SGBDR qui répond le mieux à vos besoins en fonction de vos exigences en matière de performances, de fiabilité, de sécurité, de compatibilité, de coût, etc.

=== "SQLite"

    Le moyen le plus simple et rapide de commencer à travailler avec des bases de données relationnelles est d'installer SQLite, un moteur de base de données relationnelle open-source qui stocke les données dans des fichiers locaux. Il est léger, rapide et facile à utiliser. Vous pouvez télécharger SQLite à partir de son site officiel.

    - [Télécharger SQLite](https://www.sqlite.org/download.html)

## Intéragir avec la base de données

Il existe de nombreux outils pour interagir avec les bases de données relationnelles, tels que les interfaces graphiques, les éditeurs de code source, les applications web, les notebooks, etc. Voici 3 options facile à mettre en place qui vous permettront de pratiquer SQL sur votre machine.

=== "DBeaver"

    DBeaver est un outil de gestion de bases de données relationnelles open-source et multiplateforme. Il prend en charge de nombreux SGBDR, tels que MySQL, PostgreSQL, SQLite, Oracle, DB2, SQL Server, Sybase, MS Access, Teradata, Firebird, Apache Hive, Phoenix, Presto, etc.

    - [Télécharger DBeaver](https://dbeaver.io/download/)

=== "VS Code + SQLite Extension"

    VS Code est un éditeur de code source développé par Microsoft. Il prend en charge de nombreux langages de programmation et propose de nombreuses extensions pour faciliter le développement.

    - [Télécharger VS Code](https://code.visualstudio.com/download)

    Vous pouvez ensuite installer l'extension SQLite de alexcvzz qui vous permettra de travailler avec SQLite dans VS Code.

    Grafikart a réalisé une video tutoriel qui vous montre comment installer et utiliser ces outils.

    <iframe width="560" height="315" src="https://www.youtube.com/embed/HM8ihP0MzE8?si=cVdxJYOjcd64U-az" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

=== "Jupyter Notebook + JupySQL"

    Jupyter Notebook est une application web open-source qui permet de créer et de partager des documents contenant du code, des équations, des visualisations et du texte narratif. Il prend en charge plus de 40 langages de programmation, dont Python, R, Julia et Scala.

    - [Télécharger Jupyter Notebook](https://jupyter.org/install)

    Pour exécuter des requêtes SQL dans Jupyter Notebook, vous pouvez installer l'extension JupySQL.

    - [Installer JupySQL](https://jupysql.ploomber.io/en/latest/quick-start.html)
