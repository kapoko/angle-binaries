# angle-binaries

Compiled dynamic libraries of libEGL and libGLESv2 for use in my own projects.

## How to build

More info: https://github.com/google/angle/blob/main/doc/DevSetup.md

### Clone depot-tools

```sh
git clone https://chromium.googlesource.com/chromium/tools/depot_tools.git
export PATH=/path/to/depot_tools:$PATH
```

### Clone google/angle & prepare
```sh
mkdir angle && cd angle
fetch angle # Clones angle
gclient sync # Necessary?
gn gen out/Release --args='is_debug=false'
```

### Build

```sh
ninja -C out/Release
```

Then copy the `*.dylibs` from `out/Release`
