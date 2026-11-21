# EAGLE PRO — Samsung Tizen TV

Official release channel for the Samsung Tizen TV edition of EAGLE PRO.

- **App name:** EAGLE PRO
- **Platform:** Samsung Tizen Smart TV
- **Package format:** WGT
- **Release feed:** https://api.github.com/repos/shuqair99/EaglePro-TV-Releases/releases
- **Original project:** maintained separately in the private `Eagle_Pro` repository.

## Scope of this repository

This repository is for TV builds and release metadata only. It must not contain the original Android/Windows project, credentials, subscription lists, private server URLs, or customer data.

The TV edition must omit:
- Radio recording and all recording controls/engines.
- The promotional video added in the latest update and its player/launcher code.

The TV edition must retain:
- Radio station browsing and playback.
- Favourites.
- A real audio visualizer driven by actual playback audio data (never simulated bars).
- TV remote navigation.

## Build and validation status

The current build pipeline in the private source repository has produced an **unsigned WGT packaging artifact** and validated its ZIP integrity and XML manifest. This is not yet a signed, hardware-tested production release.

Before publishing a stable release, verify:
1. The WGT installs through the intended Apps2Samsung installation flow.
2. Remote navigation works on physical Samsung TVs.
3. Radio streams play through the supported Samsung TV playback path.
4. The visualizer reacts to actual audio samples.
5. Recording and promotional-video functionality are absent.
6. Compatibility is tested separately across supported Tizen generations.

## Apps2Samsung catalog

Apps2Samsung reads third-party providers from its upstream `third-party-apps.json` file. This repository's Releases API is the intended provider endpoint, but EAGLE PRO will not appear in the Apps2Samsung catalog until its maintainers accept a catalog contribution.

Provider metadata proposal: [apps2samsung-provider.json](./apps2samsung-provider.json).

## Releases

Stable WGT files will be attached to GitHub Releases in this repository only after signing/install-path validation and real-device testing.
