# Change Log
All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](http://keepachangelog.com/)
and this project adheres to [Semantic Versioning](http://semver.org/).

## [Unreleased]
### Added
- Created `CHANGELOG.md` file.
- Created `LICENSE` file.
- Created task to install `yum-cron` and configure autoupdates
- Exposed all Debian configuration items as variables
- Platforms added to meta.yml

### Changed
- Replaced generated values in `README.md` with accurate details.
- Update metadata for ansible role
- Run with become to allow install to succeed
- Prefix all variables with `autoupdate_`

### Fixed
- Ensure we run with `become: true`
- Fix typo
