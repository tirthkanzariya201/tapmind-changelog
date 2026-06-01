# Changelog Guidelines

Standards for documenting TapMind SDK releases in this repository.

## Version numbering

TapMind SDK versions follow [Semantic Versioning](https://semver.org/) (`MAJOR.MINOR.PATCH`), prefixed with `v` in changelog headings (e.g. `## v2.4.1`).

| Segment | When to increment | Examples |
|---------|-------------------|----------|
| **MAJOR** | Breaking API, integration, or behavior changes for integrators | Removed APIs, new minimum OS/SDK requirements that break existing apps |
| **MINOR** | Backward-compatible features or meaningful capability additions | New ad formats, new optional APIs, new mediation adapters |
| **PATCH** | Backward-compatible bug fixes and small improvements | Crash fixes, logging tweaks, adapter patch updates |

**Pre-release labels** (if used in distribution) should match release status:

- Beta builds: document under **Beta** status; version may include a suffix in release artifacts (e.g. `2.5.0-beta.1`) but changelog headings should still use the base version line when referring to the same release train.
- Experimental builds: document under **Experimental**; avoid implying production readiness.

Always use the **published** version string that integrators receive (Maven, CocoaPods, UPM, pub.dev, etc.).

## Release status definitions

Every release section must declare exactly one status.

### Stable

- Recommended for production integrations.
- Passed release QA and sign-off for the target platform/mediation.
- Breaking changes (if any) are documented and versioned with a MAJOR bump.
- Support expectations apply per TapMind’s public support policy.

### Beta

- Feature-complete or near-complete; intended for early adopters and staging environments.
- API or behavior may still change before Stable; document known limitations under **Notes**.
- Not recommended for production traffic without explicit approval.

### Experimental

- Early preview, internal dogfood, or limited rollout.
- APIs, behavior, and availability may change or be withdrawn without a MAJOR version policy guarantee.
- Use for proofs-of-concept only unless TapMind communications state otherwise.

## Changelog formatting standards

### File and heading structure

- One file per **platform + mediation** (e.g. `changelog/Flutter Android/AdMob.md`).
- File title: `# <Platform> - <Mediation>` (must match the template).
- Each release is a level-2 heading: `## vX.X.X` (newest release **first** at the top of the file, below the file title).

### Required fields per release

| Field | Requirement |
|-------|-------------|
| **Release Date** | ISO 8601 date (`YYYY-MM-DD`) or explicit “TBD” until published |
| **Release Status** | One of: Stable, Beta, Experimental (bullet list as in template) |
| **Sections** | Use only: Added, Improved, Fixed, Removed, Notes — omit empty sections or leave a single “None” bullet if nothing applies |

### Writing style

- Use present tense or past tense consistently within a file (prefer **past tense** for shipped releases: “Added interstitial preload API”).
- One bullet per distinct change; lead with the user-visible outcome.
- Link to migration guides or docs when breaking changes require integrator action.
- Include mediation- or platform-specific context (adapter versions, minimum OS) in **Notes** when relevant.

### What not to include

- Unreleased or internal-only work not yet available to integrators.
- Credentials, tokens, or private infrastructure details.
- Duplicate copy-paste across platform files unless the change truly applies identically—tailor bullets per stack when behavior differs.

### Template

Copy [CHANGELOG_TEMPLATE.md](CHANGELOG_TEMPLATE.md) for each new release block.

## Review checklist

Before merging a changelog PR:

- [ ] Correct platform/mediation file updated
- [ ] Version follows semver and matches the shipped artifact
- [ ] Release Date and Release Status are set
- [ ] Sections reflect customer impact (Added / Improved / Fixed / Removed / Notes)
- [ ] Newest version appears first in the file
- [ ] GitBook SUMMARY.md updated if new pages were added (not required for edits to existing pages)
