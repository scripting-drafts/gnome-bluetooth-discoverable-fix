# Maintenance

On the install machine the two patched packages are held:

```
sudo apt-mark showhold
libgnome-bluetooth13
libgnome-bluetooth-3.0-13
```

The hold stops `apt upgrade` from replacing the patched libraries, but it also
blocks their security updates. When Ubuntu publishes a newer version:

1. Unhold the package.
2. Fetch the new Ubuntu source, apply the patch, bump `+local2` to `+local3`
   (or the next suffix), and rebuild.
3. Install the new debs and re-hold.
4. Re-verify with `bluetoothctl show` while Settings or GNOME Shell scans.

Do not leave the hold in place indefinitely. Check for a newer version with
`apt-cache policy libgnome-bluetooth13 libgnome-bluetooth-3.0-13`.
