# Squashed Mainsail

## SYNOPSIS

Tooling for and squashfs releases of [Mainsail](https://github.com/mainsail-crew/mainsail)

## Squashes

The squash bundles are world-readable, owned by root, and all timestamps are set to that of the commit it was built from.

The `-stock` squash is comparable to the `mainsail.zip` provided by upstream.

The `-prefix` squash is built to be served at `/mainasil`.

## Building

On a system with `make`, `git`, `podman`, `mksquashfs`, and at least 1000 subuids/subgids for the current user:

```bash
git clone https://github.com/Laikulo/mainsail-squashed.git
cd mainsail-squashed.git
make
```

## Usage

```bash
mount mainsail-VERSION-prefix.sfs /srv/www/mainsail
```

## Prebuild squashes
Only full releases from upstream will be published here, they will be attached to github releases with the same name as the parent project.

The tags of these releases will point to the tool version that was used to build them, including an upstream-ref. This may not be the tooling used to create teh github release itself.

## Release Cadence

There is currently no offical timeline, but three business days after the upstream release (excluding vacation/holidays) is an aspirational goal.
