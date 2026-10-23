# Clinical Vault releases

This repository is a download point. It holds only the files that the Clinical Vault Android app fetches when it checks for and installs its own updates:

* the signed Android package of each version (`.apk`),
* the signed release description (`latest.cvu`), which tells the app which version is current and which file and signer are authorised,
* short release notes.

It contains no source code, no signing keys, no configuration and no patient data, and nothing is ever stored here by the app.

Clinical Vault is a **development build for invented data only. It is not cleared for clinical use.**

How a release is made: each version has a release named `cv-<version code>` that carries its package and description. Every few weeks the description is renewed (its signature has a limited validity period); a renewal is a separate release named `cv-<version code>-renewal-<time>` that carries only the renewed description. Published releases are never edited or deleted. The app checks the signature, the size and the SHA-256 of what it downloads, and Android checks the package signature again before installing, so a file placed here by anyone else would be rejected.
