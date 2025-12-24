
# PragmaticBeaver Usage Guide

## Dev stuff

<https://news.ycombinator.com/item?id=32514472>

<https://github.com/librespot-org/librespot/wiki/Reverse-engineering>

<https://github.com/librespot-org/librespot/discussions/1562>

## Setup

Installation found under [COMPILING.md](./COMPILING.md)

## Usage

General usage information under [README.md](./README.md)

### Start app

```sh
./target/debug/librespot -n "BeaverSpotifyBox" -b 320 -c ./cache --enable-volume-normalisation --initial-volume 100 --device-type avr -v --enable-oauth
```

### Get Access token

```sh
cargo install librespot-oauth --example oauth_sync && oauth_sync
```

## Decrypt file

```sh
openssl rsautl -decrypt -in $ENCRYPTED -out $PLAINTEXT -inkey keys/privkey.pem
```

```sh
openssl pkeyutl -decrypt -in "/home/dome/src/librespot/cache/files/2f/d32d50767b51047b84ef1e588add33c0df5011" -out ./test -inkey ./key.pem
```
