# TapMind SDK Changelog

Official release notes and changelogs for the TapMind SDK, organized by **platform** and **mediation** partner.

This repository is the single source of truth for what shipped in each TapMind SDK release. Content is maintained in Git and published to readers through [GitBook](https://www.gitbook.com/) via Git Sync.

## Purpose

- Store release notes and changelogs only (no SDK source code)
- Publish changelogs through GitBook for product and developer-facing documentation
- Track releases consistently by **Platform** (Native, Unity, Flutter, Cocos × Android/iOS) and **Mediation** (AdMob, GAM, AppLovin, LevelPlay)

## Repository layout

```
changelog/
├── Native Android/     ├── Native iOS/
├── Unity Android/      ├── Unity iOS/
├── Flutter Android/    ├── Flutter iOS/
└── Cocos Android/      └── Cocos iOS/

Each platform folder contains one markdown file per mediation:
AdMob.md · GAM.md · AppLovin.md · LevelPlay.md
```

Browse the [changelog index](changelog/) or use **SUMMARY.md** (GitBook table of contents) for navigation.

## Changelog ownership

| Role | Responsibility |
|------|----------------|
| **Release owner** | Ensures a changelog entry exists for every public SDK release on their platform/mediation track |
| **Engineering** | Provides accurate Added / Improved / Fixed / Removed / Notes content |
| **Product / PM** | Approves release status (Stable, Beta, Experimental) and customer-facing wording |
| **Docs / DevRel** | Reviews GitBook rendering and cross-links after Git Sync |

Changes are made via pull request to this repository. Do not edit the same release section in GitBook’s UI when Git Sync is enabled—edit markdown here and let sync propagate.

## Release tracking methodology

1. **Identify scope** — Determine platform (e.g. Unity Android) and mediation (e.g. LevelPlay) for the release.
2. **Open the correct file** — `changelog/<Platform>/<Mediation>.md`.
3. **Add a new version block** — Use [CHANGELOG_TEMPLATE.md](CHANGELOG_TEMPLATE.md) and follow [CHANGELOG_GUIDELINES.md](CHANGELOG_GUIDELINES.md).
4. **Set release metadata** — Version (`vX.X.X`), release date, and status (Stable / Beta / Experimental).
5. **Merge to default branch** — GitBook Git Sync publishes updates to the connected space.
6. **Verify on GitBook** — Confirm TOC, headings, and links render as expected.

Releases are tracked **per platform and mediation**. The same SDK version number may appear in multiple files when that build supports multiple stacks; each file should only describe changes relevant to that platform/mediation combination.

## Contributing

- Read [CHANGELOG_GUIDELINES.md](CHANGELOG_GUIDELINES.md) before adding entries.
- Copy [CHANGELOG_TEMPLATE.md](CHANGELOG_TEMPLATE.md) for each new release section.
- Do not commit secrets, internal URLs, or unreleased roadmap items.

## GitBook

This repo includes `.gitbook.yaml` and `SUMMARY.md` for Git Sync. Connect the GitHub repository in your GitBook space and enable bidirectional or export sync per your team’s workflow. See [GitBook content configuration](https://gitbook.com/docs/getting-started/git-sync/content-configuration).
