# GNOME Bluetooth discoverability fix

Ubuntu 22.04 GNOME Settings and GNOME Shell asked BlueZ to advertise the
machine while scanning. BlueZ's reaction is documented; these patches make
both GNOME client libraries send Discoverable=false instead.

- packages/ — amd64 debs for the patched libraries (42.0-5, 3.34.5-8)
- patches/ — corresponding Ubuntu source patches
- TODO.md — remaining Pairable behavior
Install after a package upgrade: `sudo dpkg -i packages/*.deb`
