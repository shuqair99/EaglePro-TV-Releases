# EAGLE PRO — Samsung Tizen TV

This repository is the release/staging repository for the Samsung Tizen TV port of EAGLE PRO.

## Scope

- Samsung Tizen TV WGT packages only.
- The original Android and Windows projects remain in the separate `Eagle_Pro` repository.
- TV-only changes: remove radio recording and the promotional video.
- Preserve the radio station list, favourites, and the real audio visualizer where the target TV runtime supports the required audio APIs.
- TV remote navigation must be tested on actual hardware before a build is described as production-ready.

## Build status

The source repository currently produces an **unsigned WGT packaging artifact** through GitHub Actions. It is a build-validation artifact, not yet a signed, install-ready release.

The current package validation checks:
- Tizen `config.xml` parses as XML.
- Core web pages are present.
- Recording and promotional-video assets are absent from the TV package.
- The WGT archive passes ZIP integrity testing.

## Important compatibility notes

- Tizen generations differ substantially. A package declaring an older minimum version does not prove compatibility with every TV model.
- Playback must be validated against Samsung AVPlay and supported codecs/protocols.
- A browser-based audio visualizer must be connected to real audio samples; no simulated animation is acceptable.
- Apps2Samsung's catalog reads release metadata from its own upstream `third-party-apps.json`. Listing EAGLE PRO there requires an upstream catalog contribution/acceptance; merely creating this repository does not add it to the catalog.
- Apps2Samsung currently consumes public GitHub release endpoints in its catalog. This private staging repository will not be discoverable by that public catalog until a public distribution path is chosen.

## Release policy

Do not publish an artifact as a stable release until it is:
1. Built from the audited source.
2. Signed using a supported Samsung/Tizen installation path.
3. Tested for installation and remote navigation.
4. Tested for actual radio/audio playback on target TVs.
5. Checked for absence of recording and promotional-video functionality.

