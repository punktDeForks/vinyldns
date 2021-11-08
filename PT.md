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
