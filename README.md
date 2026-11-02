# libgnome-bluetooth-no-discoverability

Unofficial modified rebuilds of Ubuntu 22.04 packages: GNOME Settings and
GNOME Shell asked BlueZ to advertise the machine while scanning. The patches
make both GNOME client libraries send Discoverable=false instead.

- packages/ — `+local2` debs (3.34.5-8+local2, 42.0-5+local2), amd64
- patches/ — Ubuntu source patches; see NOTICE.md and BUILDING.md
- TODO.md, MAINTENANCE.md — remaining work and upgrade reminder
Not from Ubuntu/Canonical. Install with `sudo dpkg -i packages/*.deb`
