# libspa-aac

This is a freestanding version of the AAC spa plugin for pipewire. This allows to build and install the AAC plugin on
distributions which do not build pipewire with AAC support, such as Debian.

Dependencies:

- `libspa-0.2-dev`
- `libfdk-aac-dev`
- `libbluetooth-dev`

Build instructions:

- `meson setup build -Dbuildtype=release -Dc_args=-march=native`
- `meson compile -C build`
- `meson install -C build`

The code is taken from https://gitlab.freedesktop.org/pipewire/pipewire
