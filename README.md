# Debrfs | [![License](https://img.shields.io/badge/License-BSD_3--Clause-blue.svg)](https://opensource.org/licenses/BSD-3-Clause)

<p align="center">
  <img width="128" height="128" src="https://raw.githubusercontent.com/Nitrux/luv-icon-theme/master/Luv/places/64/folder-red.svg">
</p>

# Introduction

Create small Debian rootfs TAR files using `debbootstrap`.

> [!WARNING]
> `debrfs` does not work in unprivileged containers.

# Usage

Move `debrfs` to the `$PATH` and open a terminal:

```sh
debrfs create --config <file.conf>
```

Alternatively, place a config file in `/etc/debrfs.d/` and the utility will build it.

# Licensing

The repository and its contents are licensed under **BSD-3-Clause**.

# Issues

If any problems are encountered, users can create an issue.

©2022 Nitrux Latinoamericana S.C.
