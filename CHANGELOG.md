# Changelog

All notable changes to the Chops Mobile Blocklist will be documented here.

## [1.2.0] - 2026-06-15
### Fixed
- Commented out all Amazon Alexa endpoint blocks
  - unagi-na.amazon.com confirmed as Blink Sync Module 2 cloud keepalive
  - Amazon routes Blink and Alexa core connectivity through telemetry-labeled domains
  - Blocking causes Sync Module cloud session failures at the DNS level
  - Affected: device-metrics-us.amazon.com, unagi.amazon.com, unagi-na.amazon.com, msh.amazon.com
- Commented out Blink telemetry blocks
  - Blink backend update (June 2026) shifted core connectivity to telemetry endpoints
  - Affected: telemetry.blinkforhome.com, metrics.blinkforhome.com

### Notes
- If running HaGeZi or similar aggressive lists alongside this one, add to AdGuard Home
  custom filtering rules:
    @@||unagi-na.amazon.com^
    @@||immedia-semi.com^
    @@||blinkforhome.com^

## [1.1.0] - 2026-05-30
### Fixed
- Removed full duplicate block that was appended to the UNCLASSIFIED staging section
- Added breakage warnings to `sentry.io` and `branch.io`

## [1.0.0] - 2026-05-29
### Added
- Initial release
- Section A: DNS-layer rules for AdGuard Home, NextDNS, Control D, RethinkDNS
- Section B: Browser-extension-only rules for uBlock Origin and AdGuard extensions
- Coverage: Social, Retail, IoT, Gaming, Streaming, AI, OEM, Automotive, Attribution, Analytics
- Custom staging triage block for testing new entries
