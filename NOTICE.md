# NOTICE

These are unofficial modified rebuilds of Ubuntu 22.04 packages.

- `libgnome-bluetooth13` 3.34.5-8+local1
  from gnome-bluetooth 3.34.5-8 (Settings panel)
- `libgnome-bluetooth-3.0-13` 42.0-5+local1
  from gnome-bluetooth3 42.0-5 (GNOME Shell)

The changes are limited to the patches in `patches/`: both GNOME clients now
send `Discoverable=false` instead of asking BlueZ to advertise the machine
while scanning.

These packages are not produced, endorsed, or supported by Ubuntu, Canonical,
Debian, or the GNOME Project. They retain the upstream license; each package
contains its Debian copyright file. Exact source URLs and checksums are in
`SOURCE`; build steps are in `BUILDING.md`.

The `+local1` suffix marks the local modification. The unmodified original
versions are listed above.
