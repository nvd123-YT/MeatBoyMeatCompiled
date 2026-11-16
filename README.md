# Super Meat Boy Recompiled

A dedicated desktop build of [ScarletNX](https://github.com/scarletnx/ScarletNX), configured for the Nintendo Switch version of **Super Meat Boy**.

This fork keeps ScarletNX's Switch recompilation engine and runtime while tailoring the desktop launcher to this game. The launcher focuses on loading the Super Meat Boy game dump, compiling it for the current computer, and starting it. Unrelated console loaders and the general-purpose first-run setup are excluded from the desktop build.

## Platforms

- **macOS** (Apple silicon)
- **Windows** (x86-64)
- **Linux** (x86-64 and supported ARM64 builds)

The first release target is **1.0.0**. Builds and release packages are produced with this repository's GitHub Actions workflows. A release is published after its version tag has built successfully.

## Build from source

Install the prerequisites described in [ScarletNX's build documentation](docs/dev/build.md), then use the game-specific presets:

```sh
# Linux or Windows host
cmake --preset meatboy
cmake --build --preset meatboy

# Apple-silicon macOS
cmake --preset meatboy-macos
cmake --build --preset meatboy-macos
```

No commercial game data, console firmware, keys, or copyrighted assets are included in this repository or its releases. Users must provide game data they are legally entitled to use.

## Credits and license

- **ScarletNX contributors** — original recompiler, Switch runtime, and launcher framework.
- **Super Meat Boy** — game by Team Meat; this project is an unofficial, independent community build and is not endorsed by or affiliated with Team Meat.

This project is distributed under [GPL-3.0-or-later](LICENSE). The original ScarletNX license notices and third-party attributions are preserved in the source tree.
