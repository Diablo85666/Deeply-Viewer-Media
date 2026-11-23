# Deeply Viewer Media Plugins

This public repository publishes the platform-specific media-plugin packs used by Deeply Viewer. The viewer downloads a pack only after the user agrees, verifies the archive's pinned size and SHA-256, checks the required plugin files, and installs it in the local media data folder.

## Downloads

The human-readable download page is published at:

<https://diablo85666.github.io/Deeply-Viewer-Media/media-plugins/>

Release assets are attached to the `media-plugins-N` GitHub releases. The viewer downloads its exact pinned archive directly from the release; the page is not part of the trust or verification path.

## Building and publishing

The `Media plugins` workflow builds the packs from the pinned Legacy Viewer source and package versions. It includes the corresponding license files and source archive with the release.

Run the workflow from the default branch with `publish` enabled to publish a new pack version. Published tags are immutable: increase `PACK_VERSION` before publishing another build. After a release is verified, update the matching version, archive size, and SHA-256 in Deeply Viewer's `crates/deeply-updater/src/media_pack.rs`.

Do not upload binaries assembled from an unverified installation or replace an existing release asset.
