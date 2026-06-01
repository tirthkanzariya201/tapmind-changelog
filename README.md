# TapMind SDK Changelog

This repository is for **release tracking and changelog publishing only**. It does not contain SDK source code. Changelogs are maintained in Git and published through [GitBook](https://www.gitbook.com/) via Git Sync.

## How changelogs are organized

### Per platform

Changelogs are maintained **per platform**, one file each under `changelog/`:

| File | Platform |
|------|----------|
| [Native Android.md](changelog/Native%20Android.md) | Native Android |
| [Native iOS.md](changelog/Native%20iOS.md) | Native iOS |
| [Unity.md](changelog/Unity.md) | Unity |
| Flutter (per mediation) | [AdMob & GAM](<changelog/Flutter - AdMob & Google Ad Manager (GAM).md>), [AppLovin MAX](<changelog/Flutter - AppLovin MAX.md>), [ironSource LevelPlay](<changelog/Flutter - ironSource LevelPlay.md>) |
| [Cocos.md](changelog/Cocos.md) | Cocos |

Each file documents every public release for that platform in reverse chronological order (newest first).

### Platform-specific versions

**Version numbers are not shared across platforms.** A `v2.1.0` on Native Android is independent from `v2.1.0` on Unity or Flutter. Versions reflect the release train for that platform only and should match the artifact integrators install (Maven, CocoaPods, UPM, pub.dev, etc.).

### Mediation support per release

A single release may support **one or more** mediation partners. For every release entry you must list which mediations are included under **Supported Mediations** (AdMob, Google Ad Manager (GAM), AppLovin MAX, LevelPlay). Only document changes that apply to the mediations listed for that release.

### Release metadata

Each release block includes:

- **Release Date** — ISO date when published (`YYYY-MM-DD`)
- **Release Status** — Stable, Beta, or Experimental
- **Supported Mediations** — required checklist for that build
- **Added / Improved / Fixed / Removed / Notes** — customer-facing changes

See [CHANGELOG_GUIDELINES.md](CHANGELOG_GUIDELINES.md) and [CHANGELOG_TEMPLATE.md](CHANGELOG_TEMPLATE.md) for formatting and status definitions.

## GitBook

`.gitbook.yaml` and `SUMMARY.md` configure Git Sync. Edit changelog content in this repository—not in the GitBook editor for synced pages—to avoid conflicts. See [GitBook content configuration](https://gitbook.com/docs/getting-started/git-sync/content-configuration).

## Contributing

1. Open the changelog file for the target platform.
2. Add a new `## vX.X.X` section at the top (below the file title), using the template.
3. Set supported mediations, status, and change sections.
4. Open a pull request and merge to `main` for GitBook to sync.
