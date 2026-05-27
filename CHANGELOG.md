# Changelog

## 1.1.0 — 2026-05-27

### Added

- `ignore` input: newline-separated list of package names to skip during check or fix.

### Fixed

- Pinned `astral-sh/setup-uv` to `v8.1.0` (major-version aliases aren't published).
- Removed `--yes` flag from `fix` invocation (flag doesn't exist in chill-out).

----

## 1.0.0 — 2026-05-08

### Added

- Initial release of `chill-out-action` as a composite GitHub Action.
- `check` command:
  - audits the lockfile
  - fails the job if any package is inside the cooldown window.
- `fix` command:
  - pins violating packages to the newest safe version
  - commits to a `fix/chill-out-<timestamp>` branch
  - opens a PR against the default branch
  - reuses an existing fix PR if one is already open.
