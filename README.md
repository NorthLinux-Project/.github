# North Linux Project

An independent Linux userspace ecosystem engineered for deterministic performance, analytical graphics, and verifiable systems architecture.
Developing an integrated desktop and distribution stack across display composition, reactive UI toolkits, and SAT-solved package management.

---

## Architecture & Subsystems

- **Display & Composition**: Wayland compositor in C11 (`wlroots` 0.20.2) supporting DRM/KMS modesetting, virtual workspaces (`ext-workspace-v1`), Cairo-rendered HUD overlays, and declarative window rules.
- **Graphic Interfaces**: GPU-accelerated retain-mode UI toolkit in C++20 with zero exceptions/RTTI, analytic signed distance field (SDF) shaders, per-frame bump arenas, and Material 3 CAM16 HCT color modeling.
- **Package Management**: Daemon-less package manager in C11 (`nlpm`) implementing PubGrub SAT dependency resolution with CDCL, transactional SQLite WAL state, and Zstandard-compressed `.nlpkg` archives.
- **Distribution Tooling**: Declarative build recipe engine (`nlbuild`), binary repository indexer (`nlrepo`), and automated package packaging pipelines.

---

## Core Repositories

- **[north-compositor](https://github.com/NorthLinux-Project/north-compositor)** — Lightweight tiling and floating Wayland compositor written in C11. Integrates bare-metal DRM/KMS modesetting, VT console switching, `ext-workspace-v1` protocols, Cairo-rendered Alt+Tab switcher overlays, and memory arena lifecycles verified with AddressSanitizer.
- **[north-toolkit](https://github.com/NorthLinux-Project/north-toolkit)** — Workstation-grade, GPU-accelerated C++20 UI framework. Features bufferless quad rendering with analytic SDF box shadows, HarfBuzz/FreeType subpixel typography pipelines, reactive dirty-bubbling signals, and pointer-stable slab pools.
- **[nlpm](https://github.com/NorthLinux-Project/nlpm)** — Single-binary package manager for North Linux written in ISO C11. Employs the PubGrub SAT algorithm for conflict resolution, SQLite transactional guarantees, RFC-6234 SHA-256 verification, and parallel libcurl downloads.
- **[packaging](https://github.com/NorthLinux-Project/packaging)** — Central repository recipes and toolchains for building `.nlpkg` packages from `NLBUILD` declarations.
