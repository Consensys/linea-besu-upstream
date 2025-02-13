# Linea Besu Upstream Distribution
Github workflows to create and publish upstream Besu build for Linea.

This will replace [Linea-Besu](https://github.com/consensys/linea-besu) fork. The Linea-Besu distribution and maven packages created by this repo will be utilized by:
- https://github.com/Consensys/linea-besu-package
- various Linea plugins.

## Release Process
Modify `version.env` file and merge to `main` branch to trigger the release process.
The `LINEA_BESU_VERSION` in `version.env` file will be used to tag the release.