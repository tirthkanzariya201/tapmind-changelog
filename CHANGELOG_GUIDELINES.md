# Changelog Guidelines

Standards for TapMind SDK release notes in this repository.

## Scope

- One changelog file per **platform** (`changelog/Native Android.md`, `changelog/Unity.md`, etc.).
- **Version numbers are platform-specific** and are not reused as a global SDK version across platforms.
- Each release entry must list **Supported Mediations** for that build (one or more of AdMob, GAM, AppLovin MAX, LevelPlay).

## Version numbering

Follow [Semantic Versioning](https://semver.org/) (`MAJOR.MINOR.PATCH`), prefixed with `v` in headings (e.g. `## v2.4.1`).

| Segment | When to increment |
|---------|-------------------|
| **MAJOR** | Breaking changes for integrators on that platform |
| **MINOR** | Backward-compatible features |
| **PATCH** | Backward-compatible fixes |

Use the version string published for that platform’s artifact only.

## Release status

| Status | Meaning |
|--------|---------|
| **Stable** | Production-ready; passed release QA |
| **Beta** | Early adopters / staging; may change before Stable |
| **Experimental** | Preview only; not for production unless explicitly approved |

Mark exactly one status per release (check the applicable bullet).

## Formatting

- Add new releases **below the file title**, newest first.
- Copy the block from [CHANGELOG_TEMPLATE.md](CHANGELOG_TEMPLATE.md).
- List only mediations that ship in that release under **Supported Mediations**.
- Leave change sections empty or omit bullets when nothing applies.
- Do not include unreleased work, secrets, or internal-only details.

## Review checklist

- [ ] Correct platform file updated
- [ ] Version matches that platform’s published artifact
- [ ] Supported Mediations accurately reflect the build
- [ ] Release Date and Release Status set
- [ ] Added / Improved / Fixed / Removed / Notes are accurate
