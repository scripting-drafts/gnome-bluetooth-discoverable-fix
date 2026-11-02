# TODO

## Keep Pairable off while GNOME Settings is open

GNOME Settings' Bluetooth panel sets the adapter Pairable=yes while the
panel is open (it returns to no on close). This does not advertise the
machine, but a device that already knows its address can attempt pairing.

Development: patch the panel/widget to leave Pairable false during
scanning, rebuild the affected package, and verify with `bluetoothctl show`.
