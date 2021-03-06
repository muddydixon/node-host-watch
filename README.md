# Catfish: server process monitoring and notification tool [![Build Status](https://travis-ci.org/muddydixon/node-catfish.svg?branch=master)](https://travis-ci.org/muddydixon/node-catfish)

Catfish is server process monitoring and notification agent.

## Install

```
$ npm install catfish
```

## Usage

Write json:

```json
{
    "interval": 5000,
    "specs": [
        {
            "name": "mysql (dummy)",
            "type": "ps",
            "value": "mysqld"
        },
        {
            "name": "redis (dummy)",
            "type": "ps",
            "value": "redis-server"
        }
    ],
    "notifications": [
        {
            "name": "slack",
            "type": "slack",
            "token": "<my token>",
            "domain": "<my domain>",
            "channel": "<my channel>",
            "username": "catfish"
        }
    ]
}
```

Exec this: (WIP)
```bash
./bin/catfish
```

## Plugins

### Specs

* process
* threshold
* bash

### Notifications

* mail
* slack
* webhook
* nagios
* sensu
* mackerel
