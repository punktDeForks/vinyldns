# VinylDNS development quick-start

Use GitHub Codespaces!

## Install sbt

```
curl -s "https://get.sdkman.io" | bash
sdk install scala 2.12.11
sdk install sbt
```

## Start VinylDNS

```
sbt
```

Wait until sbt is started.

```
dockerComposeUp
project api
reStart
project portal
preparePortal; run
```

## Build

Use credentials with read_registry/write_registry scope.

```
docker login docker-registry.punkt.de/docker/vinyldns
```

Push to `pt` branch first!

```
./build/docker-release.sh --clean --branch pt --latest --push --repository docker-registry.punkt.de/docker/vinyldns
```
