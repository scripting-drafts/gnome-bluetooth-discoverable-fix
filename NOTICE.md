# NOTICE

These are unofficial modified rebuilds of Ubuntu 22.04 packages.

- `libgnome-bluetooth13` 3.34.5-8+local2
  from gnome-bluetooth 3.34.5-8 (Settings panel)
- `libgnome-bluetooth-3.0-13` 42.0-5+local2
  from gnome-bluetooth3 42.0-5 (GNOME Shell)

The changes are limited to the patches in `patches/`: both GNOME clients now
send `Discoverable=false` instead of asking BlueZ to advertise the machine
while scanning.

These packages are not produced, endorsed, or supported by Ubuntu, Canonical,
Debian, or the GNOME Project. They retain the upstream license; each package
contains its Debian copyright file. Exact source URLs and checksums are in
`SOURCE`; build steps are in `BUILDING.md`.

The `+localN` suffix marks the local modification (current build: `+local2`).
It follows the `dch --local` convention for non-official local rebuilds;
official Ubuntu revisions use `ubuntuN`. The package `Maintainer` is the
independent `scripting-drafts` project; the original Debian GNOME Maintainers
are credited via `Original-Maintainer`. The unmodified original versions are
listed above.
