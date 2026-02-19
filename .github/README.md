# Maintainer Documentation

This directory contains templates and configurations for managing the release repository.

## Contents

- **ISSUE_TEMPLATE/**: Issue templates for users reporting release-related problems
- **PULL_REQUEST_TEMPLATE.md**: PR template discouraging code contributions
- **RELEASE_TEMPLATE.md**: Template for creating new releases with proper formatting
- **workflows/**: GitHub Actions workflows (if any automation is added)

## Quick Links for Maintainers

### Creating a New Release

1. Review [RELEASE_TEMPLATE.md](RELEASE_TEMPLATE.md) for the release notes template
2. Go to the [Releases page](../../releases)
3. Click "Draft a new release"
4. Follow the template and upload all required artifacts

### Managing Issues

Issue templates guide users to provide necessary information:
- Release version
- Issue type (download, checksum, installation, etc.)
- Detailed description

### Managing Pull Requests

The PR template automatically reminds contributors that:
- This is a release-only repository
- Code contributions should go to the main development repo
- Only documentation and infrastructure PRs are acceptable

## Repository Configuration Recommendations

### Protected Branches

Consider protecting the main branch:
- Require pull request reviews
- Require status checks to pass
- Restrict who can push

### GitHub Actions

Potential automation workflows:
- Auto-generate checksums when releases are created
- Validate release asset naming conventions
- Notify teams when new releases are published
- Archive old releases automatically

### Repository Settings

Recommended settings:
- Disable wiki (not needed for release-only repo)
- Enable discussions if you want community Q&A
- Configure release notifications
- Set up security advisories

## Best Practices

### Release Cadence
- Follow semantic versioning
- Maintain a regular release schedule when possible
- Communicate release schedules to users

### Asset Management
- Keep release assets organized
- Delete draft releases that won't be published
- Archive very old releases if needed

### Documentation
- Keep README.md up to date
- Update RELEASES.md with each new release
- Maintain SECURITY.md for security policies

### Communication
- Use release notes to communicate changes clearly
- Respond to issues promptly
- Update documentation based on user feedback

## Automation Ideas

Consider adding workflows for:
1. **Checksum verification**: Auto-verify checksums on release creation
2. **Asset validation**: Check that all required files are present
3. **Notification**: Send notifications to relevant channels
4. **Changelog generation**: Auto-generate changelogs from commits
5. **Metrics**: Track download counts and popular releases

## Security Considerations

- Never commit secrets or API keys
- Verify all release artifacts before publishing
- Review contributions carefully
- Use signed commits for release tags
- Enable 2FA for all maintainers

## Support

For questions about maintaining this repository:
- Review the main [README.md](../README.md)
- Check [RELEASES.md](../RELEASES.md) for release process
- Contact other maintainers
