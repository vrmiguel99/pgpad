<div align="center">
  <img align="center" width="128px" src="https://github.com/user-attachments/assets/28f39044-185c-4750-b2e2-21f56abc773a" />
	<h1 align="center"><b>pgpad</b></h1>
	<p align="center">
		[EN COURS] Un client de base de données multiplateforme simple et direct
  </p>
</div>

<img align="center" width="1624" height="1056" alt="image" src="https://github.com/user-attachments/assets/fecbe1e2-d0a5-46cc-8843-78b25a509a3f" />

### Qu'est-ce que c'est ?

- Un outil léger et réactif pour les requêtes du quotidien
  - Démarrage rapide : se charge en moins d'une seconde sur ma machine.
  - Faible empreinte mémoire
  - Petite taille de bundle
- Plus important encore, pgpad est _gratuit_, et le restera toujours. Cela inclut le fait de ne jamais avoir d'« Édition Communautaire », de fenêtres contextuelles vous demandant de passer à une version supérieure, ou quoi que ce soit de similaire.

### Qu'est-ce que ce n'est _pas_ ?

- Un système complet et professionnel de gestion de bases de données comme DBeaver.

### Bases de données prises en charge

|     Base de données      |          Statut          |                                                                  Note                                                                   |                                          Pilote                                           |
| :----------------------: | :----------------------: | :-------------------------------------------------------------------------------------------------------------------------------------: | :---------------------------------------------------------------------------------------: |
|        PostgreSQL        |  Implémentée, primaire   |                                       Implémentée, la plus utilisée par les auteurs. Testée unitairement.                                       |            [`tokio-postgres`](https://github.com/rust-postgres/rust-postgres)             |
|          SQLite          |       Implémentée        |                                                  Implémentée, testée unitairement.                                                  |                    [`rusqlite`](https://github.com/rusqlite/rusqlite)                     |
|       CockroachDB        |       Implémentée        |              Implémentée grâce au protocole filaire Postgres. Aucun test spécifique à CockroachDB pour le moment              |            [`tokio-postgres`](https://github.com/rust-postgres/rust-postgres)             |
|          MySQL           |          Prévue          |                                                                                                                                         |                                            das                                            |
|   Microsoft SQL Server   |          Prévue          |                                                                                                                                         |                                                                                           |
|          Oracle          |          Prévue          |                                                                                                                                         |                 [`mysql`](https://github.com/blackbeam/rust-mysql-simple)                 |
|        Clickhouse        |          Prévue          |                                                                                                                                         |                [`clickhouse`](https://github.com/ClickHouse/clickhouse-rs)                |
|        SQLCipher         |          Prévue          |                                                                                                                                         |                    [`rusqlite`](https://github.com/rusqlite/rusqlite)                     |
|          DuckDB          |          Prévue          |                                                                                                                                         | [`duckdb`](<[https://github.com/rusqlite/rusqlite](https://github.com/duckdb/duckdb-rs)>) |
|         MongoDB          | Non prévue actuellement  |                                  Nécessiterait des refactorisations pour s'adapter à un SGBD NoSQL                                  |                                                                                           |
|         MariaDB          |                          | Rust ne dispose pas d'un pilote dédié à MariaDB. En l'état, nous ne pourrions prendre en charge MariaDB que via la compatibilité MySQL |                                                                                           |

#### Systèmes d'exploitation

`pgpad` prend en charge Windows (7+), macOS (10.15+) et Linux (doit disposer de `libwebkit2gtk` 4.1 ou supérieur).

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

#### Pour démarrer le serveur de développement

```
npm run tauri dev
```

## Un travail en cours !

N'hésitez pas à ouvrir des issues pour les rapports de bugs et les demandes de fonctionnalités.
