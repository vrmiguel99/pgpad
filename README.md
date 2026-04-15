<div align="center">
  <img align="center" width="128px" src="https://github.com/user-attachments/assets/28f39044-185c-4750-b2e2-21f56abc773a" />
	<h1 align="center"><b>pgpad</b></h1>
	<p align="center">
		[WIP] Un client de base de données multiplateforme simple et efficace
  </p>
</div>

<img align="center" width="1624" height="1056" alt="image" src="https://github.com/user-attachments/assets/fecbe1e2-d0a5-46cc-8843-78b25a509a3f" />

### Qu'est-ce que c'est ?

- Un outil léger et réactif pour les requêtes du quotidien
  - Démarrage rapide : se lance en moins d'une seconde sur ma machine.
  - Faible empreinte mémoire
  - Taille de bundle réduite
- Plus important encore, pgpad est _gratuit_, et le restera toujours. Cela signifie qu'il n'y aura jamais d'« Édition Communautaire », de pop-ups vous invitant à passer à une version supérieure, ni quoi que ce soit de ce genre.

### Ce que pgpad n'est _pas_

- Un système complet de gestion de bases de données professionnelles comme DBeaver.

### Bases de données prises en charge

|     Base de données     |            Statut             |                                                                    Note                                                                    |                                          Driver                                           |
| :---------------------: | :---------------------------: | :----------------------------------------------------------------------------------------------------------------------------------------: | :---------------------------------------------------------------------------------------: |
|       PostgreSQL        | Implémenté, support principal |                                   Implémenté, le plus utilisé par les auteurs. Tests unitaires.                                            |            [`tokio-postgres`](https://github.com/rust-postgres/rust-postgres)             |
|         SQLite          |         Implémenté            |                                                    Implémenté, tests unitaires.                                                            |                    [`rusqlite`](https://github.com/rusqlite/rusqlite)                     |
|       CockroachDB       |         Implémenté            |                    Implémenté grâce au protocole Postgres Wire Protocol. Pas de tests spécifiques à CockroachDB actuellement               |            [`tokio-postgres`](https://github.com/rust-postgres/rust-postgres)             |
|          MySQL          |          Prévu                |                                                                                                                                            |                                            das                                            |
| Microsoft SQL Server    |          Prévu                |                                                                                                                                            |                                                                                           |
|         Oracle          |          Prévu                |                                                                                                                                            |                 [`mysql`](https://github.com/blackbeam/rust-mysql-simple)                 |
|       Clickhouse        |          Prévu                |                                                                                                                                            |                [`clickhouse`](https://github.com/ClickHouse/clickhouse-rs)                |
|       SQLCipher         |          Prévu                |                                                                                                                                            |                    [`rusqlite`](https://github.com/rusqlite/rusqlite)                     |
|         DuckDB          |          Prévu                |                                                                                                                                            | [`duckdb`](<[https://github.com/rusqlite/rusqlite](https://github.com/duckdb/duckdb-rs)>) |
|        MongoDB          |   Non prévu actuellement      |                              Nécessiterait des refactorisations pour prendre en charge un SGBD NoSQL                                       |                                                                                           |
|        MariaDB          |                               | Rust ne dispose pas d'un driver MariaDB dédié. En l'état, MariaDB ne pourrait être pris en charge qu'à travers la compatibilité avec MySQL |                                                                                           |

#### Systèmes d'exploitation

`pgpad` prend en charge Windows (7+), macOS (10.15+) et Linux (nécessite `libwebkit2gtk` 4.1 ou supérieur).

## Compilation

### Prérequis

- Une version relativement récente de `npm`
- La chaîne d'outils Rust, avec une version minimale de 1.85

### Installation

#### 1. Installer les dépendances

```
npm install
```

#### Compiler l'exécutable

```
npm run tauri build
```

#### Lancer le serveur de développement

```
npm run tauri dev
```

## Un travail en cours !

N'hésitez pas à ouvrir des issues pour signaler des bugs ou proposer de nouvelles fonctionnalités.
