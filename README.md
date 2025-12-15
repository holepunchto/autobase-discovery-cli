# Autobase Discovery CLI

CLI for Autobase Discovery

## Install

```
npm i autobase-discovery-cli
```

## Usage

### Server

```
autodiscovery run <rpc-allowed-public-key>
```

Where `rpc-allowed-public-key` is the public key corresponding to the clients' seed (see the 'Security' section in autobase-discovery).

The RPC server's public key and the database key will be printed.

Logs are in pino's JSON format. Pipe them to `pino-pretty` for a human-readable format (`autodiscovery run | pino-pretty`)

Note that the database key is updated every time a new indexer is processed. In particular, you should add at least one entry to the database to stabilise the database key for the initial indexer.

### Client

Run `autodsicovery-client --help` to see all commands.

Example:

```
autodiscovery-client list <autodiscovery database key> <service-name>
```
