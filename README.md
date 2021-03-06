## Slack Proxy for Emoji Generator
[![CircleCI](https://circleci.com/gh/emoji-gen/web-slack-proxy/tree/master.svg?style=shield)](https://circleci.com/gh/emoji-gen/web-slack-proxy/tree/master)
[![Requirements Status](https://requires.io/github/emoji-gen/web-slack-proxy/requirements.svg?branch=master)](https://requires.io/github/emoji-gen/web-slack-proxy/requirements/?branch=master)
[![Codacy Badge](https://api.codacy.com/project/badge/Grade/56377d1a156e44fc93d98dbae392dad4)](https://www.codacy.com/app/pinemz/web-slack-proxy?utm_source=github.com&amp;utm_medium=referral&amp;utm_content=emoji-gen/web-slack-proxy&amp;utm_campaign=Badge_Grade)
[![Osushi](https://img.shields.io/badge/donate-osushi-EA2F57.svg)](https://osushi.love/intent/post/9ad90add99954e62ac79251606c10eec)

:squirrel: Ultimate Slack Incoming Webhooks proxy

<br>
<br>

## Requirements

- Python `$(cat .python-version)`
- RabbitMQ

## Libraries

- [aiohttp](https://github.com/aio-libs/aiohttp) - Server-side framework

## Getting started

```
$ python -m venv venv
$ . venv/bin/activate
$ pip install -r requirements.txt

$ python app.py    # for web server
$ python worker.py # for asynchronous worker
```

## Test

```
$ pip install -r requirements-dev.txt
$ pytest
```

## Publish
### Requirements

- [Heroku account](https://heroku.com/)
- [Heroku CLI](https://devcenter.heroku.com/articles/heroku-cli)

### Commands

```
$ heroku create
$ heroku addons:create rabbitmq-bigwig:pipkin
$ heroku config:set ROOT_LOG_LEVEL=INFO
$ heroku config:set PYTHON_ENV=production
$ heroku buildpacks:add -i 1 https://github.com/mars/heroku-buildpack-gnu-parallel -a appname
$ git push heroku master
```

## License

MIT &copy; [Emoji Generator](https://emoji-gen.ninja)
