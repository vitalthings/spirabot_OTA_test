# Security Policy

## Purpose

This repository is a release distribution repository for Spirabot OTA firmware. It contains only compiled binaries and release artifacts.

## Supported Versions

Security updates are provided for the following release versions:

| Version | Supported          |
| ------- | ------------------ |
| Latest  | :white_check_mark: |
| Previous Minor | :white_check_mark: |
| Older   | :x:                |

We recommend always using the latest stable release for the best security and features.

## Reporting a Vulnerability

If you discover a security vulnerability in any of the releases:

### For Release Distribution Issues

If the security issue is related to:
- Compromised release artifacts
- Incorrect checksums
- Tampered binaries
- Distribution infrastructure

Please report it immediately to the repository maintainers through GitHub's private security advisory feature.

### For Firmware Vulnerabilities

If the security issue is related to:
- Firmware code vulnerabilities
- Security flaws in the device software
- Cryptographic issues
- Authentication/authorization problems

Please contact the development team directly through secure channels (not through this public repository).

## Verification

All release artifacts should be verified before installation:

1. **Verify Checksums**: Always verify SHA256 checksums provided with each release
2. **Check Signatures**: Verify digital signatures where applicable
3. **Official Sources Only**: Download releases only from the official GitHub Releases page
4. **HTTPS Only**: Ensure you're downloading over HTTPS

### Verifying a Release

```bash
# Download the firmware and checksum file
# Verify on Linux/Mac:
sha256sum -c firmware.bin.sha256

# Verify on Windows (PowerShell):
Get-FileHash firmware.bin -Algorithm SHA256
# Compare output with the .sha256 file content
```

## Security Updates

When security vulnerabilities are fixed:
- A new release will be published with the fixes
- The release notes will indicate it's a security update
- Affected versions will be documented
- Users are encouraged to upgrade immediately

## Best Practices

When using releases from this repository:
- ✅ Always verify checksums before flashing firmware
- ✅ Keep firmware up to date
- ✅ Use official releases only
- ✅ Review release notes for security advisories
- ❌ Never use pre-release/beta versions in production unless necessary
- ❌ Never modify release binaries
- ❌ Don't download releases from unofficial sources

## Responsible Disclosure

We follow responsible disclosure practices:
- Security issues are handled privately until a fix is released
- Credit is given to security researchers (with permission)
- Users are notified of security updates through release notes

## Questions

For questions about security:
- Check release notes for security advisories
- Review the [RELEASES.md](RELEASES.md) documentation
- Contact maintainers through appropriate secure channels
