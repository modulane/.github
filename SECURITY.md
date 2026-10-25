# Security Policy

This policy applies to every repository in the Modulane organisation that does not have its own `SECURITY.md`.

## Reporting a vulnerability

**Never open a public issue, discussion or pull request for a security vulnerability.**

Report it privately instead:

1. Open the **Security** tab of the affected repository.
2. Select **Report a vulnerability**.
3. Describe the issue, how to reproduce it, the affected versions and the impact you expect.

You will receive an initial response within 72 hours. Please allow a reasonable amount of time for a fix to be released before you disclose the vulnerability publicly.

## Supported versions

Security fixes are released for the latest version of each tool. Update to the latest version before reporting, and check that the issue still occurs.

Once a tool reaches 1.0.0, the previous major version also receives critical security fixes for 6 months after the next major version is released. The Modulane maintainer may change this policy.

A repository's own `SECURITY.md` may list different supported versions.

## Verifying releases

Packages that Modulane repositories publish to npm are built and published by GitHub Actions with [npm trusted publishing](https://docs.npmjs.com/trusted-publishers). Each one carries a provenance attestation that links it to the source commit and the workflow run that built it. You can verify the packages you have installed with:

```bash
npm audit signatures
```
