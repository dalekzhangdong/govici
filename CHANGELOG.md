# Changelog
All notable changes to govici will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/).

## [v0.4.0] - 2020-07-03

### Added
- CHANGELOG.md particularly to help track API changes pre-v0.1.0.
- Session.Subscribe/Unsubscribe/UnsubscribeAll APIs for event subscription.
- WithAddr SessionOption to specify address that charon is listening on.
- WithDialContext SessionOption to provide a dial func to Session.
- Expose Event type with exported Name and Message fields.
- Add a timestamp to Event type.

### Changed
- Behavior of event registration. Package users can now subscribe/unsubscribe at
  any time while the Session is active.
- Event listener is always active, and the same listen() loop now services event
  registration responses as well as event packets.
- NextEvent accepts a context.Context so that it can be cancelled by the caller.

### Removed
- Session.Listen API.

[Unreleased]: https://github.com/strongswan/govici/compare/v0.4.0...HEAD
[v0.4.0]: https://github.com/strongswan/govici/compare/v0.3.0...v0.4.0
