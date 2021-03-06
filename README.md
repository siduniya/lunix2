# Lunik-Torrent
[![npm](https://img.shields.io/npm/v/lunik-torrent.svg)](https://www.npmjs.com/package/lunik-torrent)
[![Travis branch](https://img.shields.io/travis/Lunik/Lunik-Torrent/master.svg)](https://travis-ci.org/Lunik/Lunik-Torrent)
[![Codecov branch](https://img.shields.io/codecov/c/github/Lunik/Lunik-Torrent/master.svg)](https://codecov.io/gh/Lunik/Lunik-Torrent)
[![Dependency Status](https://gemnasium.com/badges/github.com/Lunik/Lunik-Torrent.svg)](https://gemnasium.com/github.com/Lunik/Lunik-Torrent)
[![js-standard-style](https://img.shields.io/badge/code%20style-standard-brightgreen.svg)](http://standardjs.com/)

## ===== View =====
![directory-view](https://puu.sh/qr53g/de79e3ea37.png)
![torrent-view](https://puu.sh/qr511/826c4c4019.png)

## ===== Installation =====
## Git

```
$ git clone https://github.com/Lunik/Lunik-Torrent.git
$ cd Lunik-Torrent
$ npm install
```

Configuration into: `configs/config.json`


### Run

```
$ npm start
or with forever
$ npm run deamon
```

## Heroku
[![Deploy](https://www.herokucdn.com/deploy/button.svg)](https://heroku.com/deploy?template=https://github.com/Lunik/Lunik-Torrent)

## Docker
[![Docker Stars](https://img.shields.io/docker/stars/lunik/lunik-torrent.svg)](https://hub.docker.com/r/lunik/lunik-torrent/)
[![Docker Pulls](https://img.shields.io/docker/pulls/lunik/lunik-torrent.svg)](https://hub.docker.com/r/lunik/lunik-torrent/)

```
$ docker pull lunik/lunik-torrent
$ docker run -d \
	-p 8080:8080 \
	-v /myconfigs:/usr/src/app/configs \
	-v /mydownloads:/usr/src/app/files \
	lunik/lunik-torrent
```

## ===== Infos =====
### Register

You need an inscription code provided by the server admin.

##### Create an invitation code
```
$ ./scripts/getinvite.sh
OR
$ curl --data "invitationkey=mykey" http://localhost:5000/auth?todo=invite
{
  "err":false,
  "invitationCode":"your_invitation_code"
}
```
To register go to `http://localhost:5000/login.html#your_invitation_code`
