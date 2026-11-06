# zenkit-releases

Signed binaries of the ZenKit executor and launcher. No source code lives here.

## What is published

Each release contains:

- the executor binary for Windows x64
- `SHA256SUMS`: the SHA-256 hash of every file in the release
- `SHA256SUMS.sig`: the signature of `SHA256SUMS`

## Trust

The launcher refuses any file whose hash is missing from `SHA256SUMS` or whose
`SHA256SUMS.sig` does not verify against the public key built into the launcher.
The signing key never lives in this repository or in GitHub.

A binary from this repository does nothing without a NexusCore account key.
No secret is ever embedded in a published file.

## Rollout

A new version runs on the operator's machine for 24 hours, then reaches other
machines only after the operator approves it.
