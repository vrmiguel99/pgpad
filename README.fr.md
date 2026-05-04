<div align="center">
  <img align="center" width="128px" src="https://github.com/user-attachments/assets/28f39044-185c-4750-b2e2-21f56abc773a" />
	<h1 align="center"><b>pgpad</b></h1>
	<p align="center">
		[EN COURS] Un client de base de données multiplateforme simple et direct
  </p>
</div>

<img align="center" width="1624" height="1056" alt="image" src="https://github.com/user-attachments/assets/fecbe1e2-d0a5-46cc-8843-78b25a509a3f" />

### Qu'est-ce que c'est ?

- Un outil léger et réactif pour les requêtes quotidiennes
  - Démarrage rapide : se charge en moins d'une seconde sur ma machine.
  - Faible empreinte mémoire
  - Taille de paquet réduite
- Plus important encore, pgpad est _gratuit_, et le restera toujours. Cela inclut le fait de ne jamais avoir d'« Édition Communautaire », de fenêtres contextuelles vous demandant une mise à niveau, ou quoi que ce soit du genre.

### Qu'est-ce que ce _n'est pas_ ?

- Un système de gestion de bases de données professionnel et complet comme DBeaver.

### Bases de données prises en charge

|     Base de données     |          Statut          |                                                                  Note                                                                   |                                          Pilote                                           |
| :---------------------: | :----------------------: | :-------------------------------------------------------------------------------------------------------------------------------------: | :---------------------------------------------------------------------------------------: |
|       PostgreSQL        |  Implémenté, principal   |                                  Implémenté, le plus utilisé par les auteurs. Testé unitairement.                                       |            [`tokio-postgres`](https://github.com/rust-postgres/rust-postgres)             |
|         SQLite          |        Implémenté        |                                              Implémenté, testé unitairement.                                                            |                    [`rusqlite`](https://github.com/rusqlite/rusqlite)                     |
|       CockroachDB       |        Implémenté        |              Implémenté grâce au protocole Postgres Wire. Aucun test spécifique à CockroachDB pour le moment                            |            [`tokio-postgres`](https://github.com/rust-postgres/rust-postgres)             |
|          MySQL          |          Prévu           |                                                                                                                                         |                                            das                                            |
|  Microsoft SQL Server   |          Prévu           |                                                                                                                                         |                                                                                           |
|         Oracle          |          Prévu           |                                                                                                                                         |                 [`mysql`](https://github.com/blackbeam/rust-mysql-simple)                 |
|       Clickhouse        |          Prévu           |                                                                                                                                         |                [`clickhouse`](https://github.com/ClickHouse/clickhouse-rs)                |
|        SQLCipher        |          Prévu           |                                                                                                                                         |                    [`rusqlite`](https://github.com/rusqlite/rusqlite)                     |
|         DuckDB          |          Prévu           |                                                                                                                                         | [`duckdb`](<[https://github.com/rusqlite/rusqlite](https://github.com/duckdb/duckdb-rs)>) |
|         MongoDB         | Pas prévu actuellement   |                              Nécessiterait des refactorisations pour s'adapter à un SGBD NoSQL                                          |                                                                                           |
|         MariaDB         |                          | Rust ne dispose pas de pilote dédié à MariaDB. En l'état, nous ne pourrions prendre en charge MariaDB que via la compatibilité MySQL    |                                                                                           |

#### Systèmes d'exploitation

`pgpad` prend en charge Windows (7+), macOS (10.15+) et Linux (doit avoir `libwebkit2gtk` 4.1 ou supérieur).

## Compilation

### Prérequis

- Une version relativement récente de `npm`
- La chaîne d'outils Rust, avec une version minimale de 1.85

### Installation

#### 1. Installer les dépendances

```
npm install
```

#### Construire l'exécutable

```
npm run tauri build
```

#### Pour démarrer le serveur de développement

```
npm run tauri dev
```

## Un travail en cours !

N'hésitez pas à ouvrir des issues pour signaler des bugs ou faire des demandes de fonctionnalités.
