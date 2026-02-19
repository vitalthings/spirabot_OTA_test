# Release Note Template

Use this template when creating a new release on GitHub.

---

## Release Title
`Spirabot OTA Firmware v{VERSION}`

Example: `Spirabot OTA Firmware v1.2.0`

---

## Release Notes Body

```markdown
# Spirabot OTA Firmware v{VERSION}

## 📦 Release Information

**Release Date**: {DATE}  
**Release Type**: {Stable/Pre-release/Beta/RC}  
**Previous Version**: v{PREVIOUS_VERSION}

## ✨ What's New

### Features
- **Feature Name**: Brief description of the new feature
- **Another Feature**: Description

### Improvements
- Improved performance in {area}
- Enhanced {functionality}
- Updated {component}

### Bug Fixes
- Fixed issue where {description} (#issue-number if applicable)
- Resolved {bug description}
- Corrected {problem}

## ⚠️ Breaking Changes

{If none, write "None" - otherwise list breaking changes}

- **Change 1**: Description and migration instructions
- **Change 2**: Description and migration instructions

## 🔧 Installation Instructions

### Prerequisites
- {List any prerequisites}
- {Required tools or knowledge}

### Installation Steps

1. **Download** the appropriate firmware file for your device:
   - `spirabot-firmware-v{VERSION}-{PLATFORM}.bin` - for {platform description}

2. **Verify** the download using the SHA256 checksum:
   ```bash
   # Linux/Mac
   sha256sum -c spirabot-firmware-v{VERSION}-{PLATFORM}.bin.sha256
   
   # Windows PowerShell
   Get-FileHash spirabot-firmware-v{VERSION}-{PLATFORM}.bin -Algorithm SHA256
   ```

3. **Flash** the firmware to your device:
   - {Provide specific flashing instructions}
   - {Tool commands or GUI instructions}

4. **Verify** successful installation after reboot

### Upgrade Notes

{Any special notes for upgrading from previous versions}

## 📋 Release Assets

### Firmware Files

| File | Description | SHA256 |
|------|-------------|---------|
| `spirabot-firmware-v{VERSION}-{PLATFORM}.bin` | Main firmware binary | See checksum file |
| `spirabot-firmware-v{VERSION}-{PLATFORM}.bin.sha256` | SHA256 checksum | - |

## ⚙️ Technical Details

- **Firmware Size**: {SIZE} KB/MB
- **Supported Hardware**: {List supported hardware versions}
- **Minimum Requirements**: {Any minimum requirements}

## 🐛 Known Issues

{List known issues, or write "None currently identified"}

- **Issue 1**: Description and workaround if available
- **Issue 2**: Description and workaround if available

## 🔒 Security

{If this release includes security fixes}

This release includes security updates. Users are encouraged to upgrade as soon as possible.

- **CVE-XXXX-XXXX**: {Description if applicable}
- Security fix for {vulnerability description}

{If no security issues}
No security issues addressed in this release.

## 📚 Additional Resources

- [Documentation](link-to-docs)
- [RELEASES.md](../RELEASES.md) - Release management information
- [SECURITY.md](../SECURITY.md) - Security policy

## 🙏 Acknowledgments

{Optional: Thank contributors, testers, or community members}

## 📞 Support

For issues or questions:
- Review the [README](../README.md)
- Check [existing issues](../../issues)
- Contact the development team through appropriate channels

---

**Full Changelog**: {link to compare, e.g., v1.1.0...v1.2.0}
```

---

## Checklist Before Publishing

- [ ] All firmware binaries are built and tested
- [ ] SHA256 checksum files generated for all binaries
- [ ] Release notes are complete and accurate
- [ ] Version tag follows semver (e.g., v1.2.0)
- [ ] All assets are uploaded
- [ ] Breaking changes are clearly documented
- [ ] Installation instructions are clear
- [ ] Known issues are documented
- [ ] Pre-release checkbox is set correctly
- [ ] Release is reviewed by at least one other maintainer

---

## Quick Release Checklist

1. ✅ Tag version created (e.g., `v1.2.0`)
2. ✅ Release title set
3. ✅ Release notes written
4. ✅ Firmware binaries uploaded
5. ✅ Checksum files uploaded
6. ✅ Pre-release marked if applicable
7. ✅ Published!
