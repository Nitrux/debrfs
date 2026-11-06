# Debrfs | [![License](https://img.shields.io/badge/License-BSD_3--Clause-blue.svg)](https://opensource.org/licenses/BSD-3-Clause)

<p align="center">
  <img width="128" height="128" src="https://raw.githubusercontent.com/Nitrux/luv-icon-theme/master/Luv/places/64/folder-red.svg">
</p>

# Introduction

Create small Debian rootfs TAR files using [mmdebstrap](https://manpages.debian.org/mmdebstrap).

> [!WARNING]
> `debrfs` does not work in unprivileged containers.

# Usage

Install `mmdebstrap`, move `debrfs` to your `$PATH`, and run:

```sh
sudo debrfs create --conf <file.conf>
```

Use `--dbg-db` to show mmdebstrap and archive output while troubleshooting. Alternatively, place a config file in `/etc/debrfs.d/` and run `sudo debrfs create`.

Set `ROOTFS_MIRROR` to one repository URL or a comma-separated list for the configured suite. Set `ROOTFS_REPOSITORY_PRIORITIES` to comma-separated `host:priority` entries to assign APT repository priorities before package resolution. `ROOTFS_KEYRING_URL` accepts one or more comma-separated HTTPS key URLs; `ROOTFS_KEYRING` accepts an existing keyring file or directory. When a custom keyring is configured, debrfs copies it into the rootfs APT trusted keyring directory, skips mmdebstrap’s automatic `Signed-By` selection, and uses `gpgv` to verify repository signatures, including signatures made by subkeys.

# Licensing

The repository and its contents are licensed under **BSD-3-Clause**.

# Issues

If any problems are encountered, users can create an issue.

©2022 Nitrux Latinoamericana S.C.
