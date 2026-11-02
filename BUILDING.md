# Building

The packages were built from the matching Ubuntu 22.04 source packages with
the patches in `patches/` applied.

- gnome-bluetooth 3.34.5-8:
  http://archive.ubuntu.com/ubuntu/pool/main/g/gnome-bluetooth/
- gnome-bluetooth3 42.0-5:
  http://archive.ubuntu.com/ubuntu/pool/main/g/gnome-bluetooth3/

Apply the patch to `debian/patches/series`, then build with:

```
DEB_BUILD_OPTIONS=nodoc,nocheck dpkg-buildpackage -b -uc -us
```
