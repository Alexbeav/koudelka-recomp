# Koudelka release feasibility

Status: `bootstrap_verified`; four-platform `v0.3.5` package pending exact-package gates

The operator confirmed that the promoted private Disc 1 build reaches
gameplay. This source-only pilot does not inherit that claim. It must pass the
exact-package setup, generation, build, and startup gates before it can claim
`bootstrap_verified`.

The owned PAL set contains four serials: `SLES-02897`, `SLES-12897`,
`SLES-22897`, and `SLES-32897`. Every disc has the same boot executable
SHA-256, `661bd13917e21032dcfe98ca012011d1021cb79f45688aa4c50a75e6d7d95390`.
The frozen verifier therefore classifies the set as one program on four data
images. One setup host is valid.

The package must validate and remember all four discs. Mid-session disc change
remains a separate gameplay seam. The public package must not contain a disc,
a BIOS, generated retail code, a save, a prebuilt title executable, or a
private absolute path.

## v0.3.3 executable-name correction

Public `v0.3.0` can complete a build and then request the wrong executable.
The corrected source uses `Koudelka_Recompiled` for CMake, the setup relaunch, and packaging.
The 24-title source parity gate passes. An exact-ZIP automatic-relaunch canary
must pass before release authorization.

## v0.3.5 three-platform refresh

The candidate targets Windows x64, Linux x64, macOS Apple Silicon ARM64, and
macOS Intel x64. The setup package uses an additive framework correction that
excludes two non-SDK helpers with developer-machine paths. Each exact package
must pass the payload, setup, startup, responsiveness, and clean-exit gates on
its declared platform before publication.

## 2026-09-03 portable Linux package

The release workflow now builds Linux in a pinned Ubuntu 20.04 container.
The package gate rejects a setup host or emitter that needs a glibc version
newer than 2.31. This keeps the release compatible with the qualified Rocky
Linux 9 host. Windows and both macOS builds keep their existing runners.
