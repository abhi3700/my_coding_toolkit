# Heroku

## Description

Heroku is a platform as a service (PaaS) that enables developers to build, run, and operate applications entirely in the cloud.

It supports following ways to deploy the code:

- Heroku Git
- Github
- Container Registry
    > Supports only docker image with amd64 architecture. Azure Container Registry supports both amd64 & arm64 architectures.

## Install

### macOS

```bash
brew tap heroku/brew && brew install heroku
```

## Setup

```bash
heroku login
```

## Commands

> Just add `--app <app-name>` or `-a <app-name>` to the command to run it for a specific app.

- `heroku apps:create`: create a new app
- `heroku apps:create <app-name>`: create a new app with a specific name
- `heroku apps:delete <app-name>`: delete an app
- `heroku apps:info <app-name>`: show info. about the app
- `heroku apps:open <app-name>`: open/run the app in browser at the generated URL. Sample: <https://rust-api-heroku-11ef8f87fb50.herokuapp.com/>
- `heroku logs`: show logs
- `heroku logs --tail`: show logs in real time
- `heroku logs --tail --app rust-api-heroku-11ef8f87fb50`: show logs in real time for a specific app
- `heroku addons`: show all the addons
- `heroku config`: show all the config vars
- `heroku config:set <key>=<value>`: set a config var
- `heroku config:unset <key>`: unset a config var
- `heroku config:get <key>`: get a config var
- `heroku config:get <key> --app <app-name>`: get a config var for a specific app
- `heroku stack:set heroku-24 -a <app-name>`: set the stack for a specific app

## Procfile

### Web app

To run a web server (API), we need to create a `Procfile` in the root of the project with the following content:

```bash
web: PORT=$PORT ./target/release/rust-api-heroku
```

> create a `.env` file (untracked) to store the `PORT` variable locally & then unwrap it in the code.

But the catch is that `PORT=$PORT` is not needed. We can simply use `web: ./target/release/rust-api-heroku`.

> The address host should be `0.0.0.0`, **NOT** ~~`127.0.0.1`/`localhost`/`::1`/`0.0.0.1`~~.

## Deployment

### Heroku Git

<u>Pros & Cons:</u> The code is to be pushed separately to Heroku & Github.

### Github

<u>Pros & Cons:</u> The code is to be pushed to Github only. Heroku will automatically deploy the code from Github.

### Container Registry

Need to push a docker image (with `amd64` architecture) to the registry.

## Troubleshooting

### 1. `Error R10 (Boot timeout) -> Web process failed to bind to $PORT within 60 seconds of launch`

- *Cause*: This means that the app is not able to bind to the port. This can happen if the port is not set correctly.
- *Solution*: Add `PORT=$PORT` in the "Settings >> Config Vars" in the Heroku app.

### 2. `MongoDB Error: Kind: Server selection timeout: No available servers. Topology: { Type: ReplicaSetNoPrimary, .....`

Full error:

```sh
Error: Kind: Server selection timeout: No available servers. Topology: { Type: ReplicaSetNoPrimary, Set Name: atlas-3wdz0g-shard-0, Servers: [ { Address: ac-xdtjxkm-shard-00-01.xrlfvc5.mongodb.net:27017, Type: Unknown }, { Address: ac-xdtjxkm-shard-00-00.xrlfvc5.mongodb.net:27017, Type: Unknown }, { Address: ac-xdtjxkm-shard-00-02.xrlfvc5.mongodb.net:27017, Type: Unknown } ] }, labels: {}
```

- *Cause*: Somehow the MongoDB connection string although being correct, is not discoverable by the Heroku app. I have experienced this in all other cloud providers like Render, Koyeb as well. Inspite of trying many different URI formats, the issue persisted.

```sh
MONGODB_URI=mongodb://USERNAME:PASSWORD@ac-xdtjxkm-shard-00-00.xrlfvc5.mongodb.net:27017,ac-xdtjxkm-shard-00-01.xrlfvc5.mongodb.net:27017,ac-xdtjxkm-shard-00-02.xrlfvc5.mongodb.net:27017/?ssl=true&connectTimeoutMS=30000&serverSelectionTimeoutMS=30000&w=majority&tlsAllowInvalidCertificates=true&authSource=admin&replicaSet=atlas-3wdz0g-shard-0
MONGODB_URI=mongodb+srv://USERNAME:PASSWORD@cluster0.xrlfvc5.mongodb.net/
MONGODB_URI=mongodb://USERNAME:PASSWORD@ac-xdtjxkm-shard-00-02.xrlfvc5.mongodb.net:27017
MONGODB_URI=mongodb+srv://USERNAME:PASSWORD@cluster0.xrlfvc5.mongodb.net/?retryWrites=true&w=majority&appName=Cluster0
```

- *Solution*: I simply switched to other MongoDB cloud provider like DigitalOcean. And on setting the URI in the Heroku app, the issue got solved 🎉.
