<div align="center">

# Zen Portable

Ready-to-run Zen Windows x64 portable build. Data stays in the folder; nothing is written to the registry.

[![Release][badge-release]][link-release]
[![Downloads][badge-downloads]][link-release]
[![Build][badge-build]][link-actions]
[![License][badge-license]][link-license]

**[⬇ Download latest][link-release]** · **[📖 User guide][link-usage]**

[简体中文](README.md) | **English**

</div>

> Build system: [Gecko-Portable](https://github.com/Piracola/Gecko-Portable) — this repository is only one of its build configs.

## Navigation

- [Latest release](https://github.com/Piracola/Zen-Portable/releases/latest): grab `Zen_<version>.7z`
- [User guide](./docs/usage.md): layout, config, verification
- [Development](./docs/development.md): CI and local builds
- [Gecko-Portable](https://github.com/Piracola/Gecko-Portable): shared builder
- [Firefox-Portable](https://github.com/Piracola/Firefox-Portable) · [Floorp_portable](https://github.com/Piracola/Floorp_portable)

## About

[Zen Browser](https://zen-browser.app/) is a Firefox-based browser built around a calm interface, split-view browsing, and workspaces. This project takes the official installer as-is and makes it portable with [libportable](https://github.com/adonais/libportable). GitHub Actions rebuilds daily to track official releases.

## Features

- Profile data in `Profiles/`, cache in `Cache/`
- No registry writes — delete the folder to uninstall
- Runs from removable media
- Every release ships a `.sha256` checksum
- Injection check + real portability smoke test before publish

## Quick start

**Install**

1. Open the [latest release](https://github.com/Piracola/Zen-Portable/releases/latest)
2. Download `Zen_<version>.7z` (**not** `Source code`)
3. Extract anywhere, e.g. `D:\Browser\Zen`
4. Double-click `开始.bat` to create a shortcut, then launch via that shortcut

**Update**

1. Close Zen completely
2. Rename the old `Zen` folder to `Zen_old`
3. Extract the new `Zen` folder in place (**keep `Profiles/`**)
4. Confirm data is intact, then delete `Zen_old`

**Uninstall**

Delete the whole extracted folder after backing up `Profiles/` if needed.

## FAQ

**Which file do I download?**  
`Zen_<version>.7z`. `Source code` is not a browser.

**Where is my data?**  
`Profiles/` next to the browser folder.

**Can I run it from a USB drive?**  
Yes. Prefer a short path such as `U:\Zen`.

**Antivirus alert?**  
Portable patching rewrites module imports and is often a false positive. Download only from this repo's Releases and verify the `.sha256` hash.

**Why does the version have letters?**  
Zen's official tags include a suffix (e.g. `1.21.9b`). We reuse them unchanged.

More in the [user guide](./docs/usage.md).

## Related projects

| Project | Notes |
| --- | --- |
| [Gecko-Portable](https://github.com/Piracola/Gecko-Portable) | Shared builder |
| [Firefox-Portable](https://github.com/Piracola/Firefox-Portable) | Portable Firefox |
| [Floorp_portable](https://github.com/Piracola/Floorp_portable) | Portable Floorp |
| [Zen Browser](https://github.com/zen-browser/desktop) | Upstream browser |
| [libportable](https://github.com/adonais/libportable) | Upstream portable runtime |

## License

MIT — see [LICENSE](LICENSE).

Zen Browser itself remains copyright its development team and is covered by its own license. The libportable component ships with the package under its own license.

---

<div align="center">

<sub>Built and maintained by</sub>

**Piracola**

</div>

[badge-release]: https://img.shields.io/github/v/release/Piracola/Zen-Portable?display_name=tag&style=flat-square&color=6366f1&label=Release
[badge-downloads]: https://img.shields.io/github/downloads/Piracola/Zen-Portable/total?style=flat-square&color=2ea043&label=Downloads
[badge-build]: https://img.shields.io/github/actions/workflow/status/Piracola/Zen-Portable/Zen-Portable-package.yml?branch=main&style=flat-square&label=Build
[badge-license]: https://img.shields.io/github/license/Piracola/Zen-Portable?style=flat-square&color=6e7681&label=License

[link-release]: https://github.com/Piracola/Zen-Portable/releases/latest
[link-usage]: ./docs/usage.md
[link-actions]: https://github.com/Piracola/Zen-Portable/actions/workflows/Zen-Portable-package.yml
[link-license]: https://github.com/Piracola/Zen-Portable/blob/main/LICENSE
