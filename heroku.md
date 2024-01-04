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
