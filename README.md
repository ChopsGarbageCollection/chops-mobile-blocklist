# Chops Mobile Blocklist

A master blocklist engineered to neutralize mobile application telemetry, bloatware, and tracking domains. This project provides a transparent, documented approach to privacy by explaining exactly what is being blocked and why, rather than relying on black-box filters.

## Technical Overview
* **Focus:** Mobile application telemetry and OS hardening.
* **Cross-Platform utility:** While designed for mobile, these rules neutralize tracking endpoints shared by premium desktop clients including Discord, Steam, Spotify, Slack, Zoom, and Office 365.
* **Maintenance:** Maintained by Chops.

## Supported Platforms
The blocklist is compatible with the following engines:
* **Browser Extensions:** uBlock Origin (Desktop & Mobile) and Brave Shields.
* **Network-Level Firewalls:** AdGuard Home, NextDNS, and Control D.
* **Android Clients:** RethinkDNS.

## Categorized Coverage
This blocklist targets telemetry, analytics, and tracking across the following domains:

* **Social & Communications:** TikTok, Meta (Facebook/Instagram), X, Snapchat, LinkedIn, Reddit, Discord, Telegram, Zoom, and Slack.
* **Retail & Commerce:** Walmart, Sam's Club, Meijer, eBay, Temu, Best Buy, Newegg, Micro Center, Target, and various fast-food/quick-service chains.
* **Smart Home & IoT:** Geeni/Tuya, DDLock, Govee, GE Cync, Blink, Amazon Alexa, and Bambu Lab.
* **Gaming & OTT:** Steam, Battle.net, Epic Games, GOG, Roblox, Twitch, Netflix, Roku, Plex, Tubi, and major streaming services (Disney+, Paramount+, etc.).
* **AI & Productivity:** OpenAI (ChatGPT), Google (Gemini), Anthropic (Claude), DeepSeek, Perplexity, and Microsoft Copilot.
* **Hardware & Automotive:** Apple, OnePlus/OPPO, Motorola, Nothing, TCL, Tesla, Ford, GM, Honda, and Toyota.
* **Infrastructure & Analytics:** General telemetry from mobile carriers (T-Mobile), weather services, crash reporting (Sentry/Bugsnag), and common attribution/ad-mediation networks (AppsFlyer, Adjust, Kochava, etc.).

## Implementation
### Section A: DNS-Layer Rules
Compatible with all listed platforms. These rules utilize naked wildcard domains (no paths, no mid-line asterisks) to ensure maximum compatibility across DNS-level cloud firewalls.

### Section B: Browser-Extension Rules
Compatible exclusively with uBlock Origin and AdGuard browser extensions. These rules contain exact paths and inline wildcards required for granular blocking that network-level DNS software cannot interpret.

## Usage Notes
* **HTTPS Filtering:** For services that utilize DNS-over-HTTPS (DoH) to bypass filters—such as TikTok—you must enable HTTPS filtering within your AdGuard settings to ensure effectiveness.
* **Critical Infrastructure:** Exercise caution with OEM-specific rules. For example, blocking OnePlus or OPPO root domains will break OTA system updates.
* **Dependencies:** Some platforms, such as Roblox, use telemetry domains for required game asset loading; ensure your specific use case allows for these before applying aggressive filters.

## License
This project is released under the MIT License.

