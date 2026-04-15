<div align="center">
  <img align="center" width="128px" src="https://github.com/user-attachments/assets/28f39044-185c-4750-b2e2-21f56abc773a" />
	<h1 align="center"><b>pgpad</b></h1>
	<p align="center">
		[WIP] Un client di database multipiattaforma semplice e diretto
  </p>
</div>

<img align="center" width="1624" height="1056" alt="image" src="https://github.com/user-attachments/assets/fecbe1e2-d0a5-46cc-8843-78b25a509a3f" />

### Cos'è?

- Uno strumento leggero e reattivo per le query di tutti i giorni
  - Avvio rapido: si carica in meno di un secondo sulla mia macchina.
  - Basso consumo di memoria
  - Dimensione del bundle ridotta
- Soprattutto, pgpad è _gratuito_, e lo sarà sempre. Questo significa che non ci sarà mai una "Community Edition", pop-up che ti chiedono di passare a una versione superiore, né nulla del genere.

### Cosa _non_ è?

- Un sistema completo di gestione di database professionale come DBeaver.

### Database supportati

|       Database       |            Stato            |                                                                       Nota                                                                        |                                          Driver                                           |
| :------------------: | :-------------------------: | :------------------------------------------------------------------------------------------------------------------------------------------------: | :---------------------------------------------------------------------------------------: |
|      PostgreSQL      | Implementato, supporto principale |                                   Implementato, il più utilizzato dagli autori. Test unitari.                                                      |            [`tokio-postgres`](https://github.com/rust-postgres/rust-postgres)             |
|        SQLite        |        Implementato         |                                                         Implementato, test unitari.                                                                |                    [`rusqlite`](https://github.com/rusqlite/rusqlite)                     |
|     CockroachDB      |        Implementato         |                    Implementato grazie al Postgres Wire Protocol. Nessun test specifico per CockroachDB al momento                                 |            [`tokio-postgres`](https://github.com/rust-postgres/rust-postgres)             |
|        MySQL         |         Pianificato         |                                                                                                                                                    |                                            das                                            |
| Microsoft SQL Server |         Pianificato         |                                                                                                                                                    |                                                                                           |
|        Oracle        |         Pianificato         |                                                                                                                                                    |                 [`mysql`](https://github.com/blackbeam/rust-mysql-simple)                 |
|      Clickhouse      |         Pianificato         |                                                                                                                                                    |                [`clickhouse`](https://github.com/ClickHouse/clickhouse-rs)                |
|      SQLCipher       |         Pianificato         |                                                                                                                                                    |                    [`rusqlite`](https://github.com/rusqlite/rusqlite)                     |
|        DuckDB        |         Pianificato         |                                                                                                                                                    | [`duckdb`](<[https://github.com/rusqlite/rusqlite](https://github.com/duckdb/duckdb-rs)>) |
|       MongoDB        | Non pianificato al momento  |                              Richiederebbe alcune refactoring per supportare un DBMS NoSQL                                                         |                                                                                           |
|       MariaDB        |                             | Rust non dispone di un driver MariaDB dedicato. Allo stato attuale, il supporto a MariaDB sarebbe possibile solo tramite la compatibilità con MySQL |                                                                                           |

#### Sistemi operativi

`pgpad` supporta Windows (7+), macOS (10.15+) e Linux (è necessario `libwebkit2gtk` 4.1 o superiore).

## Compilazione

### Prerequisiti

- Una versione relativamente recente di `npm`
- La toolchain di Rust, con una versione minima di 1.85

### Configurazione

#### 1. Installare le dipendenze

```
npm install
```

#### Compilare l'eseguibile

```
npm run tauri build
```

#### Avviare il server di sviluppo

```
npm run tauri dev
```

## Un lavoro in corso!

Non esitate ad aprire delle issue per segnalare bug o richiedere nuove funzionalità.
