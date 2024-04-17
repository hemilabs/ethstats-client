# Hemi Network Intelligence API

This is the backend service which runs along with ethereum nodes and tracks the network status, fetches information through JSON-RPC and connects through WebSockets to an [ethstats-server](https://github.com/hemilabs/ethstats-server) to feed information.

## Installation

Clone the repository, install node dependencies.

```bash
git clone https://github.com/hemilabs/ethstats-client.git
cd ethstats-client/
npm install
```

## Configuration

Set the following environment variables:

* `CONTACT_DETAILS`: Optional email of the node maintainer.
* `INSTANCE_NAME`: Name of the monitored node.
* `LISTENING_PORT`: P2P port of the node.
* `RPC_URL`: URL of the RPC endpoint of the node.
* `WS_SECRET`: Server secret. Ask in [Discord](https://discord.gg/hemixyz) for it.
* `WS_SERVER`: Server websocket URL.

## Run

```bash
docker run --env-file .env --interactive --rm --tty hemilabs/ethstats-client:master
```
