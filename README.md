# skype-bridge [![#matrix-puppet-bridge:matrix.org](https://img.shields.io/matrix/matrix-puppet-bridge:matrix.org.svg?label=%23matrix-puppet-bridge%3Amatrix.org&logo=matrix&server_fqdn=matrix.org)](https://matrix.to/#/#matrix-puppet-bridge:matrix.org)

This is a Matrix bridge for Skype. It uses [skype-http](https://github.com/ocilo/skype-http) under the hood.

## features

- [x] Skype to Matrix direct text message
- [x] Matrix to Skype direct text message
- [x] Skype to Matrix direct image attachment message
- [x] Matrix to Skype direct image attachment message
- [x] group messaging
- [ ] read receipts
- [ ] contact list syncing

## installation

clone this repo

cd into the directory

run `npm install`

## configure

Copy `config.sample.json` to `config.json` and update it to match your setup

## register the app service

Generate an `skype-registration.yaml` file with `node index.js -r -u "http://your-bridge-server:8090"`

Note: The 'registration' setting in the config.json needs to set to the path of this file. By default, it already is.

Copy this `skype-registration.yaml` file to your home server, then edit it, setting its url to point to your bridge server. e.g. `url: 'http://your-bridge-server.example.org:8090'`

Edit your homeserver.yaml file and update the `app_service_config_files` with the path to the `skype-registration.yaml` file.

Launch the bridge with ```node index.js```.

Restart your HS.

## Discussion, Help and Support

Join us in the [![Matrix Puppet Bridge](https://user-images.githubusercontent.com/13843293/52007839-4b2f6580-24c7-11e9-9a6c-14d8fc0d0737.png)](https://matrix.to/#/#matrix-puppet-bridge:matrix.org) room

# TODO
* Be able to originate conversations from the Matrix side.
