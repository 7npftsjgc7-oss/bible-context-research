# Changelog

All notable changes to Bible Context Research are recorded here.

## [0.2.0] - 2026-08-06

### Added

- Detailed Hebrew, Aramaic, and Greek pronunciation and audio behavior.
- Verified Blue Letter Bible Strong's pronunciation links as a required pronunciation resource when available.
- Capability-aware native inline pronunciation controls with written-pronunciation fallback.
- Multiword-expression and inflected-form handling that keeps Strong's links lexical.
- Pronunciation-tradition guidance for Hebrew, Aramaic, and Greek.
- Explicit distinction between יהוה (`YHWH`) and the traditional reading `Adonai`.
- Uncertain lexical-identification safeguards and generated-audio labeling rules.
- Formal pronunciation and audio synchronization QA record.

### Changed

- README documentation now describes pronunciation output and downstream synchronization behavior.
- Installed skill, three Bible-study projects, and Custom GPT instructions were synchronized manually and user-tested.

### Known limitations

- Native inline pronunciation controls depend on the current ChatGPT environment.
- Downstream copies do not update automatically from merged `main`.
- No automated CI workflow currently tests pronunciation behavior.
- External synthetic-audio integrations remain unverified.

## [0.1.0]

- Initial plugin and `research-bible-context` skill release.
