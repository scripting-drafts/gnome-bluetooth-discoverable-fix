# Building

These packages are modified rebuilds of the Ubuntu 22.04 sources listed in
`SOURCE`. The local version is `+local1`; each changelog entry and
`debian/<package>.docs` install a `README.modified` file.

Enable `deb-src` in APT, then install the build dependencies:

```
sudo apt-get build-dep gnome-bluetooth gnome-bluetooth3
```

Extract the source packages, add the matching patch to
`debian/patches/series`, add the `+local1` changelog entry, then build:

```
DEB_BUILD_OPTIONS=nodoc,nocheck dpkg-buildpackage -b -uc -us
```

The build must run in Ubuntu 22.04 (jammy) or a matching container.
