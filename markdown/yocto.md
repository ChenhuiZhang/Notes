# Yocto

## Bitbake

[Manual](https://www.yoctoproject.org/docs/1.6/bitbake-user-manual/bitbake-user-manual.html)

1. SRC_URI

To apply patch for specific *machine*:

> SRC_URI += "file://foo.patch"

> SRC_URI_append_machine += "file://bar.patch"

either:

> SRC_URI_machine += "file://foo.patch file://bar.patch"

2. dependencies

bitbake -g recipe-name -u taskexp

3. Enable debug

Add below in local.conf or recipie

DEBUG_BUILD_pn-audiocontrol = "1"
