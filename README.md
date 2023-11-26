# boltzcli

Connect boltz to your LND install and run swaps using the cli. This tool makes possible to connect your existing LND node to boltz and use the cli to make atomic swaps and reverse swaps.

First of all clone the repository and build the image

```
cd boltzcli
docker build -t massmux/boltzcli .
```

or get the ready image

```
docker pull massmux/boltcli
```

now rename the file .boltz-lnd/boltz.toml.example in .boltz-lnd/boltz.toml and configure the part of LND section to point to your LND funds source.

now just run the daemon

```
docker-compose up -d
```

when the daemon is running, you can invoke the cli like this

```
docker exec -ti boltzd boltzcli  getinfo
```
