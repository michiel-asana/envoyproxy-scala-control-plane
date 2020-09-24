# envoyproxy-scala-control-plane

The Envoy proxy controlplane APIs are not cross-compiled to Scala and are only available as Java. This project aims to fix that by regularly compiling a scala version as well.

Commands for generating scalapb definitions
Assuming you have bintray credentials.
```
sbt -mem 4096 +publish
```

Currently publishes for scala 2.11 and 2.12.

To update the API, update the SHAs in API_SHAS, and then run
```
sbt updateApi
```
