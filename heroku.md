# Heroku

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

- `heroku create`: create a new app
- `heroku info`: show info. about the app
- `heroku open`: open/run the app in browser at the generated URL. Sample: <https://rust-api-heroku-11ef8f87fb50.herokuapp.com/>
- `heroku logs`: show logs
- `heroku logs --tail`: show logs in real time
- `heroku logs --tail --app rust-api-heroku-11ef8f87fb50`: show logs in real time for a specific app
- `heroku addons`: show all the addons
- `heroku config`: show all the config vars

## Procfile

### Web app

To run a web server (API), we need to create a `Procfile` in the root of the project with the following content:

```bash
web: PORT=$PORT ./target/release/rust-api-heroku
```

> create a `.env` file (untracked) to store the `PORT` variable locally & then unwrap it in the code.

But the catch is that `PORT=$PORT` is not needed. We can simply use `web: ./target/release/rust-api-heroku`.

> The address host should be `0.0.0.0`, **NOT** ~~`127.0.0.1`/`localhost`/`::1`/`0.0.0.1`~~.
