# Linea Besu Upstream Distribution
Github workflows to create and publish upstream Besu build for Linea.

This will replace [Linea-Besu](https://github.com/consensys/linea-besu) fork. The Linea-Besu distribution and maven packages created by this repo will be utilized by:
- https://github.com/Consensys/linea-besu-package
- various Linea plugins.

## Release Process
Modify `version.env` file and merge to `main` branch to trigger the release process.
The `LINEA_BESU_VERSION` in `version.env` file will be used to tag the release.

## Accessing the Maven artifacts

### Gradle Setup
Enable Cloudsmith repository in your `build.gradle` file:
```groovy
repositories {
  maven {
    url "https://artifacts.consensys.net/public/linea-besu/maven/"
  }
}
```

Declare the relevant dependencies in your `build.gradle` file:
```groovy
dependencies {
  implementation 'org.hyperledger.besu.internal:platform:<version>'
  implementation 'org.hyperledger.besu.internal:evmtool:<version>'
}
```

## Accessing the distribution
The relevant tar.gz distribution can be downloaded from the following link:
```
https://github.com/Consensys/linea-besu-upstream/releases/download/<version>/besu-<version>.tar.gz
```

See the Github [Releases](https://github.com/Consensys/linea-besu-upstream/releases) for all available versions.