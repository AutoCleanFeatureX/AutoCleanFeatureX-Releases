# AutoCleanFeatureX Releases

Official public binary distribution and signed update metadata for AutoCleanFeatureX desktop applications by Elmo.

**This repository is for public releases only. Application source code is maintained in the private `AutoCleanFeatureX-Source` repository.**

## Download

Open the [GitHub Releases page](https://github.com/AutoCleanFeatureX/AutoCleanFeatureX-Releases/releases) and choose the package matching your operating system and CPU architecture. Release assets are public downloads.

## Automatic updates

AutoCleanFeatureX reads the signed `update_manifest.json` from the root of the `main` branch over HTTPS, then downloads package assets from this repository's GitHub Releases. Keep this repository name, owner, and `main` branch unchanged unless every installed application is rebuilt with a new manifest URL.

## Repository contents

- `update_manifest.json` — signed manifest consumed by installed applications.
- GitHub Releases assets — platform ZIPs, `CHECKSUMS.txt`, and release notes.

Do not commit source code, tests, build scripts, private signing keys, `config.ini`, `network_settings.json`, `.env`, credentials, or user-specific runtime files here.

## Security

Manifests are signed with Ed25519. The application verifies the signature and package SHA-256/size before installation. SHA-256 checks integrity; Ed25519 authenticates the manifest. Public release ZIPs are downloadable by anyone and are not DRM or per-user access control.
