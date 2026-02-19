# Release Management

This document provides information about the release management process for this repository.

## Release Structure

Each release in this repository follows a structured format to ensure consistency and clarity.

### Version Naming

Releases follow Semantic Versioning (SemVer) principles:
- **Major version** (X.0.0): Breaking changes or major feature additions
- **Minor version** (0.X.0): New features, backward compatible
- **Patch version** (0.0.X): Bug fixes and minor improvements

Version tags are prefixed with 'v' (e.g., `v1.0.0`, `v1.2.3`)

### Release Types

- **Stable Release**: Production-ready firmware (e.g., `v1.0.0`)
- **Pre-release**: Beta or release candidate versions (e.g., `v1.0.0-beta.1`, `v1.0.0-rc.1`)

## Release Artifacts

Each release typically includes:

1. **Firmware Binary**: The main firmware file(s) for flashing
2. **SHA256 Checksums**: File containing checksums for verification
3. **Release Notes**: Detailed changelog and upgrade instructions
4. **Documentation**: Any relevant documentation updates

### Artifact Naming Convention

Artifacts should follow a consistent naming pattern:
```
spirabot-firmware-v{VERSION}-{PLATFORM}.{EXTENSION}
```

Examples:
- `spirabot-firmware-v1.0.0-esp32.bin`
- `spirabot-firmware-v1.0.0-esp32.bin.sha256`

## Verification

All releases should include SHA256 checksums for verification. To verify a download:

```bash
# On Linux/Mac
sha256sum -c firmware.bin.sha256

# On Windows (PowerShell)
Get-FileHash firmware.bin -Algorithm SHA256
```

Compare the output with the checksum provided in the release.

## Release History

For a complete list of releases, see the [Releases page](../../releases).

## Release Process for Maintainers

### Creating a New Release

1. **Prepare artifacts** from the private development repository
2. **Generate checksums** for all binary files
3. **Create a new release** on GitHub:
   - Click "Create a new release" on the Releases page
   - Enter the version tag (e.g., `v1.0.0`)
   - Fill in the release title
   - Write comprehensive release notes (see template below)
   - Upload all artifacts and checksum files
   - Mark as pre-release if applicable
   - Publish the release

### Release Notes Template

```markdown
## Changes
- Feature: Description of new feature
- Fix: Description of bug fix
- Improvement: Description of improvement

## Breaking Changes
- List any breaking changes here

## Installation
1. Download the appropriate firmware file for your device
2. Verify the checksum
3. Follow the flashing instructions

## Known Issues
- List any known issues

## Checksums
SHA256 checksums for verification:
- firmware.bin: [checksum]
```

## Automation

This repository can be integrated with automated release workflows from the private development repository. Releases can be created automatically through:
- GitHub Actions workflows
- CI/CD pipelines
- Manual upload processes

## Support

For questions about the release process or specific releases, contact the development team through the appropriate channels.
