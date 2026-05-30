# Known Breakage Reference

Rules in this list that are known to break legitimate app functionality.
Check this before deploying aggressively or troubleshooting issues.

| Domain | Section | Risk | Notes |
|---|---|---|---|
| `sentry.io` | Crash Reporting | Medium | Used by many apps for legitimate error recovery, not just telemetry. May break app stability reporting. |
| `branch.io` | Attribution | Medium | Handles deep linking and password reset flows in addition to tracking. May break invite links and auth redirects. |
| `a.slack-edge.com` | Communications | High | Breaks Slack UI assets. Slack will not render correctly. |
| `realtime.linkedin.com` | Social | High | Breaks LinkedIn real-time functionality. |
| `heytap.com` / `heytapmobile.com` | OEM | Critical | Breaks OnePlus/OPPO OTA system updates. Do not block if on these devices. |
| `netskrt.net` | Streaming | Medium | CDN acceleration layer for Peacock stream delivery. May cause buffering. |
| `connectapi.garmin.com` | Fitness | High | Breaks Garmin fitness data cloud syncing entirely. |
| `unityads.unity3d.com` | Gaming | Medium | Some games use Unity for core rendering, not just ads. Test per game. |
| `firebaseremoteconfig.googleapis.com` | Firebase | Medium | Used by many apps for remote configuration, not just tracking. May break app behavior. |
