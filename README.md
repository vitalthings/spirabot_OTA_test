# spirabot_OTA_test

## Overview

This repository serves as a **release distribution repository** for the Spirabot OTA (Over-The-Air) update system. It contains compiled binaries, firmware images, and release artifacts from the main development repository.

## Purpose

The sole purpose of this repository is to:
- Host release builds and binaries from the private development repository
- Provide a public distribution point for OTA firmware updates
- Maintain version history of released artifacts
- Enable automated OTA update systems to fetch firmware versions

## Repository Contents

This repository contains:
- **Releases**: Pre-built firmware binaries and artifacts (available in the [Releases](../../releases) section)
- Release notes and changelogs for each version
- Checksums and verification files for release artifacts

## For Users

To download firmware releases:
1. Navigate to the [Releases](../../releases) page
2. Select the desired version
3. Download the appropriate binary or artifact for your device
4. Follow the installation instructions provided in the release notes

## For Maintainers

This repository is automatically updated from the private development repository. 

### Publishing a Release

Releases should be created through GitHub's release interface:
1. Tag the appropriate commit with a version number (e.g., `v1.0.0`)
2. Upload compiled binaries and artifacts
3. Include comprehensive release notes
4. Mark pre-releases appropriately for beta/testing versions

## Security

Release artifacts should be verified before deployment:
- Check SHA256 checksums provided with each release
- Verify digital signatures where applicable
- Only download releases from the official [Releases](../../releases) page

## License

See the LICENSE file for licensing information.

## Support

For issues, bug reports, or feature requests related to the firmware itself, please contact the development team through appropriate channels (not through this repository).